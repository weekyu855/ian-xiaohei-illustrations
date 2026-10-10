# 一次性六格画布提示词模板

将方括号替换为文章分析结果。必须整段一次性提交给图像生成模型。

```text
Create ONE complete editorial illustration contact sheet in a SINGLE image-generation call. The canvas must contain exactly SIX distinct panels, arranged as a clean 3-column by 2-row grid. This is one unified canvas, not six separate image files.

REFERENCE IMAGE ROLES — USE THE ATTACHED IMAGES, NOT JUST THEIR TEXT DESCRIPTIONS:
- Character reference image(s): preserve the same character identity, facial structure, hair silhouette, half-lidded eyes, stubble, hoodie, pants, sneakers, and body proportions.
- Editorial style reference image: closely follow its hand-drawn line quality, grayscale shading, white space, panel composition, visual metaphors, and restrained orange-yellow accents.
- The current article determines the new scene content only. Do not copy old scenes, text, statistics, or story beats from the reference images.
- If reference images are not actually attached to the image-generation request, do not claim they were used.

VISUAL STYLE:
Clean pure-white background; thin black hand-drawn ink outlines with slight natural wobble; grayscale pencil/marker shading; expressive but restrained sketch details; ample white space; very sparse warm orange-yellow accents only for one or two marks, gestures, or emotion lines. Match a thoughtful hand-drawn editorial illustration style: clear, slightly quirky, dry humor, not childish, not corporate vector art, not 3D, not photorealistic. Avoid beige vintage paper, heavy texture, gradients, and drop shadows.

FIXED PERSONAL IP — KEEP IDENTICAL IN ALL SIX PANELS:
The same lazy young adult man in chibi editorial illustration style: fluffy messy black medium-short hair with a side-swept fringe and a few flyaway tufts; half-lidded sleepy but calm eyes; simplified nose and mouth; subtle short stubble around the mouth and chin; oversized medium-gray hoodie with dark drawstrings; loose black pants; white sneakers with black hand-drawn outlines. Keep the same face, hairstyle, eye shape, stubble, outfit, body proportions, and shoe design in every panel. Change only pose, viewing angle, small expression, and story-relevant props. He is deadpan, relaxed, mildly skeptical, and quietly clever — not a cute mascot.

LAYOUT:
Exactly 6 panels in a 3-column x 2-row grid, with even spacing and clean white gutters. Each panel must work as a standalone crop. Keep all characters, props, handwritten notes, and visual effects entirely inside their own panel. Do not let any object cross a panel boundary. Keep safe margins inside every panel. ABSOLUTELY NO OVERALL TITLE, NO PANEL TITLES, NO PANEL NUMBERS, NO NUMBER BADGES, NO HEADER, NO LEGEND, NO explanatory paragraphs, no logo, no watermark, no decorative border around the full canvas.

PANEL 1 — HOOK / QUESTION:
[Describe scene, character action, and core idea.]

PANEL 2 — CONTEXT / CURRENT STATE:
[Describe scene, character action, and core idea.]

PANEL 3 — KEY MECHANISM:
[Describe visual metaphor, relationship, and core idea.]

PANEL 4 — CONFLICT / COST:
[Describe the tension, limitation, risk, or counterintuitive point.]

PANEL 5 — TURN / APPROACH:
[Describe the character's action, choice, or reframing.]

PANEL 6 — CONCLUSION / MEMORABLE IMAGE:
[Describe a clear visual ending that expresses the article's takeaway.]

TEXT:
TEXT BALANCE — IMPORTANT:
Use a small amount of meaningful handwritten Chinese, similar to an editorial illustration rather than a text-free comic. Place short handwritten captions in only 2 or 3 of the six panels; leave the other panels text-free. Each caption should usually be 4–12 Chinese characters and add an insight, consequence, or memorable phrase. Use natural hand lettering and, if useful, one thin orange-yellow underline. Let the character actions and visual metaphors carry most of the story.

ABSOLUTELY NO overall title, NO panel titles, NO panel numbers, NO number badges, NO header, NO legend, NO explanatory paragraphs, no logo, no watermark. Do not label all six panels. Never render tables, dense copy, gibberish, random symbols, or invented statistics.

FACTUAL ACCURACY:
Do not invent numbers, labels, causes, claims, people, or places. Preserve the article's exact meaning. Visual metaphors must not misrepresent the content.

NEGATIVE CONSTRAINTS:
Not six separate images; not a single scene spanning all panels; no extra panels; no missing panels; no character redesign; no mascot substitution; no title card; no headings; no numbering; no text-heavy infographic; no PPT infographic; no dense diagram; no unrelated accessories; no cropped-off heads, hands, feet, or key props; no objects crossing grid gutters; no watermark or signature.

Output one high-resolution image with all six panels visible and evenly laid out.
```

## 用法提醒

图像模型对复杂中文的准确度有限。每格尽量只放一个短标签；若文字必须完全准确，提示词应让模型留出空白标签区域，后续再排版。为了节省额度，默认只调用一次生图，不要为了小瑕疵自动追加第二次生成。
