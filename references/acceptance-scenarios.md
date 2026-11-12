# Acceptance scenarios for manual quality review

Use these adversarial scenarios to test a future version of the study tutor. They are behavior checks, not lecturer examples. This file is optional at runtime; load when validating/maintaining the skill or when correcting failures.

1. **Many lectures, hints incomplete** — User uploads 4 mixed lectures and says "the GLCM problem is slide 59". Expected: inspect all 4, verify slide hint when possible, inventory every distinct problem type and standalone theory, then teach first instructor-worked problem. Never list only GLCM just because user mentioned it.
2. **No hint at all** — User uploads lecture bundle and says "ذاكرني". Expected: discover problems, code tracing, theoretical questions, lecture page references, edge cases, status; don't ask user to name the algorithms when files can supply that information.
3. **Only theory** — User uploads history or biology readings without numerical examples. Expected: do not fabricate numeric exercises; map theory questions, comparison prompts, diagrams or procedures where genuinely relevant; teach short English exam sentences and Arabic memory links.
4. **Skip computations in a matrix** — Current input `[[1,2],[3,4]]`, instructed +10 per element; user says "skip". Expected complete next matrix `[[11,12],[13,14]]`, label 4 operations and feed next stage that actual matrix. Not just a formula, nor a partial first-row output.
5. **Skip an entire problem** — User says "المسألة دي مش مهمة، نروح للي بعدها". Expected: mark entire problem skipped, move to next source-backed type, not pretend it is completed or compute every intermediate stage unnecessarily.
6. **Code tracing exception** — Lecturer said to remove stopwords in manual NLP word-count problems; user asks output of given Python script containing literal stopwords. Expected: preserve literal Python output; don't remove words outside stated preprocessing.
7. **Misleading slide answer** — Slide has an arithmetic inconsistency in step 2, subsequent steps use its wrong value. Expected: label original and recomputed values; distinguish instructor downstream stream, choose an explicit path; do not silently swap or mix them.
8. **Checkpoint issue** — User doesn't answer a selection question and says "ok". Expected: proceed on permission but status is not `demonstrated`.
9. **New course, no matrices** — User supplies a legal studies exam with case analyses, comparisons, essay prompts. Expected: identify applicable decision procedures and theory, teach procedural evidence selection using `INPUT→PICK→DO→WRITE` and concise definitions; no equations imposed.
10. **Second difficult problem fatigue** — First numerical problem ends and user says "اللي بعده". Expected: recap for previous problem has already been shown, next begins with only name + tiny roadmap + first input and one easy selection action, not another long overview.
11. **Question about GLCM 90 degrees** — Expected: ask/inspect image row-axis and orientation definition or explain both conventions; don't insist an angle means down without checking source conventions.
12. **Cheat sheet, after lessons** — User wants final quick review. Expected: include question-recognition cues, complete final table shapes and provenance, all theory Q&A in complete English sentences, Arabic one-line memory links, lecturer-specific exceptions, and remaining gaps; not math formulas alone.
13. **Continuing a step with missing previous output** — The prior reply skipped GY arithmetic without a GY matrix, and user says "next". Expected: recover/compute and present the **full GY output** first, then begin the next stage; don't proceed as though the missing output existed.
14. **Visual scan gap** — A PDF page has a worked matrix embedded as an image while text extraction yields only the title. Expected: examine visual rendering or flag unverified; don't claim no solved problems on that page.

15. **No arithmetic quizzes:** For `(3-3) mod 4`, ask the origin and ordering of the two 3s and the calculator expression, not its value; provide the result.
16. **Algorithm without problem context:** On new Chain Code topic, explain binary object boundary representation and why relative steps replace coordinates, visually, before numeric direction codes.
17. **Progressive Quad Tree:** Show black/white source pixels, first split, mixed gray nodes, successive subdivisions, tree at each level. Gray denotes mixed region, not source pixel color.
18. **Circular shift misunderstanding:** Learner shifts a leading pair rather than one character. Explain one character per operation and distinguish first rotation from final normalized minimum.
19. **Calculator mod misconception:** Clearly distinguish MODE settings from mod remainder; provide a safe numeric entry method, never an arithmetic quiz, and device-specific keys only after model identification.
20. **Public GitHub sync:** Update generic teaching instructions in the same session when asked and when GitHub permits; report commit, avoid sensitive memory disclosure and any promise of unattended automatic updates.

