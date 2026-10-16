# AI 摄影提示词知识库

> 版本：1.0\
> 用途：帮助非专业用户理解摄影语言、组合 AI
> 图片提示词，并通过实验建立自己的风格库。\
> 适用范围：GPT Image、Midjourney、Flux、SDXL
> 等图像生成模型。不同模型对相机、镜头和胶片术语的响应可能不同。

------------------------------------------------------------------------

## 0. 如何使用这份知识库

你不需要一次学会所有术语。推荐按以下顺序使用：

1.  **先选目标**：想生成什么------自然人像、街拍、电影剧照、产品广告、风景等。
2.  **选构图与镜头**：确定拍摄距离、视角、主体和背景关系。
3.  **选光线**：确定光从哪里来、软还是硬、环境是什么。
4.  **选色彩与质感**：决定自然数码、胶片、黑白、复古或电影调色。
5.  **选择成片风格**：把前面元素组织成统一的视觉方向。
6.  **复制模板并替换主体**：先用基础版生成，再逐次调整。
7.  **记录实验结果**：不要只保存最好的图，也保存提示词和失败原因。

### 核心原则

-   **摄影词汇是控制意图，不是物理保证。** AI
    不一定会严格模拟指定相机的真实光学特性。
-   **具体描述通常比只写品牌更可控。**
    "柔和的侧窗光、自然肤色、细腻颗粒"比只写"Leica look"更清楚。
-   **一次只改一个主要变量。** 否则很难知道结果为什么变化。
-   **减少互相矛盾的要求。**
    例如同时要求"柔和低反差"和"极端高反差"，除非你明确知道自己想要什么。
-   **先描述画面，再描述设备。**
    主体、构图、光线和色彩通常是优先级更高的基础。
-   **不同模型需要不同写法。**
    本库是通用起点，不是所有模型都适用的固定公式。

------------------------------------------------------------------------

# 1. AI 摄影提示词总结构

建议把提示词分成七个模块。不是每次都必须写满。

  -------------------------------------------------------------------------------------------
  模块                    要回答的问题                   例子
  ----------------------- ------------------------------ ------------------------------------
  A. 主体与场景           拍什么？在哪里？正在做什么？   一位女性走过雨后的东京街道

  B. 构图与机位           从哪里拍？画面如何安排？       半身、平视、人物偏左、保留环境

  C. 相机与镜头           画面想有什么视角和成像联想？   35mm lens、85mm portrait lens

  D. 光线                 光从哪里来？软硬如何？         侧窗光、阴天漫射光、逆光

  E. 色彩与介质           像什么胶片或数码色彩？         Portra 400 风格、黑白纪实

  F. 成片风格             最终属于哪种摄影语言？         时尚编辑摄影、纪实、商业广告

  G. 质量与限制           哪些特征必须保留或避免？       自然皮肤纹理、不过度磨皮、背景简洁
  -------------------------------------------------------------------------------------------

## 通用模板

``` text
[主体与场景],
[构图与机位],
[camera / lens aesthetic],
[lighting],
[color and film aesthetic],
[photographic style],
[texture and detail],
[important constraints].
```

中文理解版：

``` text
拍摄对象与场景 + 构图与视角 + 相机/镜头风格
+ 光线 + 色彩/胶片 + 成片风格 + 质感 + 必须遵守的限制
```

## 最简模板

当你不想写很长时，只写四件事：

``` text
[主体与场景], [构图], [光线], [想要的成片风格].
```

例子：

``` text
A candid portrait of a young woman in a quiet cafe,
medium close-up, soft window light, natural skin texture,
subtle film colors, understated editorial photography.
```

------------------------------------------------------------------------

# 2. 主体、场景与构图库

这一部分决定"画面里有什么，以及观众如何看到它"。

## 2.1 景别 Shot Size

  中文     英文提示词              画面用途
  -------- ----------------------- ------------------------------
  大远景   extreme long shot       人物很小，突出环境和空间
  远景     long shot / wide shot   展示人物全身与周围环境
  全身     full-body shot          展示完整人物造型、服装与姿态
  中景     medium shot             通常展示腰部以上或人物与环境
  中近景   medium close-up         适合交流感强的人像
  近景     close-up                突出面部、物品或情绪
  特写     extreme close-up        眼睛、嘴唇、材质、产品局部

提示：景别的边界不是绝对的。为了避免歧义，可以同时写出具体范围，例如
`full-body portrait, head to toe visible`.

