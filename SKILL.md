---
name: heytea-naive-poster
description: 生成「喜茶风 · 稚拙」扁平插画海报——纯白大留白 + 黑墨细线手绘 + 单一主体自然色 + 稚拙松散手写字体。当用户想要喜茶风格海报、喜茶海报、稚拙插画、手绘水果/饮品/食材海报、naive/childlike 扁平插画风，或想把任意主题套进这套"白底+黑线+单主体自然色+稚拙手写"的插画海报风格时使用。也覆盖"帮我做张像喜茶那种海报"、"照着这个风格出图"、"喜茶字体那种感觉"、"稚拙风"等说法。
---

# 喜茶风 · 稚拙插画海报

> 这套风格源自对一组「学习喜茶风格」海报的视觉拆解（白底水果插画 + 稚拙手写文案）。本 skill 只提取其**视觉规律**，不复制任何原图；生成时永远重画，不照搬构图、不改换原作者素材。

## 风格 DNA（固定不变，每次生成都要守住）

### 1. 配色：白底 + 黑墨 + 单一主体自然色
- **背景**：纯白 `#FFFFFF`，可带极轻微暖白 `#FCFCFC`；背景占画面 **80% 以上**，是留白的主要来源。
- **墨线**：细黑 `#0C0C0C`，用于所有轮廓线、插画描边和手写文字。
- **主体色**：只允许**一个**饱和色，且必须是主体物本身的自然色、略降饱和、不发荧光、不做渐变。常见基准：
  - 暖橙（莲雾 / 柿）`#CC8424` `#E49C3C`
  - 黄绿（柚 / 青柠）`#CCCC54` `#B4B43C` `#E4E46C`
  - 红（荔枝 / 莓）`#CC3C3C` `#FC6C6C` `#B42424`
- **不要**：多色高亮拼贴、渐变、阴影、描金、霓虹色、卡通糖果色。

### 2. 构图与留白
- **单一主体**，居中或略偏上/偏一侧；主体占画面约 1/5~1/3，其余全是白。
- **大量留白**，画面通透；不做满版、不堆砌元素、不加装饰边框。
- 主体扁平、简化、略带手抖的不完美感；不要写实、不要 3D、不要精致矢量感。

### 3. 插画质感
- 扁平插画，**细黑线手绘描边**，线条有粗细起伏的"手"感。
- 轻微纸张/颗粒质感，避免光洁塑料感。
- 稚拙（naive）气质：像随手画的、故意不工整，但形是准的、可爱的。

### 4. 字体气质（最容易被毁的部分）
- **稚拙、松散、细黑线手写**。字形可以歪、大小不一、横画拉长、结构松散。
- **禁止**：标准印刷字体、书法体、圆润可爱体、工整排版。
- 文字要**参与构图**，不一定当标题，可以斜着、绕在主体旁、歪歪扭扭。
- 文案**极短**（2~6 字），可带谐音、轻松、产品灵感感；越短越不容易出乱码/错字。
- 中文若渲染不佳，宁可更短，甚至只保留 2~4 字；必要时允许无文字版。

## 工作流

1. 拿到主题，确定**主体物**（水果 / 食材 / 饮品 / 对象）和它**自然的主色**。
2. 想一句**极短文案**（谐音 / 俏皮优先，2~6 字）。
3. 按下方模板组装提示词，调用图片生成能力（本环境为 `gen_image`），竖版 `3:4`（海报感），尺寸 `2K`。
4. 出图后自查：白底是否干净、是否只有一个饱和色、字体是否稚拙不工整、文案是否错字。

## 提示词模板

```
Flat naive hand-drawn poster illustration on a pure white background with lots of negative space.
One single subject: {主体物}, drawn flat and simplified, with thin black hand-drawn ink outlines
that are slightly uneven and imperfect. The subject uses its natural muted color ({主体色}),
no gradients, no shadows, no neon. Subtle paper grain texture.
Small handwritten Chinese text "{短文案}" rendered accurately and legibly — exactly these characters,
no typos, no missing strokes, no extra strokes. The text is loose hand-lettering with a thin black
marker: strokes slightly shaky and uneven, characters not perfectly aligned, some horizontal strokes
elongated, like quick casual handwriting. NOT a printed sans-serif, NOT calligraphy, NOT a cute
rounded font. The text is small and integrated into the composition near the subject, not a neat headline.
Vertical 3:4 poster, minimalist, lots of white space.
```

- `{主体物}`、`{主体色}`、`{短文案}` 每次替换。
- 中文文案用双引号包住、原样保留，逼模型按字渲染。
- 主体不是水果时（城市 / 科技 / 品牌 / 抽象概念），主体色仍取它最自然的**一个**代表色，保持"单色克制"。
- 中文出字更稳的模型优先：`gpt-image-2` / `seedream-5-0-pro` 对中文字形保真更好；默认模型若把中文写成乱码/错字，就换这两个之一再试。仍不行则缩短文案，或改为无文字版。

## 示例

| 主题 | 主体物 | 主体色 | 文案 |
|---|---|---|---|
| 荔枝 | a lychee | muted red `#CC3C3C` | 荔好 见你 |
| 柚子 | a pomelo | muted yellow-green `#B4B43C` | 柚见你 |
| 杨梅 | a bayberry | muted dark red `#B42424` | 梅你不行 |

## 参考

原风格样本为 4 张白底水果海报，共同规律已归纳进上面的「风格 DNA」。逐张配色拆解与原始链接见 `references/samples.md`（仅作分析依据，不用于复制）。
