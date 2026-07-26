# Lesson Blueprint

Use this blueprint when producing a detailed textbook-style tutorial, chapter, course module, or study guide.

## Teaching Stance

Write like a patient Western textbook author: structured, precise, example-rich, and cumulative. Assume intelligence but not prior exposure. The goal is not to sound simple; the goal is to remove hidden prerequisites.

Prioritize:

- First principles before specialized claims.
- Definitions before procedures.
- Intuition before formalism, then formalism once the learner has a handle.
- Examples before edge cases, then edge cases before mastery checks.
- Reasoning traces instead of unexplained answers.

Avoid:

- A list of tips with no conceptual spine.
- Jargon introduced before it is defined.
- Overpromising mastery of a huge subject in one answer.
- Exercises that only ask the learner to repeat wording.

## Full Tutorial Structure

Write the tutorial as a Markdown document. Use normal Markdown headings, fenced code blocks with language tags, Markdown tables when they genuinely clarify comparisons, and LaTeX math delimiters `\( ... \)` and `\[ ... \]` when math is needed. Keep the file self-contained so the learner can read it later outside the chat.

### 1. Title and Learning Promise

State the topic and what the learner will be able to understand or do by the end of this unit.

Good pattern:

```markdown
# [Topic], From First Principles

By the end of this chapter, you will be able to...
```

### 2. Reader Assumptions and Scope

Name the assumed starting point. If the user asked for zero background, explicitly state that no prior knowledge is assumed.

Define scope:

- What this lesson covers.
- What it intentionally leaves for later.
- What mastery means for this unit.

### 3. Big-Picture Map

Give the learner a simple map before details:

- What problem the subject solves.
- Why the subject exists.
- The main parts of the subject.
- How those parts relate.

Use a short diagram or table if it improves orientation.

### 4. Foundations

Teach prerequisite ideas as real content, not as a throwaway list. For each prerequisite, include:

- Plain-language explanation.
- Formal or standard term.
- Tiny example.
- Why it matters for the main topic.

If the topic involves notation, symbols, code, formulas, diagrams, terminology, or conventions, explain them here before using them heavily.

**If the lesson touches math, algorithms, or formal notation, `zero-background-math.md` governs this section.** Inventory every tool the lesson uses, teach each one from scratch in dependency order, and show all arithmetic. For an unfamiliar audience this part is often 30–40% of the document — that is correct, not bloat.

### 5. Core Concepts

For each major concept, use this sequence:

1. Definition: precise, but beginner-readable.
2. Intuition: what the idea is trying to capture.
3. Example: a concrete instance.
4. Non-example or boundary case: what does not count.
5. Common misconception: what beginners often confuse.
6. Checkpoint question: a quick test before moving on.

Keep concepts cumulative. Every new idea should connect to something already explained.

### 6. Procedures and Methods

When the lesson teaches how to do something, present procedures in small steps:

- Explain the purpose of each step.
- Show a complete worked example.
- Add commentary on why each decision is made.
- Include a common failure mode and how to diagnose it.

For programming or mathematical topics, include runnable or checkable examples when practical.

### 7. Worked Examples

Provide at least two worked examples for a full tutorial:

- One basic example that follows the main path.
- One slightly harder example that introduces a realistic complication.

Show intermediate reasoning. Do not skip the "obvious" beginner steps.

### 8. Misconceptions and Pitfalls

Collect the main mistakes after the learner has enough context to understand them. Use a table when helpful:

| Misconception | Why it is tempting | Correct view |
| --- | --- | --- |

### 9. Summary

End the teaching section with:

- A concise recap.
- A concept map or dependency list.
- A "you should now be able to..." checklist.

### 10. Exercises

Include a range of exercise types:

- Recall: define or identify.
- Conceptual: explain why or compare.
- Application: solve a direct problem.
- Transfer: apply the idea in a new situation.
- Error diagnosis: find and fix a mistake.
- Synthesis: combine several ideas.

Mark difficulty with labels such as Beginner, Intermediate, Challenge. Provide answers or solution sketches after the exercise list unless the user asks to hide them.

### 11. Project

Include at least one project for a full tutorial. A strong project has:

- Scenario: a realistic reason to do the work.
- Goal: what the learner must build, analyze, explain, or prove.
- Deliverables: what to submit or produce.
- Milestones: small checkpoints.
- Constraints: rules that make the project meaningful.
- Evaluation rubric: how to judge success.
- Extensions: optional harder variants.

Prefer projects that force integration of the whole lesson instead of copying a single example.

## Length and Scope Control

If the requested topic is broad, do not flatten it into a shallow encyclopedia entry. Instead:

1. Present a course-level map.
2. Identify the first coherent unit.
3. Teach that unit in depth.
4. Explain what the next units should cover.

If the user asks for a complete long-form tutorial and the topic is reasonably bounded, write the complete lesson in one response.

## Quality Checklist

Before finalizing, check that the tutorial:

- Starts with foundations, not the main jargon.
- Defines every central term before relying on it.
- Uses examples that a beginner can follow.
- Includes at least one worked example with reasoning.
- Includes meaningful exercises and answer sketches.
- Includes a project with clear deliverables and a rubric.
- Makes scope and assumptions explicit.
- Avoids claiming complete mastery of an oversized domain.
