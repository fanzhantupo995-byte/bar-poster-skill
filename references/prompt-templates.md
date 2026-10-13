# 生图 Prompt 模板

> 生图方式由用户提供（API、生图工具等），模型优先级：Image 2 / 2.5 → Seedream 5.0 Pro。模板中的 `{...}` 为占位符，按实际情况填充。

## Prompt 污染防范

- 有用户参考图时，场景、构图、光影、氛围词必须来自参考图提炼，不要把模板里的默认场景词带进 Prompt。
- 模板中标注 `{场景锚点}`、`{光影锚点}` 的位置，必须来自用户需求、用户参考图提炼或用户选定的参考输入；Skill 不提供默认夜店舞台风格。
- 不要因为 Skill 名字或海报类型是夜店/酒吧，就自动追加 `club`、`nightclub`、`stage` 等词；这些词只应出现在用户需求或参考图提炼明确指向该场景时。
- 缺少场景依据时，先向用户要参考图或问清楚想要的场景与光影；不要替用户填入夜店舞台、舞池、霓虹等默认词。

## 通用结构

```
[场景与主体] + [构图与空间] + [光影描述] + [色彩方案] + [风格锚点] + [氛围细节] + [画幅]
```

## 场景与光影锚点

所有场景与光影锚点只使用以下来源：

1. 用户文字需求中明确提到的场景、光影或氛围
2. 用户提供的参考图
3. 用户选定或认可的搜索参考图

没有这些依据时，不要生成场景与光影锚点；先向用户确认参考方向。

## 按海报类型的模板

### 嘉宾海报（DJ / 音乐人）
```
{嘉宾照片描述}, {姿态/位置}, {场景锚点: 必须来自用户需求或参考图},
{光影锚点: 必须来自用户需求或参考图}, rim light on subject,
{氛围细节: 来自参考图提炼}, {构图}, 9:16 poster background, no text
```

### 女团 / 男团海报
```
group of {N} performers, {站位构图}, {风格: hip-hop / electronic / jazz},
{光影锚点: 必须来自用户需求或参考图}, {主色} color scheme, {明度氛围},
dynamic energy, poster background, no text
```

### 酒水海报
```
{酒名} bottle / cocktail, {置入方式}, {背景场景: bar counter / ice / splash},
{光影: backlit / neon glow}, liquid splash frozen motion,
{强调色} accent, premium product photography style, no text
```

### 月底收官 / 爆满 / 氛围向
```
{场景锚点: 必须来自用户需求或参考图}, hands in the air,
{色调与光效: 来自参考图提炼}, lens flare, haze, energy and movement, wide angle,
cinematic atmosphere, poster background, no text
```

### 品牌概念海报
```
{品牌空间/概念描述}, minimal or atmospheric composition,
{品牌色} palette, {光影氛围}, premium mood,
poster background, no text
```

### 节日海报
```
{节日元素: halloween pumpkins / christmas lights / fireworks},
{场景锚点: 必须来自用户需求或参考图}, {节日色系} lighting,
{氛围: mysterious / festive / grand}, poster background, no text
```

### 派对主题海报
```
{主题视觉元素}, {主题色} dominant color, {主题风格锚点},
{场景锚点: 必须来自用户需求或参考图}, {场景元素}, high energy,
poster background, no text
```

## 融合类 Prompt 段落（Logo / IP / 人物 / 产品）

> 融合类需求建议用「图生图 / 参考图」方式：把 Logo / IP / 写真 / 酒水图作为参考图输入。

```
将参考图中的 {logo/IP/人物/产品} 融入海报场景：
- 保持 {logo/IP/人物/产品} 的识别度和完整轮廓
- 场景光照与主体光影统一（{光源方向}、{色温}）
- 主体与背景边缘自然融合（{处理方式: rim light / glow / color grade}）
- 构图位置：{位置}；文字后期可直接叠加在主体或场景元素上，不要求预留空白
```

## 通用负面词

```
text, watermark, logo placeholder, low quality, blurry, deformed hands,
extra fingers, oversaturated, flat lighting
```