## 2.2 相机机位 Camera Angle

  中文         英文                            视觉效果
  ------------ ------------------------------- ------------------------------
  平视         eye-level angle                 自然、平等、纪实
  低机位仰拍   low-angle shot                  主体显得高大、有力量
  高机位俯拍   high-angle shot                 主体显得弱小，或展示环境
  顶视         overhead shot / top-down view   平面布局、食物、静物、设计感
  贴地低机位   ground-level angle              强调前景、运动感、宏大透视
  过肩镜头     over-the-shoulder shot          对话、观察感、叙事感
  主观视角     first-person POV                让观众仿佛身处现场

## 2.3 构图 Composition

  中文         英文                      适合用途
  ------------ ------------------------- ----------------------------
  三分法       rule of thirds            自然、平衡、不呆板
  居中构图     centered composition      稳定、庄重、产品展示
  对称构图     symmetrical composition   建筑、仪式感、秩序感
  留白         negative space            极简、海报、奢侈品牌
  引导线       leading lines             道路、走廊、建筑、纵深
  前景遮挡     foreground framing        增加空间层次和窥视感
  层次构图     layered composition       让前景、中景、背景各有作用
  近距离裁切   tight crop                时尚编辑摄影、情绪特写
  非中心构图   off-center composition    抓拍、自然感、动态感
  负空间构图   generous negative space   高端广告、封面设计

## 2.4 画面比例

  比例   常见用途
  ------ ----------------------------
  1:1    头像、社交媒体方图、产品图
  4:5    人像、社交平台竖图
  2:3    经典照片比例、全身人像
  3:2    常见相机横幅照片
  16:9   电影感画面、横向场景
  9:16   手机竖屏、短视频封面
  21:9   宽银幕电影感构图

比例通常应使用生成工具本身的画幅设置来控制；在提示词中也可以描述构图，但文字不一定能决定最终输出尺寸。

------------------------------------------------------------------------

# 3. 相机系统与机身风格库

## 3.1 先理解相机类型

  --------------------------------------------------------------------------------------------------
  类型              通俗理解                       常见风格联想               常见用途
  ----------------- ------------------------------ -------------------------- ----------------------
  35mm 胶片相机     传统胶片摄影                   生活感、颗粒、抓拍         街拍、旅行、人像

  旁轴胶片相机      小巧、适合街头观察的相机类型   人文、克制、纪实           街头、日常记录

  中画幅胶片相机    使用更大胶片画幅               时尚人像、细腻层次         人像、编辑摄影

  全画幅数码相机    常见的专业数码相机类别         清晰、现代、用途广         商业、人像、活动

  中画幅数码相机    高端商业摄影常用类别           精细、平滑层次、奢华       产品、时尚、静物

  电影摄影机        为动态影像设计的摄影系统       电影色彩、宽银幕、氛围光   电影剧照、叙事画面

  即时成像相机      拍摄后直接得到实体照片         即时照片、边框、怀旧       生活快照、复古

  玩具胶片相机      光学控制较简单的相机           暗角、漏光、粗粝、随机感   实验、艺术摄影

  运动相机          小型、广角、适合运动场景       临场感、夸张广角           运动、旅行、第一人称
  --------------------------------------------------------------------------------------------------

## 3.2 常见机身名称：把它们当作风格入口

  -------------------------------------------------------------------------------------------------------------------
  相机 / 系统             可尝试的提示词方向           示例关键词
  ----------------------- ---------------------------- --------------------------------------------------------------
  Leica M6                35mm 胶片街拍、人文纪实      `Leica M6, 35mm film photography, candid street photography`

  Leica M11               现代旁轴街拍、高端纪实       `Leica M11, understated documentary photography`

  Contax T2               便携胶片快照、旅行人像       `Contax T2, candid travel snapshots, analog film aesthetic`

  Contax 645              中画幅时尚人像               `Contax 645, medium-format portrait aesthetic`

  Hasselblad 500C/M       经典中画幅胶片、静物         `Hasselblad 500C/M, classic medium-format film`

  Hasselblad X2D          高端中画幅数码、产品与时尚   `Hasselblad X2D, refined commercial photography`

  Canon EOS R5            现代商业人像与清晰画面       `Canon EOS R5, professional portrait photography`

  Sony A7R V              高解析数码、时尚与细节       `Sony A7R V, high-resolution editorial photography`

  Nikon D850              高细节、风光、商业摄影       `Nikon D850, detailed landscape photography`

  Fujifilm X100 系列      便携街拍、生活方式摄影       `Fujifilm X100, candid everyday street photography`

  Polaroid SX-70          即时成像、怀旧快照           `Polaroid SX-70, instant film photograph`

  Holga 120               玩具相机、暗角、漏光         `Holga 120, vignetting, light leaks, lo-fi film aesthetic`

  ARRI ALEXA 65           大画幅电影剧照风格           `ARRI ALEXA 65, cinematic still, controlled lighting`

  RED V-RAPTOR            高细节数字电影摄影联想       `RED V-RAPTOR, detailed cinematic image`
  -------------------------------------------------------------------------------------------------------------------

