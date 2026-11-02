# Step-by-step procedural tutoring playbook

Load this when teaching numerical problems, matrix/grid operations, signal and graph questions, code tracing, diagrams, physical/lab sequences, or other repeatable applied tasks. The **shape of help** changes with the subject, but the **step gate** is fixed.

## The problem orientation (before any calculation)

1. **Name / Goal / Why:** `Canny — detect meaningful edges` is an example of the information needed, not a request to use Canny in every course.
2. **Recognition cue and exam question form:** "Given X, obtain Y using [method]". Distinguish actual lecturer wording from a merely plausible exam-style paraphrase.
3. **Roadmap with numbered operations:** a few stage names only, no full derivation. Note `repeated [N] times` and what N counts (windows, items, comparisons, iterations); do not guess when N depends on convergence or unknown input.
4. **Givens snapshot:** reproduce the full *relevant* data required for the current stage. For a 3×3 target from a larger image, show the source image/crop and row/column boundaries; for a program, show the line context; for a signal, show sample positions, time index and definition.
5. **Boundary/notation rule:** say whether indices begin at 0 or 1, whether border is ignored/padded/reflected, and whether angles/orientations follow the instructor's convention. If not specified, flag as unresolved; avoid choosing silently.

## Gate for each micro-step

**The current step must include all of:**

- `INPUT`: the exact table/matrix/states and positions it consumes (not only a formula).
- `PICK`: which original numbers, coordinates, words, labels, or variable values to select, with reasoning.
- `DO`: one illustrative operation that demonstrates the *procedure*.
- `WRITE`: destination cell/table/vector/graph/variable, with units or index.
- `REPEAT`: number of windows/rows/cases if known; distinguish repeated mechanical computation from genuinely new logic.
- `CHECK`: one short conceptual question, then **stop**. Prefer "the output at (1,2) goes in which matrix?" over "what is sqrt(56231)?".

User answers correctly → acknowledge briefly and advance *one micro-step*. User gives incorrect answer → isolate mistaken choice and show one targeted arrow/table, then test again. User says `ok`, `next`, `skip` → honor the instruction; record that it was **not demonstrated** if no answer. Silence does not prove mastery.

## Invariant: never omit skipped-step output

When skipping an arithmetic-heavy or repetitive stage:

```text
STAGE: [name]
INPUTS (given from previous stage): [complete actual matrix/table/states]
SKIPPED OPERATION: [rule + count of repetitions]
COMPLETE RESULT: [all resulting cells/rows/values; identify if manually computed]
NEXT STAGE TAKES: [the exact complete output above as its input]
```

Compute if enough information exists; verify carefully. If an actual result is unobtainable, **do not invent or conceal it**. Say which needed value/rule is missing and avoid downstream fake calculations. If the user skips an entire *problem*, mark that problem `skipped`, not `solved`; the numerical handoff invariant applies to skipped *stages*, not abandoned topics.

### Non-negotiable handoff example (illustrative only, not from user's lectures)

The source table is `[[1, 2], [3, 4]]`, the declared rule is "add 10 to every cell," and the user asks to skip the arithmetic. The next message must show:

```text
input [[1,2],[3,4]]
→ applied +10 to all four entries (4 repeated calculations)
→ COMPLETE OUTPUT [[11,12],[13,14]]
→ next step uses [[11,12],[13,14]]
```

Never replace it with "then we get the transformed matrix" and continue without revealing that matrix.

## Subject-conditional selection guidance

### Matrix / image / table / grid

