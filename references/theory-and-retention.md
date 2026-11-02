# Theory, recall, and exam-ready wording

Load this when the user wants theoretical lectures, questions, comparisons, definitions, explanations, quizzes, links for remembering, or a theory cheat sheet. The user wants an answer **short enough to reproduce in an exam** but **long enough to express the meaning**, not one-word definitions.

## First: exhaustive but honest question discovery

From every available lecture and sheet, collect:

- Definitions and what a component does; its input/output.
- Why a method is used, when it is chosen, its assumptions, drawbacks, and special cases.
- Comparisons among nearly synonymous concepts (especially same-word-root terms), levels of abstraction, stages, application examples and diagrams.
- Instructor review questions, end-of-slide questions, question stems, and theory that accompanies numerical solutions.
- Theories mentioned only once or in captions, if included in the taught material; do not ignore them because the larger topic had a worked example.

Mark source/slide and whether the subject is `covered through P`, `partially covered`, or `standalone T`. Embedded theory coverage does **not** mean all related theoretical questions are answered. When exact sheet questions exist, preserve the question's meaning and ordering; don't swap in generic internet FAQs.

## Teach a short conceptual unit, not a word salad

Default unit:

```text
Q (English): [Actual question or clearly labeled exam-style question]
A (English): [A complete accurate ONE-SENTENCE answer; two if necessary.]
Remember: [a short English keyword]
لينك بالمصري: [one understandable causal / visual / everyday association]
Different from [confusable term]: [the one meaningful distinction]
Source: [lecture + page, if verified]
```

**Avoid:** `Word sense = meaning`; `Morphology = words`; or an Arabic link that merely translates an English word. **Prefer:** say what the concept operates on, what it changes/identifies, and its defining difference. Example of **format only** (not claimed to appear in the user's lecture):

```text
Q: What is tokenization?
A: Tokenization splits text into smaller units, such as words or subwords, so the text can be processed.
Remember: split
لينك بالمصري: بنفك الجملة قطع قبل ما الكمبيوتر يحسب أي حاجة عليها.
Different from normalization: tokenization decides the boundaries; normalization changes the form of a token.
```

For a comparative exam question, use symmetric phrasing so the difference is visible:

```text
Q: Compare A and B.
A: A [input/operation/result], whereas B [input/operation/result].
Remember: A = [distinctive cue]; B = [distinctive cue].
لينك بالمصري: [an image that makes the contrast unavoidable].
```

When two categories differ by **scope** (single document vs whole collection), **stage** (before vs after), **representation** (value vs index), or **goal** (detect vs classify), explicitly state that dimension. Answers must not overclaim simplifications to the point of being wrong.

## Theory types and response forms

| Kind | Best short structure |
| --- | --- |
| `Define` | "X is [what it is] that [does X] to [input] for [purpose]." |
| `Why` | "X is used because [mechanism] which [benefit]." |
| `When/use` | "Use X when [condition], because [reason]." |
| `Compare` | "A [property/operation], while B [same dimension contrasting]." |
| `Advantage/limitation` | One benefit and one precise limitation, with context. |
| `Steps` | Numbered verbs with one purpose line each, not bare labels. |
| `Draw/label` | Minimal source-consistent diagram plus explanation of each important arrow/part. |
| `Identify/explain code` | Retain literal syntax and language output; don't apply unrelated preprocessing shortcuts. |

## Retention strategy: repeated *retrieval*, not repeated paragraphs

1. **First exposure:** English sentence + key word + short Arabic link; anchor in an existing example if available.
2. **Quick check after a small cluster (about 2–4 items):** ask to distinguish two concepts or name which one fits a scenario. One question at a time.
3. **Later in same subject:** revisit common confusions in a compact comparison table, without re-explaining every definition.
4. **Final cheat sheet:** reuse the *same* short keyword and the same conceptual contrast so the user can mentally recover the complete English sentence.
5. **For review errors:** ask a better distinguishing question; don't answer "wrong" and dump a textbook chapter.

If the user explicitly requests the **entire** theoretical sheet and every question at once, provide it (grouped by lecture/theme), without making interactive checkpoints a blocker. The one-step rule is for **live tutoring**, not for an explicitly requested compiled study artifact.

## Working around attention and exam constraints

- The user finds the **start of a second long problem** harder than the arithmetic of the second problem. At transitions, show a 2-line bridge, a concrete first input, and *one tiny action*, not a 15-paragraph explanation.
- For tired or distracted moments, ask one **successfully answerable** index/selection question. Once engaged, return to normal difficulty.
- Use bite-size targets tied to a real course task; do not prescribe unsupported clinical explanations for attention.
- When the user states a specific exam duration, aim for a short workable written answer format; do not promise any question will definitely appear.
- Stick to lecture terminology and the user's English technical vocabulary; avoid gratuitous formal Arabic translations.

## Exam revision synthesis

Produce two distinct products when requested:

**Problem cues:** a compact decision tree — `If question asks ... → select method ... → inputs ... → next outputs ... → tricky boundary / repeated step ...`.

**Theory cues:** full lecturer question coverage — `English Q | one-sentence English A | memory keyword | short Arabic link | compare / exception | source`.

In both, add an `easy-to-confuse` section based on *actual* misunderstandings/questions observed in the session, not arbitrary generic trivia. The cheat sheet should be usable even after the detailed explanations are forgotten.