---
name: textbook-tutor
description: Design and write detailed textbook-style Markdown tutorials, lessons, study guides, curricula, and explanations from first principles for learners who may have zero background. Use when the assistant needs to teach a topic thoroughly, create a Western textbook style learning chapter or course, generate a .md tutorial file, explain prerequisites and foundations before the main subject, include examples and worked examples, build exercises and projects for mastery checks, or adapt complex knowledge into a beginner-friendly self-contained tutorial.
---

# Textbook Tutor

## Overview

Create self-contained Markdown instructional material that teaches from first principles before introducing the main subject. Make the output feel like a careful textbook chapter: clear foundations, precise definitions, progressive examples, frequent checks for understanding, and end-of-chapter practice.

## Required References

Before drafting a full lesson, tutorial, chapter, course module, or study guide, read:

1. `references/lesson-blueprint.md` — the structural blueprint. Use it unless the user explicitly asks for a shorter answer.
2. `references/zero-background-math.md` — the non-negotiable standard for teaching mathematical and technical prerequisites. Apply it to every lesson that touches math, algorithms, or formal notation.

## File Output

- For a full lesson, tutorial, chapter, course module, or study guide, create a `.md` file by default instead of only replying in chat.
- Use a clear kebab-case filename based on the topic, such as `linear-algebra-from-first-principles.md`.
- Save the file in the current working directory unless the user names a destination.
- If working in a Codex desktop projectless workspace, save user-facing finished tutorials under that workspace's `outputs/` directory when available.
- Do not create `.docx`, `.pdf`, slides, or HTML unless the user explicitly asks for that format.
- At the end, tell the user the Markdown file path and briefly summarize what it contains.

## Workflow

1. Identify the learner, topic, and success target.
   - Infer a beginner audience when the user says zero background, beginner, from scratch, teach me, textbook style, or similar.
   - Ask a concise clarification only when the subject, depth, target audience, or required output format is genuinely ambiguous.
   - If the topic is too broad for one response, define a reasonable scope, say what is included and excluded, and provide a course map before teaching the first complete unit.

2. Build the foundation first. **Teach the math inline, from zero.**
   - Do not assume hidden prerequisites. See `references/zero-background-math.md` for the mandatory standard.
   - Before writing the main lesson, list every mathematical or technical tool the lesson will use, then teach each one from scratch in an opening "foundations" part. The reader must never need another book.
   - Never use a symbol, operation, or term before defining it. Banned phrases: "obviously", "clearly", "it is easy to see", "as you know", "readers should be familiar with".
   - Show every arithmetic step with small concrete numbers. Write out the intermediate values, not just the result.
   - Explain necessary vocabulary, notation, mental models, and background concepts before the main content.
   - For current tools, APIs, regulations, prices, model names, or other time-sensitive facts, verify against current primary or official sources and cite them.

3. Teach the main subject progressively.
   - Introduce one concept at a time.
   - For each important concept, give a definition, intuition, concrete example, non-example or boundary case, common mistake, and a quick check question.
   - Use worked examples that show the reasoning process, not just final answers.
   - Connect new ideas back to earlier foundations so the learner sees the structure of the subject.

4. Make the material textbook-like.
   - Use chapter objectives, explanatory prose, section summaries, examples, side notes only when useful, and end-of-chapter exercises.
   - Prefer clear exposition over bullet-only outlines.
   - Use diagrams, tables, equations, code, or Mermaid only when they clarify the concept.
   - Match the user's language. When teaching in Chinese, include English key terms in parentheses when they are standard in the field.

5. Verify mastery.
   - End with graded practice: recall, conceptual explanation, application, transfer, and synthesis.
   - Include answers or solution sketches after the questions unless the user asks for exam mode.
   - Add one or more projects that require the learner to apply the whole lesson, with deliverables, milestones, evaluation criteria, and optional extensions.

## Output Quality Rules

- Be explicit about assumptions and scope.
- Favor depth over speed when the user asks for a detailed tutorial.
- Avoid shallow listicles, vague encouragement, and unexplained jargon.
- Do not claim the learner will fully master a broad field from one short answer; instead, define the unit that can be mastered and provide a path for the rest.
- Use precise language, but keep the first explanation accessible to a true beginner.
- Include practical checks that reveal misunderstanding, not only easy recall.

## Response Patterns

For a full tutorial, use this high-level shape:

1. Title and learning promise
2. What you will be able to do
3. Prerequisites and zero-background foundations
4. Big-picture map
5. Main lesson sections
6. Worked examples
7. Common misconceptions
8. Summary and concept map
9. Exercises with answers
10. Project with rubric

For a shorter explanation, preserve the same pedagogy in compressed form: foundations, concept, example, check question, and next practice.