### 关于机身名称的注意事项

-   上表不是使用量排行榜，也不表示某个机身一定比其他型号生成得更好。
-   真实相机的颜色还会受镜头、曝光、光源、白平衡、胶片、冲洗和后期影响。
-   AI 可能只理解相机名称的一部分联想，甚至忽略具体型号。
-   如果型号名称没有带来明显变化，优先写清楚你真正想要的效果：构图、光线、色彩、反差和质感。

------------------------------------------------------------------------

# 4. 镜头与焦段库

## 4.1 焦段选择表

  ------------------------------------------------------------------------------------------------------------
  焦段范围                常见视觉用途               英文提示词
  ----------------------- -------------------------- ---------------------------------------------------------
  14--20mm                超广角、建筑、夸张透视     `ultra-wide-angle lens, dramatic perspective`

  24mm                    环境、旅行、空间感         `24mm wide-angle lens, immersive environment`

  28mm                    街头、纪实、环境人像       `28mm lens, documentary street photography`

  35mm                    街拍、日常、环境人像       `35mm lens, environmental portrait`

  50mm                    自然视角、通用人像         `50mm lens, balanced natural perspective`

  85mm                    人像、背景分离             `85mm portrait lens, shallow depth of field`

  105mm                   人像、细节、局部特写       `105mm lens, refined portrait compression`

  135mm                   长焦人像、远距离抓拍       `135mm telephoto lens, compressed perspective`

  200mm 及以上            运动、野生动物、远景       `long telephoto lens, isolated distant subject`

  微距镜头                极近距离细节、材质         `macro lens, extreme close-up, fine surface detail`

  变形宽银幕镜头          电影宽银幕联想、椭圆散景   `anamorphic lens aesthetic, cinematic wide composition`
  ------------------------------------------------------------------------------------------------------------

## 4.2 焦段不是固定风格开关

摄影中的透视关系主要取决于相机到主体的距离。焦段决定视角与取景范围；AI
对这些物理规律的模拟并不总是准确。

使用时可以把焦段和构图一起描述：

-   `35mm lens, environmental portrait, subject and surroundings both visible`
-   `85mm portrait lens, tight head-and-shoulders framing, soft background`
-   `macro lens, close-up of water droplets on a flower petal`

## 4.3 光圈与景深

  --------------------------------------------------------------------------------------
  关键词                                期望效果                 适合场景
  ------------------------------------- ------------------------ -----------------------
  `f/1.2`                               极浅景深的风格联想       人像、弱光、背景虚化

  `f/1.4`                               浅景深、主体分离         人像、夜景

  `f/2`                                 明显背景虚化             人像、生活方式

  `f/2.8`                               主体突出但保留部分环境   人像、活动摄影

  `f/4`                                 更多环境清晰             环境人像、旅行

  `f/5.6`                               中等至较大景深           街拍、日常

  `f/8`                                 更大范围清晰的风格联想   风光、建筑、静物

  `shallow depth of field`              浅景深                   主体突出

  `deep depth of field`                 深景深                   环境与主体都清楚

  `soft background bokeh`               柔和背景虚化             人像、花卉

  `subject and background both sharp`   主体与背景均清晰         建筑、产品、风景
  --------------------------------------------------------------------------------------

注意：光圈数字不是精确控制 AI
景深的保证。还要写明主体与背景的距离、拍摄距离以及想要的虚化效果。

------------------------------------------------------------------------

# 5. 胶片与成像介质库

胶片名称是风格联想入口。建议同时描述实际视觉特征，不要只写一个品牌型号。

## 5.1 常见彩色胶片

  -------------------------------------------------------------------------------------------------------------------
  胶片                    可探索的视觉方向               英文关键词
  ----------------------- ------------------------------ ------------------------------------------------------------
  Kodak Portra 160        柔和色彩、细腻人像             `soft color palette, fine grain, natural skin tones`

  Kodak Portra 400        自然肤色、柔和色彩、通用人像   `natural skin tones, subtle grain, gentle colors`

  Kodak Portra 800        高感胶片联想、暖调弱光人像     `warm skin tones, available light, fine film grain`

  Kodak Gold 200          暖阳、生活快照、怀旧感         `warm sunny colors, nostalgic snapshot aesthetic`

  Kodak Ektar 100         鲜明色彩、细节、风光           `vivid colors, fine detail, saturated landscape`

  Fujifilm Velvia 50      高饱和风光、浓郁色彩           `rich greens, vivid saturation, slide film aesthetic`

  Fujifilm Pro 400H       柔和人像色彩、浅淡绿色         `airy pastel tones, soft greens, delicate portrait colors`

  Fujifilm Superia        日常彩色快照、生活感           `everyday color film, casual snapshot aesthetic`

  CineStill 800T          钨丝灯夜景、霓虹、光晕联想     `tungsten night, neon glow, halation`

  Kodachrome 64           经典旅行纪实、复古反转片联想   `classic slide film, rich reds, vintage documentary color`
  -------------------------------------------------------------------------------------------------------------------

