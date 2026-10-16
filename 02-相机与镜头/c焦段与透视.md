# 焦段与透视

> 版本：1.0  
> 本文件目标：让你理解广角、标准焦段、长焦、空间压缩和透视，并把这些概念变成可用的 AI 摄影提示词。

---

## 1. 焦段是什么？

焦段通常以毫米（mm）表示，例如 24mm、35mm、50mm、85mm、135mm。它与镜头视角相关：在同一画幅上，焦段越短，通常看到的范围越宽；焦段越长，通常看到的范围越窄。

对 AI 图像来说，焦段提示词常被用来引导视角和空间观感。但模型未必严格遵循真实镜头的光学规律，因此应把焦段词当作一种视觉指令，而不是绝对保证。

## 2. 常见焦段速查

以下以 35mm 全画幅视角作为便于理解的参考。不同画幅上的实际视角会不同。

| 焦段范围（约） | 常见称呼 | 视觉特点 | 常见用途 |
|---|---|---|---|
| 14–20mm | 超广角 | 视野很宽，近处与远处的大小差异容易显著 | 建筑、室内、夸张空间、广阔场景 |
| 24–28mm | 广角 | 环境信息多，空间感明显 | 街头、旅行、建筑、环境人像 |
| 35mm | 广角到标准之间的常用视角 | 环境与主体较容易平衡 | 街拍、纪实、环境人像 |
| 50mm | 标准焦段 | 视角较自然，适合通用题材 | 日常、人像、静物 |
| 85mm | 人像常用中长焦 | 便于突出人物，背景更容易简化 | 肖像、时尚、半身人像 |
| 105–135mm | 中长焦 | 取景范围较窄，适合突出主体 | 人像、舞台、远处细节 |
| 200mm 及以上 | 长焦 | 视野窄，适合远距离主体 | 体育、野生动物、远景细节 |

不要把表格当作硬性规则。摄影师可以用 35mm 拍人像，也可以用 85mm 拍街头；镜头选择取决于距离、环境和想表达的效果。

## 3. 不同焦段如何写进提示词？

### 3.1 24mm：环境与空间

适合：街景、室内、建筑、旅行、需要环境参与叙事的人像。

```text
24mm wide-angle perspective, environmental portrait,
the surroundings remain important, visible depth in the street,
natural perspective, avoid exaggerated facial distortion
```

中文理解：

`24mm 广角视角，环境人像，周围街景仍然重要，街道空间纵深明显，透视自然，避免面部被夸张拉伸。`

注意：广角靠近人物拍摄时，脸部和身体比例可能显得夸张。若希望人物面部自然，不要同时要求极近距离广角肖像。

### 3.2 35mm：街头与纪实

适合：街头抓拍、旅行人像、生活场景。

```text
35mm street photography perspective, candid framing,
subject and environment balanced, natural eye-level view,
documentary atmosphere
```

中文理解：

`35mm 街头摄影视角，抓拍式构图，主体与环境平衡，平视角度，自然纪实氛围。`

### 3.3 50mm：自然通用视角

适合：日常人像、静物、生活方式摄影。

```text
50mm standard-lens perspective, natural proportions,
balanced framing, realistic subject-to-background relationship
```

中文理解：

`50mm 标准镜头视角，主体比例自然，构图平衡，主体与背景的空间关系可信。`

### 3.4 85mm：人像与背景简化

适合：半身肖像、时尚人像、需要突出人物的画面。

```text
85mm portrait-lens look, flattering portrait perspective,
clear facial features, softly simplified background,
natural skin texture
```

中文理解：

`85mm 人像镜头观感，人物面部比例自然，背景柔和简化，保留真实皮肤纹理。`

### 3.5 135mm：更远距离的人像

适合：舞台、户外人像、背景简化、远距离抓拍。

```text
135mm telephoto portrait look, tighter field of view,
subject separated from a distant background,
natural facial proportions, compressed spatial appearance
```

中文理解：

`135mm 长焦人像观感，视野较窄，人物与远处背景分离，面部比例自然，空间显得更压缩。`

### 3.6 200mm 及以上：远处主体

适合：体育、舞台、远处人物、野生动物或远景细节。

```text
long telephoto perspective, distant subject framed tightly,
narrow field of view, background appears visually closer,
clear subject separation
```

## 4. 焦段和透视不是同一件事

这是一个很重要、也很容易混淆的概念：

- **焦段**影响镜头的视角范围。
- **透视关系**主要由相机与主体之间的位置和距离决定。
- 在真实摄影中，为了让主体在不同焦段下保持相同大小，摄影师通常会移动相机；距离变化会改变透视观感。

因此，不要简单地认为“长焦天生把脸拍得更扁”或“广角天生让鼻子变大”。更准确的说法是：广角镜头经常被用于靠近主体拍摄，而靠近会强化近大远小的透视差异；长焦人像通常在较远距离拍摄，因此透视差异相对不明显。

## 5. 什么是透视夸张？

当镜头离主体很近时，离镜头近的部分会显得更大，远处部分显得更小。例如近距离拍脸时，鼻子可能显得较大，耳朵和头部后侧相对缩小。

提示词可以这样写：

```text
close camera distance, pronounced perspective,
foreground features appear larger, dynamic spatial depth
```

如果你不想要这种效果：