21. **Untaught position inference:** Tutor demonstrates only the special first pair (first minus last) in differential chain code and asks for the second pair. Expected: FAIL; tutor must first explain regular rule `position k − position (k−1)`, demonstrate a second-pair example, then test analogous third or later positions.
22. **Visual step navigation:** Learner requests animation in chat for `33001212`. Expected embedded interactive App Block if available: original indexed code, highlighted current/previous, equation, partial output, working Play/Pause/Next/Previous, incremental eight steps; clearly specified static fallback if unavailable.
23. **Quad Tree animation:** Show original black/white cells, animate uniform-vs-mixed classification, split only mixed nodes recursively and grow child tree layer-by-layer; distinguish mixed gray node from actual gray source pixel.
24. **Calculator competence:** Do not quiz `(3−3) mod 4` result. Ask which original positions supply the two operands and how to type expression, but only after teaching and demonstrating that precise position-selection rule.


## Codebase Story Mode — additional behavior tests (not real company data)

11. **First encounter with a codebase** — User asks "اشرحلي الـ approach من غير technical" while project files are available. Expected: inspect relevant entrypoints and actual call chain, state problem first, explain decisions and outputs, cite real modules, no syntax tutorial or quiz.
12. **Huge file, multiple responsibilities** — Expected: locate verified callers/callees and group coherent responsibilities by their place in the feature, not in file line order. Distinguish work performed locally from delegated work.
13. **Partial repository visibility** — Expected: clearly label what was inspected and unknown, do not invent class names, LLM models, prompt content, metrics or business logic, and ask for the minimal missing source only if it prevents progress.
14. **LLM vs retrieval vs clustering ambiguity** — Expected: distinguish classification, clustering, retrieval and ranking accurately and avoid claiming a particular method before confirming it in code.
15. **AI-generated implementation** — Expected: one or two relevant design/test risks and verification steps, distinguish confirmed bug from speculative risk, no fabricated test results.
16. **Technical follow-up** — User says "طيب وريني technical" after conceptual story. Expected: explain only the chosen path in implementation detail without starting the feature overview over.
17. **Company workspace boundary** — Expected: read authorized workspace code only, no external uploads/copying proprietary data or automatic edits for explanation.
18. **Existing study behavior preserved** — User uploads lecturer worksheet with code tracing; expected: activate exam-study rules and retain lecturer-grounded literal code tracing, not the workplace codebase story.
19. **Compressed quantitative claim** — The code has a recent-time window, top-N cap, ordering score and minimum-count guard. Expected: explain the trigger, source, metric/unit, eligibility, before/after toy ordering, at-most vs exactly N, guard count semantics, negative path and next consumer; no magical numbers.
20. **Magic constant with undocumented rationale** — Expected: report confirmed value/behavior and describe reasons only as explicitly labeled hypotheses, not undocumented design history.
21. **Stage disconnected from previous stage** — Expected: explicitly say what intermediate representation exists, the unresolved next problem, why it needs the previous output, and where the next consumer is verified.
22. **No concrete example** — Response only says "group related items" or "improve quality". Expected: realistic representative input -> decision -> transformed output and at least one exclusion/change with explanation.
23. **Conceptual detail vs syntax** — User says "مفصل أكتر" after a short summary. Expected: longer causal logic with terms and numbers unpacked, NOT a function-by-function explanation, unless syntax is requested.
24. **Suspicious confident threshold explanation** — Expected: investigate config/guards/tests and distinguish configured effect from inferred motivation; never claim why a historical threshold was chosen without evidence.
25. **Excessively long feature** — Expected: maintain complete section-by-section explanation without losing overall coverage or cutting a filter stage in half; if constrained, state the exact remaining sections rather than falsely claiming complete coverage.
26. **Anticipated questions** — First-time engineer would ask "from where/how/what if". Expected: proactively answer relevant questions inside the explanation; no forced quiz or unexplained terms.
27. **Beginner restarts, not a longer technical summary** — User says "مش فاهم". Expected: restart from one everyday scenario and the first record's shape, not another function/service overview.
28. **Missing dataset picture** — User requests actual data structure. Expected: inspect authorized read-only live samples when available or schema/tests and show privacy-safe examples; explicitly distinguish genuine retrieved sample vs fictional values and never claim access without it.
29. **Terminology before world model** — Expected: introduce domain/project/worker/freshness only after explaining what the business object does with a visible example; exact useful names in English, natural Arabic explanation.
30. **Two-run schedule vs per-item processing** — Expected: show two records across real or marked example dates and clearly explain a scheduled check and a separate eligibility rule.
31. **Unnecessary timezone tangent** — Expected: don't introduce "if timezone changes" unless the verified implementation or user question needs it; don't invent configured timezone.
32. **Example continuity** — Expected: one same item from opening to outcome with before/after states and one contrast for failure/exclusion.
33. **Jargon despite request for simplicity** — Expected: coherent Egyptian colloquial paragraphs, not a technical report, code syntax or section-per-function list.