## 5.2 常见黑白胶片

  ------------------------------------------------------------------------------------------------------------
  胶片                    可探索的视觉方向               英文关键词
  ----------------------- ------------------------------ -----------------------------------------------------
  Kodak Tri-X 400         粗粝纪实、明显颗粒、强烈明暗   `gritty monochrome, visible grain, punchy contrast`

  Ilford HP5 Plus         灵活的黑白纪实、丰富灰阶       `classic black-and-white film, rich midtones`

  Ilford Delta 100        细腻黑白、清晰细节             `fine-grain monochrome, clean tonal detail`

  Kodak T-Max 100         细颗粒、清晰黑白影调           `fine-grain black-and-white photography`
  ------------------------------------------------------------------------------------------------------------

## 5.3 不指定具体胶片时的质感词

  目标           英文提示词
  -------------- ----------------------------------------------
  自然肤色       `natural skin tones`
  柔和高光       `gentle highlight roll-off`
  细腻颗粒       `subtle fine film grain`
  粗颗粒         `visible coarse film grain`
  低对比         `low-contrast tonal rendering`
  高反差         `high-contrast tonal rendering`
  柔和色彩       `muted color palette`
  浓郁色彩       `rich saturated colors`
  轻微褪色       `slightly faded colors`
  暖色调         `warm color palette`
  冷色调         `cool color palette`
  轻微漏光       `subtle film light leaks`
  暗角           `natural lens vignetting`
  高光光晕       `subtle halation around bright lights`
  真实材质       `natural material texture`
  避免塑料皮肤   `realistic skin texture, minimal retouching`

### 真实胶片与 AI 胶片风格的区别

真实胶片会受到曝光、冲洗、扫描和后期处理影响。同一款胶片也不会在所有场景下呈现完全相同的颜色。AI
中的胶片名称应被视为风格提示，而不是准确的物理模拟。

------------------------------------------------------------------------

# 6. 光线与布光库

描述光线时，尽量同时写明：**光源 + 方向 + 软硬 + 环境**。

## 6.1 光线类型

  类型         英文提示词                     常见效果
  ------------ ------------------------------ ----------------------------
  窗边自然光   `soft window light`            自然、亲近、适合人像
  侧光         `directional side lighting`    强调轮廓和材质
  逆光         `backlighting`                 发丝轮廓、通透感、剪影
  轮廓光       `rim lighting`                 主体边缘与背景分离
  顺光         `front lighting`               清晰、阴影较少
  顶光         `overhead lighting`            戏剧化或强烈的顶部阴影
  阴天漫射光   `overcast diffused daylight`   柔和、均匀
  黄金时刻     `golden hour sunlight`         温暖、低角度阳光
  蓝调时刻     `blue hour ambient light`      日落后偏冷的环境光
  直接闪光     `direct on-camera flash`       明亮主体、明显阴影、快照感
  柔光箱       `large diffused softbox`       受控、柔和的商业布光
  伦勃朗光     `Rembrandt lighting`           经典戏剧性人像
  蝴蝶光       `butterfly lighting`           正面偏上方的人像光
  霓虹混合光   `mixed neon lighting`          城市夜景、彩色反射
  烛光         `candlelight`                  暖色、低照度、亲密氛围
  聚光灯       `hard spotlight`               强烈主体强调和舞台感

## 6.2 光线软硬

  描述           英文                         视觉理解
  -------------- ---------------------------- ------------------------
  柔光           `soft light`                 阴影边缘柔和
  硬光           `hard light`                 阴影边缘清晰
  漫射光         `diffused light`             光线经过扩散，较均匀
  方向性强的光   `directional light`          明确的明暗方向
  低反差光       `low-contrast lighting`      明暗差距较小
  高反差光       `high-contrast lighting`     明暗差距明显
  轮廓清晰       `defined shadows`            形体感更强
  阴影保留细节   `detailed shadows`           暗部不完全糊黑
  高光不过曝     `controlled highlights`      亮部细节更完整
  光线穿透薄雾   `light beams through haze`   形成可见光束与空间层次

