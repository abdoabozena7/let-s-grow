# Study My Way 👑

**Your portable, exam-first, subject-agnostic tutoring skill.**  
مذاكرة أي مادة بطريقتك — من المحاضرات للمسائل للنظري للمراجعة النهائية.

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
| [SKILL.md](SKILL.md) | Core tutor rules and routing |
| [Intake and coverage](references/intake-and-coverage.md) | Lecture auditing and coverage |
| [Procedural tutoring](references/procedural-tutoring.md) | Numerical problems, code, diagrams |
| [Theory and retention](references/theory-and-retention.md) | Exam theory and mental links |
| [Output templates](references/output-templates.md) | Maps, tables, checkpoints, recap |
| [Acceptance scenarios](references/acceptance-scenarios.md) | Behavior test cases |
| [Agent metadata](agents/openai.yaml) | UI metadata |

## ⚠️ Portable, not account-synced

This repository contains the actual tutor instructions, independent of any one ChatGPT account's memory. Sharing a repository URL does not automatically install a native Skill in someone else's account; the account must have suitable skill functionality or read the instructions manually. Changes to this repository do not automatically update a previously uploaded ZIP.

MIT-style sharing is not presumed; please respect the repository owner's preferred licensing terms.
