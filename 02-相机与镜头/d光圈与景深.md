# 光圈与景深

> 版本：1.0  
> 本文件目标：理解光圈、景深、背景虚化、对焦和运动模糊，并学会用这些概念控制 AI 图像的清晰范围和视觉重点。

---

## 1. 先记住最重要的区别

- **光圈**：镜头内部控制进光量的开口大小，通常用 f 值表达。
- **景深**：画面中看起来足够清晰的距离范围。
- **背景虚化**：背景呈现模糊的视觉结果。
- **对焦**：让你指定的主体或细节处于清晰状态。

这四个概念彼此相关，但不是同义词。

在 AI 提示词里，写 `f/1.4` 或 `shallow depth of field` 都可能影响生成结果，但模型未必严格模拟真实光学。新手最稳妥的做法是：**把想要的清晰范围说清楚，再用光圈数值作为可选补充。**

## 2. f 值是什么？

常见光圈标记包括 f/1.4、f/2、f/2.8、f/4、f/5.6、f/8、f/11、f/16。

在同一镜头下，较小的 f 值通常表示更大的光圈开口；较大的 f 值通常表示更小的光圈开口。

| 光圈示例 | 一般意义 | 常见视觉倾向 |
|---|---|---|
| f/1.2–f/1.8 | 大光圈 | 容易形成浅景深，背景虚化明显 |
| f/2–f/2.8 | 较大光圈 | 人像中常见，主体容易突出 |
| f/4 | 中等光圈 | 主体清晰，背景仍可能有一定虚化 |
| f/5.6–f/8 | 较小光圈 | 更大范围容易保持清晰 |
| f/11–f/16 | 小光圈 | 常用于需要较深景深的场景，但真实画质还受镜头和衍射等因素影响 |

这张表只是一般趋势。实际景深还取决于焦距、对焦距离、主体与背景的距离、画幅等条件。

## 3. 什么是浅景深？

浅景深意味着只有较小范围处于清晰状态，前景或背景容易虚化。常用于人像、静物、食物和需要突出单一主体的画面。

可复制提示词：

```text
shallow depth of field, sharp focus on the subject,
softly blurred background, gentle background separation
```

中文理解：

`浅景深，主体清晰对焦，背景柔和虚化，主体与背景有自然分离。`

适用场景：

- 人像：让眼睛和面部成为视觉重点。
- 产品：让商品从背景中突出。
- 食物：突出食物表面的质感。
- 花朵与微距：让局部细节突出。

### 浅景深常见问题

如果你同时希望“人物眼睛、头发、衣服、远处建筑全部极其清晰”，又要求“极浅景深”，这可能会产生冲突。可以改成：

`人物眼睛清晰，面部主要区域清晰，背景柔和虚化。`

## 4. 什么是深景深？

深景深意味着较大范围内的画面都保持清晰，适合需要展示环境和空间信息的场景。

可复制提示词：

```text
deep depth of field, clear environmental details,
foreground and background remain recognizable,
balanced overall sharpness
```

中文理解：

`较深景深，环境细节清楚，前景与背景都能辨认，整体清晰度平衡。`

常见用途：

- 风光摄影
- 建筑摄影
- 旅行记录
- 环境纪实
- 多人物群像

深景深并不等于画面所有部分都必须拥有完全相同的锐度。真实摄影中，距离、镜头表现和空气透视仍会影响画面。

## 5. 背景虚化与散景

“背景虚化”描述背景变模糊的结果；“散景”（bokeh）更偏向描述焦外高光和模糊区域的视觉形态，例如圆形光斑、柔和边缘或旋涡感。

常用提示词：

- `softly blurred background` — 背景柔和虚化
- `creamy bokeh` — 柔和、顺滑的散景
- `round out-of-focus highlights` — 圆形焦外高光
- `natural background separation` — 自然的主体与背景分离
- `subtle bokeh highlights` — 轻微散景高光

示例：

```text
85mm portrait-lens look, shallow depth of field,
sharp focus on the eyes, creamy background bokeh,
natural skin texture, soft side lighting
```

不要只写“背景虚化”而不说明主体需要清晰的部分。人像通常可写“眼睛清晰对焦”；产品图可以写“标签和产品边缘清晰”。

## 6. 什么影响景深？

### 6.1 光圈

在其他条件相近时，较大光圈通常更容易获得浅景深。

### 6.2 焦距

在其他条件与取景安排相近时，焦距变化会影响景深表现。但不要单独用焦距推断最终虚化程度，因为摄影师可能同时改变拍摄距离。

### 6.3 拍摄距离

相机越靠近主体，通常越容易形成浅景深和明显的前后距离差异。

### 6.4 主体与背景的距离

主体离背景越远，背景通常越容易显得模糊。即使不使用极大光圈，也可能获得较好的主体分离。

### 6.5 画幅与输出尺寸

不同画幅、观看尺寸和成像条件也会影响景深观感。AI 模型不一定严格模拟这些物理关系，因此提示词应优先描述视觉结果。

## 7. 对焦：究竟要让哪里清晰？

在提示词中明确焦点，通常比单写一个光圈数值更有用。

| 目标 | 可复制提示词 |
|---|---|
| 人像眼睛清晰 | `sharp focus on the eyes` |
| 整张面部清楚 | `the entire face in clear focus` |
| 产品标签清晰 | `sharp focus on the product label and edges` |
| 花朵中心清晰 | `focus on the center of the flower` |
| 前景物体清晰 | `foreground subject in sharp focus` |
| 背景建筑清晰 | `clear architectural details in the background` |
| 只有局部清晰 | `selective focus on the key detail` |
| 焦点从近到远变化的感觉 | `focus transition from foreground to background` |

