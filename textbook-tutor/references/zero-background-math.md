# Zero-Background Math Standard

The non-negotiable standard for teaching mathematical, algorithmic, and formal-notation prerequisites. Apply to every lesson that uses math, algorithms, or symbolic notation.

## The Core Rule

> **The reader must be able to go from the first page to the last without opening another book.**

If the lesson uses a dot product, teach the dot product. If it uses a matrix, teach what a matrix is. If it uses a derivative, teach what a derivative is. No exceptions, no "for a refresher, see...", no external links as a substitute for teaching.

Assume the reader knows: arithmetic (add, subtract, multiply, divide), square roots, and how to read a simple graph. Assume nothing else. Not algebra fluency, not trigonometry, not linear algebra, not calculus, not big-O, not any programming beyond reading a few lines.

## Mandatory Structure

Every math-touching lesson opens with a **foundations part** that is a real part of the document, not a bulleted warm-up.

1. **Before drafting, inventory the tools.** List every mathematical object, operation, and notation the lesson will use. This list becomes the foundations part's table of contents.
2. **Teach each tool in dependency order.** A tool may only use tools already taught. If §5 needs the norm, the norm is taught in §3 or §4.
3. **Then teach the main subject**, referring back by section number ("using the projection formula from §4.3").

Sizing guidance: for a genuinely unfamiliar audience the foundations part is often 30–40% of the document. That is correct, not bloat.

## Per-Tool Teaching Pattern

For each mathematical tool, in this order:

1. **What it is** — plain language, before any symbol. ("A matrix is a rectangular table of numbers. That's it — nothing more mysterious.")
2. **Why we need it** — what problem it solves in this lesson.
3. **How to compute it** — the rule, stated operationally.
4. **Worked arithmetic** — at least one full computation with small concrete numbers, every intermediate value written out.
5. **Geometric or physical intuition** — what it *means*, ideally with an ASCII diagram.
6. **A check question with its answer.**

## Banned Moves

Never write these. Each one silently assumes the reader already knows the thing being taught.

| Banned | Why it fails | Do instead |
| --- | --- | --- |
| "obviously", "clearly", "easy to see" | If it were obvious the reader wouldn't be reading | Show the step |
| "as you know", "recall that", "readers familiar with…" | Assumes prior exposure | Teach it |
| "it can be shown that" | Hides the reasoning | Show it, or say explicitly "we take this on faith here, and here's why it's believable" |
| Using a symbol before defining it | Reader stalls and can't recover | Define on first use, every time |
| Stating a formula with no worked example | Formula without arithmetic is not teaching | Always follow a formula with numbers |
| Giving only the final answer | Hides the method | Write every intermediate value |
| "left as an exercise" for a core step | Core steps are the lesson | Reserve for genuine practice only |

## Arithmetic Must Be Visible

Wrong:

> The projection ratio is \(a = 0.5\), so the point lies at the midpoint.

Right:

> **Step 1**, the two vectors:
> \[\mathbf p-\mathbf s=(0.10,\ 0.03,\ 0),\qquad \mathbf t-\mathbf s=(0.20,\ 0,\ 0).\]
> **Step 2**, the numerator (dot product):
> \[(0.10)(0.20)+(0.03)(0)+(0)(0)=0.02+0+0=0.02.\]
> **Step 3**, the denominator:
> \[\lVert\mathbf t-\mathbf s\rVert^2=0.20^2+0^2+0^2=0.04.\]
> **Step 4**:
> \[a=\frac{0.02}{0.04}=0.5.\]
> So the point's shadow lands exactly at the midpoint of the segment.

Use small round numbers chosen so the arithmetic is checkable by hand. Prefer 3-4-5 triangles, halves, and tenths over realistic-but-ugly values. Realistic values belong in the applied sections, after the mechanics are clear.

## Algorithms Must Be Hand-Traceable

An algorithm is not taught until the reader has watched it run on paper.

- **Trace it step by step on a tiny instance.** Number the iterations. For each one, write out every quantity the algorithm computes — not just the outcome.
- **Include at least one failing or rejected step.** Learners who only see the happy path believe failure is a bug. Show a collision rejection, a backtrack, a candidate that doesn't pass.
- **Show the data structure evolving** after each step (the tree, the queue, the visited set).
- **Then, and only then,** give the pseudocode or real code, and map it line-by-line back to the trace.

## Abstractions Need Concrete Numbers

When claiming something is large, small, fast, slow, or infeasible, **compute it**.

Wrong: "grid search suffers from the curse of dimensionality and becomes intractable in high dimensions."

Right: a table from 1 to 7 dimensions showing \(10^n\) grid points, then: \(10^7 \times 0.1\,\mathrm{ms} = 1000\,\mathrm{s} \approx 17\) minutes — and at \(k=100\), \(10^{14}\times 0.1\,\mathrm{ms} \approx 317\) years.

The number is what makes the abstraction land.

## Notation Discipline

- Introduce notation in a small table when several symbols arrive together.
- Re-state a symbol's meaning when it reappears after a long gap. Repetition is a feature.
- Say how to *read* unfamiliar notation aloud: \(\dot{\mathbf q}\) is "q dot"; \(\lceil x\rceil\) is "ceiling of x"; \(\lVert\mathbf v\rVert\) is "the norm, or length, of v".
- When a field uses several names for one thing, list them all once: "norm, magnitude, length, Euclidean distance — same thing."

## Checkpoints and Practice

- A short check question after each concept, with its answer immediately visible (mark them so they're skimmable, e.g. a pencil emoji).
- End-of-chapter exercises graded Beginner / Intermediate / Challenge, with full answers — including the arithmetic, not just final values.
- At least one Challenge exercise should be **diagnostic**: give a plausible-but-wrong fix to a real failure and ask the learner to say why it's wrong and what the actual root cause is.

## Connecting to Real Code

When the lesson explains a real codebase:

- Quote the actual lines, then map each line back to the formula taught earlier, by section number.
- Explain **why** the code makes each choice (why `ceil` and not `round`; why `max` across joints and not the mean).
- Prefer real production failures with real dates and real numbers over invented examples. A genuine postmortem is the best teaching material available.
- Be honest about what is verified versus what is only calculated. If a value was derived but never tested in production, say so plainly.