## 6.3 按场景选择光线

  场景       推荐起点
  ---------- ------------------------------------------------------
  自然人像   `soft window light, gentle shadows`
  户外人像   `open shade, diffused daylight`
  时尚大片   `large softbox, subtle rim light`
  纪实街拍   `available light, realistic ambient shadows`
  电影夜景   `motivated practical lights, atmospheric backlight`
  产品摄影   `controlled softbox reflections, soft ground shadow`
  戏剧肖像   `directional side light, deep but detailed shadows`
  夏日旅行   `warm afternoon sunlight, natural color`
  霓虹夜景   `mixed neon lighting, colored reflections`

------------------------------------------------------------------------

# 7. 成片风格库

成片风格是多个因素共同产生的结果。不要只依赖一个标签。

  ---------------------------------------------------------------------------------------------------------------------
  风格                    主要视觉特征                   可用关键词
  ----------------------- ------------------------------ --------------------------------------------------------------
  日系生活摄影            日常感、自然光、克制色彩       `Japanese lifestyle photography, candid, soft natural light`

  人文纪实                真实瞬间、环境关系、自然瑕疵   `humanist documentary photography, candid moment`

  街头摄影                城市环境、抓拍、瞬间感         `street photography, spontaneous composition`

  高端时尚                造型精确、布光控制、画面秩序   `high-end fashion editorial, refined styling`

  商业人像                清晰、专业、可控布光           `professional commercial portrait photography`

  奢侈品广告              克制、材质细腻、留白           `luxury campaign, elegant negative space`

  电影剧照                空间层次、叙事光线、氛围       `cinematic still, narrative lighting, atmospheric depth`

  复古快照                直接闪光、随手构图、怀旧色彩   `vintage snapshot, direct flash, analog color`

  极简产品摄影            简洁背景、精确反射、明确形体   `minimalist product photography, controlled reflections`

  黑白纪实                灰阶、颗粒、明暗塑形           `black-and-white documentary photography, rich midtones`

  风光摄影                空间、自然色彩、层次           `landscape photography, atmospheric depth`

  建筑摄影                线条、几何、透视控制           `architectural photography, clean geometry`

  美食摄影                食物质感、方向性光线           `food photography, appetizing texture, directional light`

  静物摄影                物体关系、材质和阴影           `still-life photography, carefully controlled lighting`

  运动摄影                动作瞬间、动势、临场感         `sports photography, decisive moment, dynamic framing`
  ---------------------------------------------------------------------------------------------------------------------

## 风格组合规则

建议采用：

-   一个主风格；
-   最多一到两个辅助风格；
-   明确三到五个可见的视觉特征。

例如：

``` text
Main style: candid street photography
Supporting style: subtle analog film aesthetic
Visual traits: natural skin tones, available light, imperfect framing
```

不要在没有明确主次的情况下堆叠大量风格标签。

------------------------------------------------------------------------

# 8. 后期、质感与真实感控制

  -----------------------------------------------------------------------------------------
  目标                    英文提示词                           注意事项
  ----------------------- ------------------------------------ ----------------------------
  自然皮肤                `natural skin texture`               不等于夸张毛孔

  少修饰                  `minimal retouching`                 适合真实人像

  保留细节                `fine detail preserved`              避免过度锐化

  轻微颗粒                `subtle film grain`                  不要误写成严重噪点

  高光柔和                `gentle highlight roll-off`          强调亮部过渡

  暗部有层次              `detailed shadows`                   不要让暗部全黑

  自然颜色                `restrained color grading`           适合真实摄影

  轻微镜头光晕            `subtle lens flare`                  光源附近适度出现

  浅景深                  `shallow depth of field`             适合主体分离

  轻微动态模糊            `subtle motion blur`                 适合运动或抓拍

  轻微暗角                `subtle natural vignetting`          避免过重黑边

  真实反射                `physically plausible reflections`   对产品图尤其重要

  避免过度磨皮            `avoid overly smooth plastic skin`   可用于支持负面提示词的模型

  避免过度锐化            `avoid excessive sharpening`         模型不一定严格遵守
  -----------------------------------------------------------------------------------------

------------------------------------------------------------------------

# 9. 八个完整摄影案例

这些案例是可直接复制的起始模板。应根据模型、画幅、主体和生成结果调整。

## 案例 1：自然日系人像

目标：日常、自然、柔和，不像过度修图的商业广告。

``` text
A candid portrait of a young woman sitting beside a window
in a quiet apartment, medium close-up, eye-level angle,
Contax 645 medium-format film aesthetic, 80mm lens,
soft window light from camera left, Kodak Portra 400
inspired color palette, natural skin texture, delicate
pastel tones, subtle organic film grain, gentle highlight
roll-off, relaxed expression, understated Japanese lifestyle
photography, authentic candid composition.
```

