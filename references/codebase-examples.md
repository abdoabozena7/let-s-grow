# Codebase Story Mode — style and acceptance examples

These are **invented teaching scenarios**, not documentation of a real company, repository or codebase. Replace illustrative details with verified code facts, or state that the repository could not be inspected.

## A. Categorizing a very large collection of AI-related events/pages

**User:** "لسه داخل على جزء بيحاول ينظم آلاف الـ pages/categories؛ مش عايز syntax، عايز أفهم الـ approach والملفات بتتقسم ليه."

**Good explanation when code is NOT available:**

> بص، المشكلة هنا مش بالضرورة إننا مش عارفين نجيب الداتا؛ ممكن نكون بنجيب حاجات كتير جدًا، بس بالـ raw form صعب حد يطلع منها معنى. فإحنا محتاجين نحول العناصر المتناثرة لمجموعات مفهومة نقدر نحللها. كفكرة تصميم، ممكن نمشي من استقبال الـ item، لتجهيزه في شكل consistent، لتحديد معناه، وبعدها نربط الـ labels أو المجموعات بنتيجة مفيدة للمنتج.
>
> فيه فرق لازم ناخد بالنا منه: `classification` بيختار label من مجموعة معرّفة؛ `clustering` بيكتشف مجموعات من التشابه؛ `retrieval` بيرجع candidates، و`ranking` بيرتبهم. ممكن الحل الحقيقي يستخدم واحد أو أكتر، لكن **مش هقدر أجزم بمين مستخدم عندكم قبل ما أقرأ الكود**.
>
> أول ما نشوف الملفات هنوصل أربع قرارات: الداتا جاية منين، بتتحول لإيه، مين بيقرر الفئة أو الترتيب، والنتيجة بتتخزن/بتظهر فين. بعدين نربط كل قرار بمسؤولية verified من الملفات، مش نقرأ folder tree وخلاص.

If source is accessible, replace hypotheticals with **actual** entrypoints, categorization mechanism (LLM prompt vs embedding similarity vs static mapping vs clustering), postprocessing, confidence interpretation, tests and persistence. No invented metrics or paths.

**Bad:** "الكود فيه KMeans وLLM وEmbeddings و`CategoryService.cs`" without proof or a causal explanation.

## B. ASP.NET endpoint, Service and Repository

**User:** "أنا لسه جديد في .NET. لو كنت بصمم الـ feature دي من الصفر هفكر إزاي؟"

**Good explanation, assuming the actual code confirms the shape:**

> عندنا user بيطلب يغيّر حاجة. الموضوع مش مجرد تعديل field؛ محتاجين نفهم الطلب، نتأكد إنه valid ومسموح، نطبّق business rule، وبعدها نحفظ التغيير ونرجع نتيجة مفهومة. عشان كده توزيع المسؤوليات بيساعد: الـ endpoint بيستقبل ويعرض الـ request، الـ service بياخد قرار الـ business، والـ repository بيتعامل مع التخزين. بس مهم نتأكد من الكود مين بينفذ validation والauthorization فعلًا.
>
> الرحلة: user action → request → checks → domain decision → database → response. هنربط ده بالـ real files اللي بتعمل كل خطوة، وبعدين نقرر نحتاج technical details فين. أول AI-review question: هل الـ response بيتقال عليه success قبل ما الـ write تتم؟ ده احتمال للفحص، مش bug أثبتناه.

**Bad:** Start with teaching `async`, `Task<IActionResult>`, `DI` or `DbContext` syntax before explaining the feature.

## C. A huge file with many helpers

**User:** "الملف ده كبير؛ عايز أعرف هو مسؤول عن إيه والapproach اللي وراه."

**Good:** First place it in the verified feature. Identify 2–5 coherent responsibilities (e.g., choosing records, normalizing, deciding, dispatching). Show input/output and why each exists. Map known callers, dependencies, and downstream results. Distinguish "this file owns X" from "this file delegates X." Offer one real decision to zoom into.

**Bad:** 200-line summary or function-by-function inventory without a problem story; claim a single file represents the entire feature when code shows otherwise.

## D. Technical on explicit request

**User:** "تمام، دلوقتي technical اشرح الجزء اللي بيختار label."

**Good:** Focus on the *real* label-selection function/path only. Show actual input contract, decision branches, fallbacks, model or provider call, returned shape, where the output is consumed, and a targeted test or trace. Explain unfamiliar language features just in time. Do not restart the full feature story or add an exam quiz.

## E. AI-assisted code review

**User:** "الـ AI ممكن يكون عامل إيه غلط هنا؟"

**Good:** Start with implemented behavior confirmed in code. Identify 1–3 plausible failure modes specifically tied to observed contracts or data flow, mark each `confirmed` or `to verify`, and give an inspection/test that would settle the question. Never invent a passing test, real bug, or a framework method.
