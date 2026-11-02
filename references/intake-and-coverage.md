# Source audit and coverage ledger

Load this reference when the user provides one or many lectures, sheets, slide decks, course PDFs, handwritten images, source code, instructor hints, or past papers.

## Evidence policy

**Priority:** (1) user's instructor/exam-specific instructions; (2) directly visible original lecture examples and their worked steps; (3) other supplied material; (4) clearly labeled general explanatory background. An instruction about *exam conventions* can override a textbook convention (e.g., whether to omit stop words in *preprocessing problems*), but it **does not change literal code output** unless the code itself does that. Do not silently apply a method from another course.

- Identify every file/sheet/lecture and actual accessible range. Detect source-based slide numbering versus PDF page numbering (e.g., `Lecture 3, printed slide 37 / PDF page 38`) and label if different.
- Inspect **images where necessary**; text-only extraction often omits matrix grids, side annotations, plotted arrows, equations, screenshots, highlighted answers, or a worked problem rendered as a picture. If images cannot be viewed, note the coverage gap, rather than treating blank extracted text as a blank page.
- Count a **problem type** only when a concrete repeatable approach exists, and count **instances** separately. Example: three lecture-solved Sobel windows may be one *type* with three *instances*. A single lecture may contain several types. Avoid claiming "7 problems" if you actually found 7 mentions of the same example.
- For each example, capture the **actual original question/givens**, expected output, intermediate data when shown, worked/unsolved status, page, instructor conventions, repetitions, and hidden edge cases (padding, border handling, orientation, indexing, special cases).
- Preserve negative signs, decimal points, row/column ordering, units, angle conventions, diagrams, code indentation, and text exactly where they affect results.
- Verify a numerical worked solution with available methods where feasible; flag slide arithmetic/logic inconsistency as `LECTURE OUTPUT` versus `RECOMPUTED OUTPUT`, and distinguish which stream subsequent lecturer steps depend on. Never silently replace either.
- Past exam questions and sheets may be evidence of *actual wording or emphasis*, but do not guarantee future exam coverage. User hints ("Canny L3 p37", etc.) are **pointers, not proof**; verify the page when possible.

## Classify by what the student must do

| Tag | What qualifies | Teaching form |
| --- | --- | --- |
| `P: calculation` | Algebra, signal transforms, image matrices, TF-IDF, probability, any multistage formula. | Choose exact numbers/locations → operate → write output. |
| `P: algorithm/diagram` | Region growing, graph traversal, finite-state diagrams, circuit flows, logical decisions. | Spatial or state-transition walkthrough + arrows/coordinates. |
| `P: code trace` | Predict console output/state, pointer/reference changes, regex matching, code execution reasoning. | Literal line-by-line state table + exact output. |
| `P: applied/protocol` | Lab, systematic classification, diagnosis, case analysis, stepwise written procedure. | Decision/sequence table + what triggers the next step. |
| `T` | Define, compare, explain, list, why/when, limitations, examples and theory diagrams. | English exam-ready answer + Arabic link + comparison as needed. |
| `H` | Embedded theory required for a procedural problem. | Explain just-in-time; keep unasked theory in `T` ledger. |

A course can be `T`-only, `P`-only, or mixed. Never force numeric calculations into a nonnumeric subject.

## Coverage ledger structure

Store or maintain one row per relevant **distinct problem type** and a second row/ledger per **theory question/cluster**. Recommended representation:

```text
COURSE: [title]
SOURCES: [files / page ranges / unreadable areas]
PROCEDURES:
ID | Problem type | Origin and slide/page | Instances: worked/unsolved | Exam cue | Inputs/outputs | Special cases | Status
P1 | [actual type] | [Lx pY] | [2 worked, 1 exercise] | [cue] | [matrix → scalar] | [border] | not started
THEORY:
ID | Topic/question family | Origin | Attached to P? | Missing subquestions | Status
T1 | [actual concept] | [Lx pY] | P1 / standalone | [compare/why] | not started
UNCERTAINTIES: [source gaps, question wording, slide error, not-provided examples]
NEXT: [precise ID + micro-step]
```

When the ledger is long, show the user a **short readable map** (number of types, titles, source pages, theory groups, order); maintain detailed underlying rows so no topics are discarded. If the platform cannot persist the ledger across conversations, provide a **copyable session handoff** at user request. Do not imply permanent memory of all attachments.

## Starting after the audit

Use the introductory phrasing (paraphrase naturally): "لقيت في المحاضرات [N verified] أنواع مسائل: [names + pages]، والنظري متقسم إلى [topics]. هنحل اللي الدكاترة شارحين خطواته الأول، وبعدها نرجع للنظري اللي ما اتغطّاش."

Then, unless the user asked only for an overview, go directly to **P1: question shape, recognition clue, roadmap, first input-location action, one checkpoint**. If there are no problems, start **T1**. Never force a needless yes/no question about starting.

## Partial/ambiguous inputs

- Missing materials: provide a provisional high-level map and ask for the lectures when a source-specific audit is required; avoid fabricated count/pages.
- Some files missing: audit available files fully and label count *partial*.
- Pages visually unreadable: identify exactly which page/step is illegible; ask for that screenshot only if necessary.
- Unsolved teacher exercises: can work them with the instructor's method if supported; label `lecture exercise (not lecturer-solved)`. Do not invent sample values to force a solution.
- Special lecturer rule confirmed by the user: record it explicitly in the relevant topic ledger and use it **only in its proper task context**.