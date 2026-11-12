# Install Study My Way in GitHub Copilot / VS Code

This is the **same original portable study skill**, now with an additional **Codebase Story Mode** for architecture-first understanding of real workplace code. The repository contains generic instructions only; **no company source code or proprietary data**.

## Recommended: personal agent skill (keeps company repositories unchanged)

1. Download the GitHub repository ZIP (Code → Download ZIP), or clone it locally.
2. The **root of this repository** already has `SKILL.md`, `references/`, and `agents/`. Put these contents together inside `study-my-way`, directly under:
   - Windows: `%USERPROFILE%\.copilot\skills\study-my-way\SKILL.md`
   - macOS/Linux: `~/.copilot/skills/study-my-way/SKILL.md`
3. Quick clone on **Windows PowerShell** (when folder does not already exist):
   ```powershell
   New-Item -ItemType Directory -Force -Path "$HOME\.copilot\skills" | Out-Null
   git clone https://github.com/abdoabozena7/let-s-grow.git "$HOME\.copilot\skills\study-my-way"
   ```
4. Open your approved company workspace in VS Code and use GitHub Copilot **Agent Mode**. Open the Command Palette and `Chat: Open Customizations` to inspect Skills; if listed, invoke `/study-my-way`.
5. Automatic selection is not guaranteed: if necessary, use the explicit slash command and ask for a *codebase story*. Company/enterprise policy can restrict skills or agent access; don't bypass those rules.

## Copyable first prompts

**First look at a feature:**

> /study-my-way أنا أول مرة أدخل الـfeature دي. اقرأ الكود المتاح ليك في الـworkspace وابدأ بالقصة بالمصري: المشكلة اللي بنحلها، الـapproach والقرارات اللي وراه، رحلة input → decision → output، وبعدها وزّع الخطوات على الملفات الحقيقية ومين بينادي مين. مثال صغير، من غير syntax أو line-by-line. افصل confirmed عن inference، وماتغيّرش أي ملفات.

**Opened a large file:**

> /study-my-way اشرحلي الملف المفتوح من وجهة نظر المشكلة اللي بيحلها والـapproach. حدد مسؤولياته، الـinput/output لكل جزء، ومكانه بين الـcallers والـconsumers اللي اتأكدت منهم. بلاش قائمة functions أو شرح C# syntax دلوقتي.

**Go technical after understanding the story:**

> /study-my-way تمام، دلوقتي technical deep dive في الجزء اللي بيحدد النتيجة، بالـverified code paths والـbranches والفشل المحتمل. ما تعيدش overview من الأول.

**AI-first review:**

> /study-my-way بعد ما توضح الـapproach، إيه اللي الـAI-generated implementation ممكن يكون ناسيه؟ فرق بين bug مثبت وrisk محتاج اختبار، ووريني طريقة التحقق من الـworkspace من غير edits.

**Follow up when Copilot skips reasoning (paste into the same chat):**

> /study-my-way شرحك لسه مختصر وفيه logical jumps. راجع اللي قلته والـcode اللي بتستند عليه، وابدأ القصة تاني بالتفصيل المفهومي، مش technical syntax. لكل مرحلة عرّف المدخلات جاية منين، المصطلحات معناها إيه، اعمل مثال قبل/بعد واضح، فك كل رقم أو threshold (قيمته، بيتحسب على إيه، ليه، وإيه اللي بيحصل لو الشرط فشل)، وبعدين وضّح الناتج بيروح فين وليه المرحلة اللي بعدها محتاجاه. ما تسيبنيش أسأل "منين؟/ليه؟/إزاي؟/وبعد كده؟" عن حاجة موجودة في الكود. لو سبب قرار غير موثّق قوله كـ hypothesis، وما تخترعش حقائق. خليك بتشرح بالمصري بطريقة متصلة، من غير quizzes أو edits، ومتختصرش التفاصيل عشان توفر مساحة.

**To restart from zero without jargon (same chat):**

> /study-my-way ابدأ من أول وجديد بطريقة أبسط: احكيلي قصة عنصر واحد واضح من العالم الحقيقي قبل أي مصطلحات تقنية. وريني شكله في الداتا بحقول اتأكدت منها من الـmodels أو source متاح read-only. لو القيم افتراضية وضّح ده؛ ولو مالكش access للداتا الحقيقية ما تدعيش عكس كده. امشي بنفس المثال من البداية للنهاية مع قبل/بعد كل قرار. وريني واحد الشرط بيقبله وواحد بيرفضه، وفرق بين معاد الفحص وقرار تحديث العنصر. عرف الـdomain/project/worker بس لما نحتاجهم، وخلي أسماء المصطلحات بالإنجليزي. احكي بالمصري في فقرات طبيعية مترابطة؛ من غير functions/syntax أو database/infrastructure details الأول، وماتغيّرش أي داتا أو ملفات.

## Company privacy and scope

The skill is generic and does not grant new access. Copilot can only see files allowed by your existing company setup. Don't paste private code into personal external chats or public repos; explanations should remain inside the approved workspace. For simple explanations, stay read-only.

## Documentation

- https://code.visualstudio.com/docs/agent-customization/agent-skills
- https://docs.github.com/en/copilot/concepts/customizations/agent-skills