```text
natural facial proportions, moderate camera distance,
avoid exaggerated wide-angle facial distortion
```

## 6. 什么是空间压缩？

空间压缩通常指画面里不同距离的对象看起来距离更接近。长焦镜头常与这种观感联系在一起，因为拍摄者通常会站得更远来获得相似的主体大小。

适合：人像背景、城市街道、山脉层叠、舞台摄影。

```text
telephoto perspective, compressed spatial appearance,
distant buildings appear visually closer together,
subject framed against a simplified background
```

风光例子：

```text
long-lens landscape photography, layered mountain ridges,
compressed distance, atmospheric haze, subtle tonal separation
```

## 7. 焦段如何影响背景？

焦段并不是唯一决定背景虚化的因素。背景虚化还与光圈、拍摄距离、主体与背景距离、传感器/画幅等因素有关。

可以用以下思路：

- 想让环境更明显：尝试广角视角，并让环境进入画面。
- 想突出人物同时保留环境：尝试 35mm 或 50mm 的环境人像。
- 想简化背景：尝试 85mm 或更长焦段的视觉联想，并明确背景虚化或背景简洁。
- 想让背景中的远处建筑看起来更靠近：尝试长焦与空间压缩描述。

不要只写“85mm”就期待模型自动得到完美背景虚化。最好明确写出结果。

## 8. 用场景选焦段

| 场景 | 可先尝试 | 为什么 |
|---|---|---|
| 狭窄街巷环境人像 | 24–35mm | 能展示环境和空间 |
| 自然街头抓拍 | 35mm | 主体与环境较容易平衡 |
| 日常半身人像 | 50–85mm | 容易控制人物比例与背景 |
| 时尚半身肖像 | 85mm | 便于突出人物与简化背景 |
| 舞台或远处人物 | 135–200mm+ | 适合远距离取景 |
| 极简建筑室内 | 16–24mm | 便于纳入空间，但要控制线条和边缘变形 |
| 山脉层叠风光 | 100–300mm 视觉联想 | 容易突出远处山脉层次与压缩感 |
| 食物与静物 | 50–100mm 视觉联想 | 便于控制主体比例和背景 |
| 微小物体细节 | 微距镜头描述 | 强调极近距离细节和局部清晰度 |

这只是起点，不是限制。AI 生成时也可以直接描述你希望的视角，不必拘泥于焦段数字。

## 9. 透视、脸型与人像

如果你想生成自然的人像，可以优先使用：

```text
natural facial proportions, eye-level portrait,
moderate camera distance, realistic perspective,
no exaggerated wide-angle distortion
```

如果你有意追求强烈广角效果：

```text
close wide-angle portrait, dynamic perspective,
foreground features subtly enlarged, energetic editorial style
```

注意“夸张透视”是风格选择，不一定是错误；关键是它是否符合你的目的。

## 10. 焦段与透视的常见问题诊断

| 问题 | 可能原因 | 提示词调整 |
|---|---|---|
| 脸部比例夸张 | 近距离广角观感 | natural facial proportions, moderate camera distance |
| 背景过多、主体不突出 | 视野太宽或景别太远 | tighter framing, subject fills more of the frame |
| 环境不够丰富 | 视野较窄或取景太近 | wider environmental view, 24–35mm perspective |
| 人物和背景混在一起 | 背景复杂、主体分离不足 | simplified background, clear subject separation |
| 山脉层次不明显 | 空间层次或长焦压缩描述不足 | telephoto landscape, layered ridgelines |
| 建筑边缘过度拉伸 | 夸张广角透视 | moderate wide angle, straight vertical lines |
| 人物看起来太扁平 | 光线和角度缺少塑形 | three-quarter angle, directional side light |
| 背景虚化不明显 | 只写焦段，没有写景深结果 | shallow depth of field, softly blurred background |

## 11. 焦段对照实验

固定同一人物、同一光线和同一构图意图，分别测试：

A. `24mm wide-angle environmental portrait`  
B. `35mm street portrait perspective`  
C. `50mm standard-lens perspective`  
D. `85mm portrait-lens look`  
E. `135mm telephoto portrait look`

对比：

- 面部比例是否变化？
- 环境进入画面的多少？
- 背景是否更简洁？
- 空间感是夸张还是压缩？
- 哪个视角最符合你的审美？

注意：模型可能不严格执行毫米数值，因此应同时观察实际画面，不要只看提示词字面。

## 12. 可复制的焦段词库

- `ultra-wide-angle perspective`
- `24mm wide-angle environmental portrait`
- `35mm street photography perspective`
- `50mm standard-lens perspective`
- `85mm portrait-lens look`
- `135mm telephoto portrait look`
- `long telephoto perspective`
- `compressed spatial appearance`
- `natural facial proportions`
- `moderate camera distance`
- `close camera distance`
- `layered mountain ridges`
- `clear subject separation`
- `wide environmental view`
- `tight framing`

## 13. 最小练习

选择一个主体，比如“穿黑色外套的人站在城市街道上”。只改焦段和视角描述：

- 24mm：环境人像，街道占画面较大部分。
- 35mm：人物与街道平衡。
- 50mm：人物更突出，环境仍然可见。
- 85mm：半身肖像，背景柔和简化。
- 135mm：较远距离取景，空间压缩感更明显。

其他提示词保持不变。保存结果并比较，你会比单纯背焦段定义学得更快。
