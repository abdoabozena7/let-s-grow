# Study My Way 👑

**Your portable Egyptian-Arabic tutor and AI-first codebase explainer — for GitHub Copilot and ChatGPT.**  
مذاكرة أي مادة بطريقتك، وكمان فهم الـcodebase كقصة: المشكلة → الـapproach → مسؤوليات الملفات → مراجعة قرارات التصميم، من غير الغرق في syntax.

## 🧠 NEW: Codebase Story Mode for GitHub Copilot

Use **the same skill** for two modes: **Codebase Story Mode** when exploring real engineering code, or **Exam Study Mode** when studying lectures and solving instructor problems. The original exam-tutoring rules remain intact.

With Copilot connected to the files your workplace permits, the code mode explains: **the actual problem → why this approach → real input/decision/output flow → verified groups of files → architectural trade-offs → AI-generated-code review questions**. It deliberately avoids syntax, invented file responsibilities and forced quizzes until you ask for technical depth. **NEW:** No Logical Jumps—every important term, number, threshold, transformation and decision gets a clear meaning, evidence, small before/after example, negative path when relevant, and handoff to the next stage. Conceptual depth is **not** technical syntax.

**[Copilot setup and copyable prompts](COPILOT-SETUP.md)** · **[Codebase storytelling protocol](references/codebase-storytelling.md)** · **[Example explanations](references/codebase-examples.md)**

Recommended personal installation path: `%USERPROFILE%\.copilot\skills\study-my-way\SKILL.md` (Windows). Install this repository's **root contents** into that directory, then verify the skill in Copilot Agent Mode. Follow the guide for steps and enterprise-policy caveats.

```text
/study-my-way اشرحلي الـ feature دي من أول المشكلة للـ approach،
وبعدين اربط كل خطوة بالملفات الحقيقية. من غير technical تفاصيل دلوقتي.
```

## 📥 Use in another ChatGPT account

**Repository:** https://github.com/abdoabozena7/let-s-grow

1. Open this repository and choose **Code → Download ZIP**.
2. Extract the archive. The skill entry point is **SKILL.md**, alongside **references/** and **agents/**.
3. On the target account, if custom Skills upload is available, upload a ZIP that contains these files directly at its root (not in an extra nested folder). You can create such a ZIP from the extracted folder contents.
4. Start a new chat, upload your lectures, then type:

> ذاكر معايا المادة دي بطريقتي. حلل المحاضرات كلها، استخرج المسائل والنظري، وابدأ بأول مسألة.

**If custom Skills upload is unavailable:** give the target ChatGPT a link to `SKILL.md` in this repository and ask it to read and follow that document, along with the linked files in `references/`. This is prompt-based use, not a guaranteed native Skill installation. You can also copy the files into the chat if GitHub access is unavailable.

## 🔍 Core workflow

**Audit lectures → map questions and theory → solve lecturer-worked problems one micro-step at a time → exam-ready theory → active-recall and cheat sheets.**

- Egyptian Arabic explanation + English technical terms and exam answers.
- Don't assume what page hints were omitted; audit supplied documents.
- Ask one decision-based question per step (not mindless arithmetic).
- Show complete resulting tables and matrices when skipping repetitive calculations.
- End every completed problem with a full ordered recap.
- Use mental links, comparison prompts, practical exam answer forms, and spaced recall.
- Distinguish a slide typo from validated calculations; never invent lecturer outputs.

## 📂 Files

| File | Purpose |
| --- | --- |
| [SKILL.md](SKILL.md) | Routing between codebase-story mode and original exam tutor |
| [Copilot setup](COPILOT-SETUP.md) | Personal install, approved workspace use and prompts |
| [Codebase storytelling](references/codebase-storytelling.md) | Problem-first reasoning and verified file map |
| [Codebase examples](references/codebase-examples.md) | Egyptian-style conceptual explanations |
| [Intake and coverage](references/intake-and-coverage.md) | Lecture auditing and coverage |
| [Procedural tutoring](references/procedural-tutoring.md) | Numerical problems, code, diagrams |
| [Theory and retention](references/theory-and-retention.md) | Exam theory and mental links |
| [Output templates](references/output-templates.md) | Maps, tables, checkpoints, recap |
| [Acceptance scenarios](references/acceptance-scenarios.md) | Behavior test cases |
| [Agent metadata](agents/openai.yaml) | UI metadata |

## ⚠️ Portable, not account-synced

This repository contains the actual tutor instructions, independent of any one ChatGPT account's memory. Sharing a repository URL does not automatically install a native Skill in someone else's account; the account must have suitable skill functionality or read the instructions manually. Changes to this repository do not automatically update a previously uploaded ZIP.

MIT-style sharing is not presumed; please respect the repository owner's preferred licensing terms.