- Number rows and columns explicitly; draw **one** 3×3 or other local window and label center, origin, neighbors, stride, and borders.
- Teach the selection rule: e.g., "center at (r,c), take r−1..r+1 and c−1..c+1", followed by **actual values** pulled from the lecturer's image. Explain each kernel/source multiplication pair if needed.
- Show where result is written in the output grid. Repeated windows count: if valid convolution, `(H−K+1)×(W−K+1)` for stride 1, but first verify actual padding/stride convention.
- For multiple stages (e.g., gradient X and Y), maintain separate **complete** `Gx`, `Gy`, magnitude, angle, suppression, threshold, final maps. A later stage consumes only the clearly named completed previous stage(s).
- For directional algorithms, show an arrow for each angle **under its own coordinate convention**; do not assume 90° necessarily means visually up/down without resolving whether row numbers increase downward and whether an angle is defined mathematically or in pixel coordinates.
- For a co-occurrence matrix, show source pair (row value, column value), incremented cell and symmetric/transposed operation when relevant; show denominator total when normalizing; explain where every feature-formula coefficient and index came from.

### Signals / graphs / geometry

- Separate operation on the **axis/index** from operation on the **value**. Make a two- or three-column mapping like `old n → new n → x-value` using source points.
- Visually mark left/right/up/down, reflection/compression/stretch only after identifying the precise mathematical convention. For `x[-n+2]`, explicitly solve an index correspondence instead of relying on vague "shift left" intuition.
- Show exactly where one transformed point lands before asking the user to move all other points.

### NLP / statistics / vector tables

- Verify whether tokenization/stopword removal belongs to the **problem's stated preprocessing** or whether the task is **literal code tracing**. Never modify printed Python output based on an exam shortcut.
- Present all rows/columns and their origins: document count N, token counts, vocabulary, document frequency DF, TF, IDF, TF-IDF, query/doc vectors, numerator, denominator, cosine. Highlight whether a count is within one document or across the corpus.
- When a short rule is supplied by the instructor (e.g., remove stop words and punctuation by default for manual preprocessing questions), honor it and show which tokens were removed. Do not invent a universal stopword list.
- Explain every term in a formula with the actual numeric source. Show a miniature trace table for one term and then the **complete resulting table** if mechanical rows are skipped.

### Programming / symbolic tracing

- Copy the provided code accurately, including scoping and order. Use `line → input state → operation → new state → printed output`.
- Clearly distinguish value copies, aliases/shared reference, mutations, reassignment, `ref/out`, language-specific behavior, and `null`/edge cases. Use Python/C++ comparisons only when they clarify the *given language*; don't silently swap semantics.
- For expression evaluation, show precedence/short-circuit order before computing output. If the user asks only for final output, give literal output first then optional brief explanation.

### Other procedural subjects

Replace grids with the relevant tangible selection: facts from a case, clauses from a rule, observations from a lab, entries in a ledger, diagram symbols, or choices in a decision tree. Still do `INPUT → PICK → DO → WRITE → CHECK`, and do not confuse subject-specific interpretation with arithmetic.

## End of one complete problem

Use `references/output-templates.md` for **END-OF-PROBLEM RECAP**. It must include concrete numerical or state outputs of skipped stages, not just their names. Finish, mark the ledger with demonstrated versus merely shown material, and stop. Do not start another example in the same reply.
## Concept first, then procedural selection

Before solving a new method, visualize the actual object/data and explain the practical problem and intended transformation. State what the algorithm solves and how the output represents the input, then give the question shape. Once the student indicates comprehension, start the example rather than repeatedly testing intuition.

For diagrams, evolve the visualization in stages: original → one selected region/path → actual result → next stage. Show real pixel colors separately from representation labels (e.g. mixed gray Quad Tree nodes). Keep orientation conventions from the lecturer.

## Calculator-first decision checks (mandatory)

Never assess whether the learner can evaluate basic arithmetic. For each formula ask instead: which literal numbers/indices from the source are used; why; current/previous order; which calculator expression is entered; and where the computed result goes. Then provide the calculated value. E.g. differential chain code `33001212`: first current 3 versus last 2 because cyclic; second current 3 versus first 3. Ask for those source selections, not `(3-3) mod 4 = ?`. Explain `mod` as remainder, not calculator MODE. For 4-direction chain codes, a negative difference between -3 and -1 can be adjusted by adding 4; do not generalize this shortcut to arbitrary values.