不要同时要求焦点在人物眼睛和远处建筑，而且背景又完全虚化，除非你想要特殊的合成式效果。

## 8. 运动模糊与定格动作

景深解决的是空间中的清晰范围；运动模糊则与主体或相机在曝光期间的运动有关。

### 定格动作

```text
frozen motion, crisp details, sharp subject,
clear action moment
```

适合运动、舞蹈、飞溅水滴等画面。

### 运动模糊

```text
intentional motion blur, moving subject,
dynamic sense of movement, background streaks
```

适合奔跑、车流、舞蹈或表现速度。

### 慢门街景联想

```text
long-exposure street photography, light trails,
stationary architecture, moving traffic blur
```

注意：不要把运动模糊和失焦混为一谈。运动模糊有方向和动态感；失焦通常是清晰平面没有落在正确位置。

## 9. 按题材选择清晰范围

| 题材 | 建议优先描述 | 示例 |
|---|---|---|
| 半身人像 | 眼睛清晰，背景柔和虚化 | `sharp focus on the eyes, softly blurred background` |
| 全身穿搭 | 人物整体清晰，背景适度简化 | `full-body subject in clear focus, gently softened background` |
| 群像 | 多个人物的面部尽量清晰 | `all main subjects in clear focus` |
| 风光 | 前景与远景都能辨认 | `deep depth of field, clear landscape details` |
| 建筑 | 线条与空间细节清楚 | `crisp architectural details, balanced depth of field` |
| 产品图 | 产品关键材质和标签清晰 | `sharp focus on product edges and label` |
| 食物 | 食物主体清晰，背景轻柔 | `food in sharp focus, soft background blur` |
| 微距 | 指定极小细节清晰 | `macro detail, selective focus on the texture` |
| 体育动作 | 主体动作清晰或有意拖影 | `frozen action` 或 `intentional motion blur` |

## 10. 光圈与景深的常见错误

### 错误一：只写 f/1.4

模型可能忽略数值，或只生成模糊背景，却没有把焦点放在你需要的地方。

更好：

```text
wide-aperture portrait look, shallow depth of field,
sharp focus on the eyes, softly blurred background
```

### 错误二：背景模糊得太夸张

更好：

```text
moderate background blur, natural subject separation,
environment still recognizable
```

### 错误三：整张图都模糊

更好：

```text
sharp focus on the main subject, realistic fine details,
only the background is softly blurred
```

### 错误四：所有内容都要求清晰

如果是人像特写，背景不必清晰；如果是建筑和风光，背景细节可能非常重要。根据用途选择。

### 错误五：把大光圈当成高级感

大光圈是技术选择，不是质量保证。清晰的环境肖像、深景深风光和清楚的产品图也可能非常出色。

## 11. 四组可直接使用的提示词

### A. 自然半身人像

```text
natural waist-up portrait, 85mm portrait-lens look,
wide-aperture aesthetic, shallow depth of field,
sharp focus on the eyes, softly blurred park background,
natural skin texture, soft daylight
```

### B. 环境人像

```text
environmental portrait, 35mm perspective,
moderate depth of field, the person and surrounding street remain recognizable,
natural available light, candid documentary feeling
```

### C. 极简产品摄影

```text
minimal product photography, 70mm lens look,
product edges and label in sharp focus,
controlled depth of field, clean background,
soft side lighting, realistic glass and metal texture
```

### D. 风光摄影

```text
wide landscape photography, deep depth of field,
clear foreground rocks and distant mountain ridges,
natural atmospheric perspective, balanced sharpness,
soft early-morning light
```

## 12. 一次只测试一个变量

固定主体、构图、光线和色彩，分别比较：

- A：`shallow depth of field`
- B：`moderate depth of field`
- C：`deep depth of field`

之后再测试焦点位置：

- A：眼睛清晰
- B：整个主体清晰
- C：主体与环境都清晰

每次生成多张并记录结果。这样可以分清楚模型对“景深”与“对焦”指令的响应。

## 13. 可复制的景深词库

**光圈联想**
- `wide-aperture look`
- `f/1.4 lens aesthetic`
- `f/2.8 lens aesthetic`
- `f/5.6 lens aesthetic`
- `f/8 lens aesthetic`

**景深**
- `shallow depth of field`
- `moderate depth of field`
- `deep depth of field`
- `natural background separation`
- `softly blurred background`
- `environment remains recognizable`

**对焦**
- `sharp focus on the eyes`
- `the entire face in clear focus`
- `sharp focus on product edges`
- `selective focus on the key detail`
- `clear environmental details`

**运动**
- `frozen motion`
- `intentional motion blur`
- `long-exposure light trails`
- `stationary subject, blurred background movement`

## 14. 最小练习

使用同一个主体，例如“一只放在桌上的黑色香水瓶”。保持构图和光线一致，测试：

1. 浅景深，标签清晰，背景虚化。
2. 中等景深，瓶身和一部分环境清晰。
3. 深景深，产品和背景细节都可辨认。

再固定景深，分别尝试“50mm 标准视角”和“85mm 产品摄影视角”。比较主体大小、背景关系和清晰范围。

**记住：想让 AI 照片看起来像真实摄影，先说清楚哪里清晰、哪里模糊，再补充光圈数值。**
