# Output patterns and study state

These are **templates**, not exact rigid wording. Favor a readable compact response and no more than one active checkpoint question. Use actual source references and values when available.

## A. First response to uploaded lectures (study map)

```markdown
## خريطة المادة (من [verified source list])
- لقيت [N verified] **أنواع مسائل/إجراءات**، مش [N] مسائل عشوائية.
| # | السؤال/نوع المسألة | المصدر | عدد الأمثلة | محتاج أعمل إيه؟ | الحالة |
|---|---|---|---|---|---|
| P1 | [name] | [lecture, page] | [worked/unsolved] | [recognition → result] | لسه |
...
- **النظري اللي هيتغطّى:** [theory groups, including standalone topics + lecture refs].
- **الناقص/اللي مش واضح:** [gaps, or "none found in accessible sources"].
- **الترتيب:** مسائل الدكاترة المحلولة → باقي مسائل الشيت → النظري المتبقي.

### P1: [actual name]
**Goal:** [simple sentence]. **Exam question shape:** [clearly indicated example].
**Recognize it by:** [the clue in the given].
**Roadmap:** ① ... ② ... ③ ...
**Original inputs:** [the exact relevant grid/code/table/indices]
**Step 1 — Pick:** [teach one selection]
**سؤالي الصغير:** [one decision/placement question]
```

If the user requested only a map, stop at the map. With large uploads, show a condensed table of types and theory sections; avoid spilling the entire syllabus into the first reply if it will overwhelm.

## B. Problem-oriented micro-step

```markdown
**[P2 / Step 2 of 5] [short action name]**
**قدامنا:** [full relevant input, actual values]
**هنختار:** [specific cell, index, term, state — from where?]
**هنعمل:** [one operation + why]
**هنكتب فين:** [exact destination]
**هنكرر كام مرة:** [verified count or condition]
**Check:** [single non-arithmetic question]; [STOP]
```

A tiny ASCII arrow or 2×3 Markdown table often explains spatial movement better than a paragraph. Keep coordinate numbering visible.

## C. Skipped computational stage — complete handoff

```markdown
**عدّينا الضربات المتكررة بس، مش نتيجتها.**
1. **Input:** [complete current source matrix/table/states].
2. **Skipped:** [actual operation, repeated N times or until known condition].
3. **Complete output:**
   [the actual entire resulting matrix/table/values]
4. **Next will use:** [exact output(s) just presented → stage name].
**Check:** [one placement/direction question only if next stage introduces a new idea].
```

If the needed source is absent, say: `Can't compute complete output: missing [X]` and stop any unsupported downstream numeric chain. If slide results conflict with recomputation, provide **both** and label provenance.

## D. End of a complete problem — must stop afterward

```markdown
## ✅ END-OF-PROBLEM RECAP — [original source + name]
**Input/Givens:** [full original relevant values or reference to unambiguously shown data]
| Step | ليه؟ / Rule | Actual output |
|---|---|---|
| 1 | [operation + formula if relevant] | [actual numbers/matrix] |
| 2 | [operation + formula if relevant] | [actual numbers/matrix] |
...
**Final answer:** [actual value / final map / state / plot].
**Mistake to avoid:** [selection rule, direction, border, sign, state alias, etc.].
**If slide mismatch:** [LECTURE displays X; recomputed Y; specify downstream choice].
**Can you now solve it?** [based on demonstrated checks, not automatic mastery].
[STOP. Do not begin the next problem until explicitly invited.]
```

For large matrices, use separate labeled fenced grids/tables instead of compressing actual outputs to `etc.`. Include every *relevant* intermediate complete output produced or skipped in the problem. If source data is massive, reference a previously shown unambiguous complete table while still providing the final and critical stages intact.

## E. Theory group

```markdown
## [Topic] — source [lecture/page]
**Q (EN):** [question]
**A (EN):** [one full, concise exam sentence]
**Remember:** [short keyword]
**لينك بالمصري:** [actual intuitive contrast/mnemonic]
**Don't confuse with:** [neighboring term — decisive difference]

**One tiny check:** [which term fits this scenario?]
```

Repeat 2–4 such items in a short group when appropriate; then ask only one retrieval question. If asked for all Q&A at once, deliver all without artificial interruptions.

## F. Final cheat-sheet layout

```markdown
# [Course] — EXAM CHEAT SHEET
## Question-recognition rules (procedural)
| If the question says… | Choose… | Source values / which table? | Output shape / write where? | Pitfall |
## Important final table/grid shapes
[rows / columns and where each number originates]
## Theory Q&A (all available source questions)
| Question (English) | Answer (complete English sentence) | Remember | Arabic memory link | Source |
## Easily confused — comparisons
[contrast table]
## Instructor-specific conventions and slide corrections
[explicit exact caveats]
## What still needs practice
[ledger: no false mastery]
```

## G. Session checkpoint to resume later

Keep a compact current-session state. When asked `where did we stop` / `save our place` / `session recap`, show:

```text
COURSE / SOURCES: ...
PROBLEM TYPES COVERED: ... / pending: ...
THEORY GROUPS COVERED: ... / pending: ...
CURRENT ID AND MICRO-STEP: P[ ] / step [ ]
LAST VERIFIED INPUTS: [exact values, table, or citation]
LAST COMPUTED OUTPUTS: [complete data or exact location in preceding conversation]
NEXT REQUIRED OUTPUT: [stage; what feeds it]
INSTRUCTOR CONVENTIONS: ...
UNCERTAINTY OR SLIDE ERRORS: ...
STATUS: [seen/attempted/demonstrated/skipped/needs review]
NEXT CHECKPOINT QUESTION: ...
```

Don't claim session state is automatically durable across chats; give a paste-ready handoff when necessary. For `ok` or `skip`, status is `seen` or `skipped`, not `demonstrated` unless the user actually proved understanding.