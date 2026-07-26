<div align="center">

<a href="https://github.com/CSQ-AN94/textbook-tutor-skill"><img src="https://img.shields.io/badge/语言-简体中文-2563EB?style=for-the-badge" alt="简体中文"></a>
<a href="https://github.com/CSQ-AN94/textbook-tutor-skill/tree/english"><img src="https://img.shields.io/badge/Language-English-111827?style=for-the-badge" alt="English"></a>

# 📚 Textbook Tutor

**把复杂知识写成真正能从零读懂的教材。**

An OpenAI Codex skill for creating self-contained, textbook-style tutorials from first principles.

[![Codex Skill](https://img.shields.io/badge/Codex-Skill-111827?style=for-the-badge)](./textbook-tutor/SKILL.md)
[![Markdown](https://img.shields.io/badge/Output-Markdown-2563EB?style=for-the-badge)](https://www.markdownguide.org/)
[![License](https://img.shields.io/github/license/CSQ-AN94/textbook-tutor-skill?style=for-the-badge&label=%E2%9A%96%EF%B8%8F%20License&color=22C55E)](./LICENSE)

</div>

---

## 它解决什么问题？

很多“教程”只是把术语换成项目符号，仍然默认读者已经懂了大量前置知识。

Textbook Tutor 要求 Codex 像一位耐心的教材作者那样写作：

- 从第一性原理开始，不隐藏前置知识；
- 先讲定义和直觉，再进入公式、代码与方法；
- 用完整算例展示每一个中间步骤；
- 为每个核心概念提供例子、反例、常见误区和检查题；
- 用分级练习、答案和综合项目检验真正理解；
- 默认产出结构完整、可长期阅读的 Markdown 教材。

## 一分钟安装

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

安装后重启 Codex。

## 立即试用

在 Codex 中输入：

```text
请使用 $textbook-tutor，从零开始写一章线性代数教材。
假设我只会基本算术，必须包含完整算例、练习答案和一个综合项目。
```

也可以直接描述任务，Codex 会在合适时自动调用这个 skill：

```text
Write a self-contained textbook chapter that teaches graph algorithms
to a complete beginner, with hand-traced examples, exercises, and a project.
```

## 教学方法

一篇完整教材通常遵循这条学习路径：

```text
学习目标
   ↓
零基础前置知识
   ↓
全局概念地图
   ↓
逐个核心概念
   ↓
完整推导与算例
   ↓
误区和边界情况
   ↓
分级练习与答案
   ↓
综合项目与评分标准
```

对于数学、算法和形式化符号，skill 还会强制执行更严格的标准：

1. 使用任何工具前，先解释它是什么、为什么需要它；
2. 用小而清晰的数字写出全部计算步骤；
3. 算法必须在纸面上逐轮运行，并展示数据结构如何变化；
4. 不使用“显然”“容易看出”“读者应该熟悉”等跳步表达；
5. 读者应当能从第一页读到最后一页，而不必另找一本书补课。

## 适合这些任务

- 从零编写某个主题的完整教程；
- 为课程设计章节、模块或学习路线；
- 把论文、代码库或技术概念改写成初学者教材；
- 制作包含习题、答案、项目和评分标准的学习材料；
- 用中文教学，同时保留标准英文术语；
- 解释数学、算法、工程和编程主题中的隐藏前置知识。

## 仓库结构

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

- `SKILL.md`：触发条件与核心工作流程；
- `lesson-blueprint.md`：完整教材的结构蓝图；
- `zero-background-math.md`：数学、算法和符号教学的零基础标准；
- `openai.yaml`：Codex 中展示所需的界面元数据。

## 更新

```bash
cd textbook-tutor-skill
git pull
cp -R textbook-tutor ~/.codex/skills/
```

## 参与改进

欢迎提交 Issue 或 Pull Request。尤其欢迎：

- 更真实的教材写作测试案例；
- 对初学者不友好的跳步或术语；
- 更好的练习、项目和掌握度检查方法；
- 不同语言和学科中的教学经验。

## License

⚖️ 本仓库采用 [MIT License](./LICENSE)，并已被 GitHub 原生许可证检测识别。你可以自由使用、修改与分享，但请保留许可证声明。