为什么这样组合：

-   80mm：突出人物，减少环境干扰。
-   窗边柔光：让面部阴影自然过渡。
-   Portra 400 风格：引导柔和肤色与色彩。
-   生活方式摄影：避免过度摆拍的商业感。

## 案例 2：暖调夜间街拍

目标：有城市生活气息和胶片感，但不是赛博朋克。

``` text
A candid nighttime portrait of a young woman outside a
small Tokyo bookstore, Leica M6 35mm film camera aesthetic,
35mm lens, warm shop-window light, Kodak Portra 800 inspired
color palette, natural skin tones, subtle film grain,
realistic ambient shadows, muted urban colors, imperfect
candid framing, humanist street photography.
```

关键是暖色店铺光源和自然环境阴影，而不是只写"night photography"。

## 案例 3：高端时尚编辑摄影

目标：精致、克制、品牌感强。

``` text
A high-end fashion editorial portrait of a model wearing
a sculptural black outfit against a warm gray studio
backdrop, Hasselblad X2D medium-format digital photography
aesthetic, 80mm lens, large diffused softbox, subtle rim
lighting, realistic skin texture, refined tonal gradation,
restrained neutral color grading, elegant negative space,
precise styling, luxury fashion magazine photography.
```

重点是受控布光、服装造型和画面秩序。这里不需要强行添加胶片颗粒。

## 案例 4：复古直接闪光街拍

目标：有冲击力、年轻、像早期数码或胶片时尚快照。

``` text
A spontaneous late-night fashion street photograph of
a young man wearing a black leather jacket outside a
convenience store, 35mm film snapshot aesthetic, direct
on-camera flash, Kodak Gold 200 inspired warm colors,
bright foreground subject against a darker urban background,
subtle film grain, candid framing, raw early-2000s street
fashion editorial.
```

重点是正面直闪、明亮主体与暗背景的反差。

## 案例 5：电影感雨夜

目标：有叙事、空间和电影剧照感。

``` text
A cinematic still of a lone woman walking through a
rain-soaked Tokyo alley at midnight, large-format digital
cinema camera aesthetic, anamorphic lens aesthetic, wide
composition, cool blue ambient shadows, restrained red
neon reflections, atmospheric backlight through light mist,
realistic wet pavement reflections, layered foreground
and background, subtle highlight bloom, deep but detailed
shadows, restrained cinematic color grading.
```

重点是环境光源、前后景层次和湿地反射。不要只用"cinematic"代替具体描述。

## 案例 6：高饱和风光

目标：鲜明、浓郁、有旅行杂志感。

``` text
A dramatic mountain lake surrounded by alpine forests
under clear morning sunlight, Fujifilm Velvia 50 slide
film aesthetic, vivid greens, rich blues, strong color
separation, crisp natural textures, controlled highlights,
deep tonal contrast, carefully composed landscape photography,
realistic atmospheric depth, richly saturated but believable
colors.
```

重点是色彩、自然光和空间层次。

## 案例 7：黑白纪实

目标：粗粝、有力量、真实。

``` text
A black-and-white documentary photograph of an elderly
street vendor arranging vegetables before sunrise,
Leica M6 35mm film camera aesthetic, Kodak Tri-X 400
inspired tonal character, directional side lighting,
rich midtones, deep but detailed shadows, visible organic
film grain, natural skin and fabric texture, unposed gesture,
imperfect framing, timeless humanist street photography.
```

重点是灰阶、颗粒、明暗和瞬间感。

## 案例 8：极简奢侈品产品图

目标：材质精细、反射受控、留白高级。

``` text
A minimalist luxury perfume bottle on a matte warm-gray
pedestal, medium-format commercial photography aesthetic,
80mm lens, large diffused softbox above and to camera left,
subtle controlled rim light, precise glass reflections,
clean specular highlights, soft ground shadow, restrained
neutral palette, meticulous material detail, balanced
negative space, premium luxury product campaign.
```

重点是玻璃反射、主光方向和背景材质。相机名称只是辅助。

------------------------------------------------------------------------

