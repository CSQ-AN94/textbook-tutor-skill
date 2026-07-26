<div align="center">

<a href="./README.md"><img src="https://img.shields.io/badge/Language-Chinese-111827?style=for-the-badge" alt="Chinese"></a>
<a href="./README_EN.md"><img src="https://img.shields.io/badge/Language-English-2563EB?style=for-the-badge" alt="English"></a>

# 📚 Textbook Tutor

**Turn complex knowledge into a textbook that a true beginner can actually understand.**

An OpenAI Codex skill for creating self-contained, textbook-style tutorials from first principles.

[![Codex Skill](https://img.shields.io/badge/Codex-Skill-111827?style=for-the-badge)](./textbook-tutor/SKILL.md)
[![Markdown](https://img.shields.io/badge/Output-Markdown-2563EB?style=for-the-badge)](https://www.markdownguide.org/)
[![License](https://img.shields.io/github/license/CSQ-AN94/textbook-tutor-skill?style=for-the-badge&label=%E2%9A%96%EF%B8%8F%20License&color=22C55E)](./LICENSE)

</div>

---

## What problem does it solve?

Many tutorials merely replace jargon with bullet points while still assuming that the reader already understands a long list of hidden prerequisites.

Textbook Tutor asks Codex to write like a patient textbook author:

- Start from first principles without hiding prerequisites.
- Explain definitions and intuition before formulas, code, and procedures.
- Show every intermediate step in worked examples.
- Give each core concept an example, a non-example, a common misconception, and a checkpoint question.
- Test real understanding through graded exercises, solutions, and an integrative project.
- Produce a structured Markdown chapter designed for careful, long-term reading.

## Install in one minute

### macOS / Linux

```bash
git clone https://github.com/CSQ-AN94/textbook-tutor-skill.git
mkdir -p ~/.codex/skills
cp -R textbook-tutor-skill/textbook-tutor ~/.codex/skills/
```

### Windows PowerShell

```powershell
git clone https://github.com/CSQ-AN94/textbook-tutor-skill.git
New-Item -ItemType Directory -Force "$HOME\.codex\skills"
Copy-Item -Recurse textbook-tutor-skill\textbook-tutor "$HOME\.codex\skills\"
```

Restart Codex after installation.

## Try it

Enter this prompt in Codex:

```text
Use $textbook-tutor to write a linear algebra chapter from first principles.
Assume that I only know basic arithmetic. Include complete worked examples,
solutions to the exercises, and one integrative project.
```

You can also describe the task naturally. Codex will invoke the skill automatically when appropriate:

```text
Write a self-contained textbook chapter that teaches graph algorithms
to a complete beginner, with hand-traced examples, exercises, and a project.
```

## Teaching method

A complete chapter usually follows this learning path:

```text
Learning objectives
   ↓
Zero-background foundations
   ↓
Big-picture concept map
   ↓
Core concepts, one at a time
   ↓
Complete derivations and worked examples
   ↓
Misconceptions and boundary cases
   ↓
Graded exercises with solutions
   ↓
Integrative project with a rubric
```

For mathematics, algorithms, and formal notation, the skill enforces an even stricter standard:

1. Explain what each tool is and why it is needed before using it.
2. Write out every calculation using small, readable numbers.
3. Hand-trace algorithms one iteration at a time and show how each data structure changes.
4. Avoid shortcuts such as “obviously,” “it is easy to see,” and “the reader should be familiar with.”
5. Make the chapter self-contained enough to read from the first page to the last without another textbook.

## Good use cases

- Write a complete beginner tutorial on a bounded topic.
- Design a chapter, course module, or learning path.
- Turn a paper, codebase, or technical idea into beginner-friendly teaching material.
- Create learning material with exercises, solutions, projects, and evaluation rubrics.
- Teach in clear language while retaining standard technical terminology.
- Reveal and teach the hidden prerequisites behind mathematics, algorithms, engineering, and programming.

## Repository structure

```text
textbook-tutor-skill/
├── README.md
├── README_EN.md
├── LICENSE
└── textbook-tutor/
    ├── SKILL.md
    ├── agents/
    │   └── openai.yaml
    └── references/
        ├── lesson-blueprint.md
        └── zero-background-math.md
```

- `SKILL.md`: Triggering conditions and the core workflow.
- `lesson-blueprint.md`: The structural blueprint for a complete textbook chapter.
- `zero-background-math.md`: The zero-background standard for mathematics, algorithms, and notation.
- `openai.yaml`: Interface metadata used by Codex.

## Update

```bash
cd textbook-tutor-skill
git pull
cp -R textbook-tutor ~/.codex/skills/
```

## Contributing

Issues and pull requests are welcome, especially for:

- Realistic textbook-writing test cases.
- Steps or terminology that remain unfriendly to beginners.
- Better exercises, projects, and mastery checks.
- Teaching experience from different languages and subject areas.

## License

⚖️ This repository is available under the [MIT License](./LICENSE), recognized by GitHub's native license detection. You may use, modify, and share it freely while retaining the license notice.