# 10. 常见问题诊断表

  ----------------------------------------------------------------------------------------------------------------------
  问题                    优先检查                             可尝试的修改
  ----------------------- ------------------------------------ ---------------------------------------------------------
  皮肤像塑料              过度美化、光线、后期风格             `natural skin texture, minimal retouching`

  人物太扁平              光线方向、拍摄距离、构图             `directional side light, dimensional facial shadows`

  背景太乱                景别、背景元素、景深                 `simple background, shallow depth of field`

  色彩太艳                饱和度、光源、调色                   `muted color palette, restrained saturation`

  画面太干净              构图、颗粒、生活细节                 `candid framing, subtle organic grain`

  颗粒像噪点              颗粒强度和尺度                       `subtle fine film grain`

  电影感不足              光源逻辑、前后景、色彩关系           `motivated lighting, layered depth, restrained grading`

  产品反射混乱            光源大小、位置、材质描述             `controlled softbox reflections, clean highlights`

  背景虚化不足            主体距离、背景距离、焦段和光圈描述   `shallow depth of field, distant background`

  人像过度摆拍            动作、表情、构图                     `candid moment, relaxed posture, natural gesture`

  画面风格混乱            风格词太多或互相矛盾                 保留一个主风格，删掉冲突词

  相机型号没效果          模型是否理解该型号                   改用明确的光线、构图、色彩和质感词
  ----------------------------------------------------------------------------------------------------------------------

这些建议是排查起点，并不保证每个模型都按字面执行。通过对照实验验证最可靠。

------------------------------------------------------------------------

# 11. 如何建立个人实验库

这是最值得长期维护的部分。不要只存提示词，还要存生成结果、模型、参数和评价。

## 11.1 推荐的实验记录字段

  字段         记录内容
  ------------ ------------------------------------
  实验编号     EXP-0001
  日期         生成日期
  模型         GPT Image / Midjourney / Flux 等
  模型版本     尽可能填写准确版本
  实验目标     例如测试胶片对肤色的影响
  固定条件     主体、构图、光线等保持不变的部分
  修改变量     本次只修改了什么
  完整提示词   保存原文
  图片文件名   关联生成图片
  评分         构图、光线、色彩、质感、风格一致性
  观察结果     哪些变化符合预期
  下次计划     下一轮准备测试什么

## 11.2 评分标准

每项 1--5 分：

-   1：明显不符合目标。
-   2：有部分特征，但问题明显。
-   3：基本符合目标，结果一般。
-   4：效果好，只有少量问题。
-   5：高度符合目标，值得加入预设库。

建议评分维度：

1.  主体质量
2.  构图
3.  光线
4.  色彩
5.  质感
6.  风格一致性

不要把单次高分当作定论。尽可能生成多张图，并在同一模型、相近设置下比较。

## 11.3 对照实验示例

实验目标：比较两种胶片描述对同一场景的影响。

固定内容：

-   主体：同一人物。
-   场景：同一家咖啡馆。
-   构图：半身、平视。
-   镜头：50mm。
-   光线：左侧窗光。
-   成片风格：自然人像。

只改变这一项：

A 组：

``` text
Kodak Portra 400 inspired color palette
```

B 组：

``` text
Kodak Portra 800 inspired color palette
```

记录：肤色、色彩、颗粒、整体偏好是否发生变化。

注意：不同模型可能忽略这些差异，因此实验记录应以实际生成结果为准。

------------------------------------------------------------------------

# 12. 可复用的六个风格预设

## 预设 A：自然胶片人像

``` text
Contax 645 medium-format film aesthetic, 80mm lens,
Kodak Portra 400 inspired color palette, soft window light,
natural skin texture, delicate pastel colors, subtle grain,
gentle highlight roll-off, candid portrait photography.
```

## 预设 B：暖调复古快照

``` text
35mm film snapshot aesthetic, Kodak Gold 200 inspired warm
colors, direct afternoon sunlight, candid framing, slight
color fading, natural imperfections, nostalgic everyday
photography.
```

## 预设 C：高端时尚

``` text
Hasselblad X2D medium-format digital photography aesthetic,
80mm lens, large diffused softbox, subtle rim light,
refined skin texture, restrained neutral color grading,
precise styling, luxury fashion editorial.
```

## 预设 D：黑白纪实

``` text
Leica M6 35mm film camera aesthetic, Kodak Tri-X 400
inspired monochrome tones, directional side lighting,
rich midtones, visible organic grain, candid documentary
photography, imperfect framing.
```

## 预设 E：电影雨夜

``` text
Large-format digital cinema camera aesthetic, anamorphic
lens aesthetic, mixed neon lighting, cool blue shadows,
restrained red reflections, atmospheric depth, wet pavement,
subtle highlight bloom, cinematic narrative still.
```

## 预设 F：极简商业产品

``` text
Medium-format commercial photography aesthetic, 80mm lens,
large diffused softbox, controlled reflections, clean
specular highlights, soft ground shadow, neutral background,
meticulous material detail, elegant negative space,
premium minimalist product photography.
```

------------------------------------------------------------------------

# 13. 如何根据不同 AI 模型调整提示词

这份知识库是通用的，但不同模型的工作方式不同。

## GPT Image

优先把场景、主体、构图、光线、材质和修改要求说清楚。对复杂场景，应明确哪些元素必须保留、哪些地方允许变化。相机型号可以作为风格辅助，不应代替清楚的画面描述。

## Midjourney

可以用摄影术语、简洁风格词和明确构图来探索画面。按所用版本使用画幅参数、参考图和
Style Reference 等功能。具体参数应以当前版本的官方文档为准。

## Flux / SDXL

除自然语言描述外，部分工作流还会使用负面提示词、采样器、步数、CFG
等参数。具体效果取决于模型版本、界面和工作流。不要把某一模型的参数经验直接照搬到另一模型。

## 跨模型比较规则

-   保持主体和目标视觉效果相同。
-   尽量使用等价的画幅与生成设置。
-   每个模型分别保存实验记录。
-   不要因为某模型对一个相机名称响应明显，就假设其他模型也会如此。
-   比较多张结果，而不是只比较单张最佳图。

------------------------------------------------------------------------

# 14. 建议的知识库目录结构

如果你准备长期维护，建议采用以下目录：

``` text
AI摄影知识库/
├── README.md
├── 01-基础概念/
│   ├── 提示词总结构.md
│   ├── 构图与景别.md
│   └── 摄影术语速查.md
├── 02-相机与镜头/
│   ├── 相机系统库.md
│   ├── 相机型号索引.md
│   ├── 焦段与透视.md
│   └── 光圈与景深.md
├── 03-胶片与色彩/
│   ├── 彩色胶片库.md
│   ├── 黑白胶片库.md
│   └── 质感与调色词库.md
├── 04-光线/
│   ├── 自然光.md
│   ├── 棚拍布光.md
│   └── 夜景与混合光.md
├── 05-风格预设/
│   ├── 自然人像.md
│   ├── 街头纪实.md
│   ├── 高端时尚.md
│   ├── 电影剧照.md
│   └── 产品摄影.md
├── 06-完整案例/
│   └── 案例集.md
├── 07-实验记录/
│   ├── 实验模板.md
│   └── 实验日志.md
└── 08-模型适配/
    ├── GPT-Image.md
    ├── Midjourney.md
    └── Flux-SDXL.md
```

不必一开始就创建所有文件。可以先把本文件作为总入口，等某个分类内容变多时再拆分。

------------------------------------------------------------------------

# 15. 可复制的实验记录模板

每次测试时复制下面这份模板：

``` markdown
# 实验编号：EXP-0001

## 目标
我想得到什么视觉效果？

## 使用模型
- 模型：
- 版本：
- 画幅：
- 其他生成参数：

## 固定条件
- 主体：
- 场景：
- 构图：
- 光线：
- 风格：

## 本次修改的变量
只改变了什么？

## 完整提示词
```text
在这里粘贴完整提示词
```

## 生成结果

-   图片文件名：
-   结果数量：

## 评分（1--5）

-   主体：
-   构图：
-   光线：
-   色彩：
-   质感：
-   风格一致性：

## 观察

哪些变化符合预期？哪些没有？

## 下次实验

下一轮只修改什么？ \`\`\`

------------------------------------------------------------------------

# 16. 最后：新手应该从哪里开始？

不要试图一次掌握整份知识库。建议按四周推进。

### 第 1 周：掌握构图与光线

-   每天选一个主体。
-   分别测试平视、低机位、近景、全身。
-   比较窗光、逆光、阴天漫射光。
-   不要加入太多相机和胶片词。

### 第 2 周：掌握镜头与景深

-   固定同一个场景。
-   分别尝试 35mm、50mm、85mm。
-   比较环境人像、半身人像和紧凑特写。
-   记录透视和背景关系的变化。

### 第 3 周：掌握胶片与色彩

-   选择 Portra 400、Portra 800、Gold 200 三种风格。
-   固定构图和光线，只替换色彩描述。
-   记录肤色、饱和度、颗粒与整体氛围。

### 第 4 周：建立自己的预设

-   从实验结果中挑出最稳定的 3--6 组组合。
-   为每组保存提示词和代表图片。
-   写明适用场景、缺点和下一次要测试的内容。

## 结论

你真正需要的不是成为专业摄影师，也不是记住所有相机型号。

你需要的是一套从**视觉目标 → 摄影语言 → 提示词组合 → 生成实验 →
经验沉淀**的闭环。

把这份文件作为基础知识库，先学会少量高价值特征，再用实际生成结果验证。随着案例增加，你会逐渐知道哪些术语值得保留、哪些只是听起来专业但对你使用的模型帮助不大。
