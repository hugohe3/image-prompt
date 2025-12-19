# 📖 AI 图像提示词参考指南

> 本文档为 Image Prompt Architect 的配套参考资料，提供详细的选项说明和示例。
> 
> 💡 **使用方式**：配合 [`image-prompt-architect.md`](./image-prompt-architect.md) 一起复制到 ChatGPT / Gemini / Claude 等 Web 版中使用。

---

## 目录

1. [图片类型速查表](#1-图片类型速查表)
2. [视觉风格速查表](#2-视觉风格速查表)
3. [主题成功率评估](#3-主题成功率评估)
4. [光线效果速查表](#4-光线效果速查表)
5. [视角与构图速查表](#5-视角与构图速查表)
6. [镜头类型速查表](#6-镜头类型速查表)
7. [氛围情绪关键词](#7-氛围情绪关键词)
8. [提示词结构模板](#8-提示词结构模板)
9. [常见问题修复](#9-常见问题修复)
10. [避坑指南](#10-避坑指南)

---

## 1. 图片类型速查表

| 类型 | 英文关键词 | 适用场景 | 示例 |
|------|------------|----------|------|
| 照片 | photo, photograph | 产品展示、人物肖像、写实场景 | `photo of a coffee cup on wooden table` |
| 插画 | illustration | 博客配图、儿童读物、概念图 | `illustration of a magical forest` |
| 油画 | oil painting | 艺术创作、装饰画、古典风格 | `oil painting of a countryside landscape` |
| 水彩 | watercolor | 柔和氛围、自然主题、文艺风格 | `watercolor painting of cherry blossoms` |
| 3D渲染 | 3D render | 产品渲染、科技感、游戏资产 | `3D render of a futuristic car` |
| 卡通 | cartoon, anime | 社交媒体、趣味内容、IP形象 | `cartoon character of a friendly robot` |
| 数字艺术 | digital art | 概念设计、游戏海报、科幻主题 | `digital art of an alien cityscape` |
| 素描 | pencil sketch, drawing | 草图展示、极简风格、手绘感 | `pencil sketch of a vintage car` |
| 矢量图 | vector art | Logo、图标、扁平设计 | `vector art of a mountain logo` |
| 像素画 | pixel art | 游戏、复古风格 | `pixel art of a space invader` |

---

## 2. 视觉风格速查表

| 风格 | 英文关键词 | 特征 | 适用场景 |
|------|------------|------|----------|
| 写实 | realistic, photorealistic | 高度写实、细节丰富 | 产品、建筑、人物 |
| 极简 | minimalist | 简洁、留白、克制 | 商务、UI设计 |
| 未来 | futuristic, sci-fi | 科技感、未来元素 | 科技、创新主题 |
| 复古 | vintage, retro | 复古、怀旧质感 | 品牌、时尚、文化 |
| 超现实 | surreal, surrealistic | 梦幻、非现实组合 | 艺术创作、创意广告 |
| 赛博朋克 | cyberpunk | 霓虹、都市、高科技低生活 | 游戏、科幻 |
| 蒸汽朋克 | steampunk | 维多利亚+机械美学 | 奇幻、复古科幻 |
| 电影感 | cinematic | 戏剧性光影、宽银幕构图 | 海报、概念图 |
| 印象派 | impressionist | 光影斑驳、笔触可见 | 艺术、自然风景 |
| 装饰艺术 | art deco | 几何对称、奢华感 | 奢华品牌、建筑 |
| 波普艺术 | pop art | 高对比、鲜艳色彩 | 潮流、广告 |
| 浮世绘 | ukiyo-e | 日式传统版画风格 | 东方主题 |

---

## 3. 主题成功率评估

### ✅ 高成功率主题（训练数据丰富）

| 类别 | 示例 |
|------|------|
| 人物 | 肖像、自拍、职业人物、时尚模特 |
| 动物 | 常见宠物（猫、狗）、野生动物 |
| 风景 | 海滩、山脉、森林、城市天际线 |
| 食物 | 各类美食、咖啡、甜品 |
| 建筑 | 现代建筑、古典建筑、室内设计 |
| 物品 | 电子产品、家具、车辆 |

### ⚠️ 中等成功率主题

| 类别 | 示例 | 建议 |
|------|------|------|
| 特定职业场景 | 手术室、法庭 | 添加更多细节描述 |
| 抽象概念 | 时间、自由 | 用具象元素表达 |
| 复杂交互 | 多人互动场景 | 限制人物数量 |
| 特定历史场景 | 古代战争、历史事件 | 参考知名绘画风格 |

### ❌ 低成功率主题

| 类别 | 示例 | 替代方案 |
|------|------|----------|
| 罕见物种 | 深海鱼类、灭绝动物 | 使用更常见的相似物种 |
| 专业设备 | 医疗仪器、工业机械 | 简化或用通用描述 |
| 特定品牌 | 具体产品型号 | 用通用描述代替 |
| 精确文字 | 带文字的标牌 | 后期添加文字 |

---

## 4. 光线效果速查表

| 光线类型 | 英文关键词 | 视觉效果 | 情绪氛围 | 最佳搭配场景 |
|----------|------------|----------|----------|--------------|
| 黄金时刻 | golden hour | 温暖金色柔光 | 温馨、浪漫、希望 | 户外人像、风景 |
| 蓝调时刻 | blue hour | 冷调蓝紫 | 宁静、神秘、梦幻 | 城市夜景、海边 |
| 柔和日光 | soft daylight | 自然均匀 | 清新、日常、自然 | 产品、室内 |
| 正午强光 | harsh midday sun | 强烈对比、锐利阴影 | 戏剧性、紧张 | 沙漠、街头 |
| 戏剧光影 | dramatic lighting | 明暗对比强烈 | 神秘、电影感 | 人像、产品 |
| 霓虹灯光 | neon lights | 霓虹色彩、赛博感 | 未来、派对、活力 | 城市夜景、科幻 |
| 摄影棚灯 | studio lighting | 专业可控 | 干净、专业 | 产品、人像 |
| 烛光 | candlelight | 暖橙、柔和光点 | 浪漫、复古、私密 | 晚餐、复古场景 |
| 月光 | moonlight | 冷白、神秘 | 静谧、奇幻 | 夜景、奇幻 |
| 逆光 | backlight | 轮廓光、剪影 | 戏剧、唯美 | 人像、日落 |
| 环境光 | ambient light | 自然环境光源 | 真实、沉浸 | 室内、街景 |

---

## 5. 视角与构图速查表

| 视角 | 英文关键词 | 效果 | 适用场景 |
|------|------------|------|----------|
| 平视 | eye level | 自然、亲近 | 人物、日常场景 |
| 仰视 | low angle, worm's eye view | 高大、气势、英雄感 | 建筑、人物、车辆 |
| 俯视 | high angle | 全局、弱化主体 | 场景概览、俯瞰 |
| 鸟瞰 | bird's eye view, top-down | 正俯视、地图感 | 布局、美食摆盘 |
| 特写 | close-up, macro | 聚焦细节、质感 | 产品、表情、纹理 |
| 极特写 | extreme close-up | 局部放大 | 眼睛、材质 |
| 中景 | medium shot | 半身、平衡 | 人物、对话 |
| 全景 | wide shot, full shot | 展现全貌 | 风景、建筑、场景 |
| 过肩 | over-the-shoulder | 视角代入 | 对话、游戏视角 |
| 荷兰角 | Dutch angle | 倾斜、不安 | 悬疑、紧张 |

---

## 6. 镜头类型速查表

| 镜头 | 英文关键词 | 效果 | 适用场景 |
|------|------------|------|----------|
| 标准镜头 | 50mm | 自然视角、人像标准 | 人物肖像 |
| 广角镜头 | wide-angle, 35mm | 视野宽广、空间感 | 风景、室内、街拍 |
| 超广角 | ultra wide-angle, 24mm | 夸张透视 | 建筑、戏剧效果 |
| 鱼眼镜头 | fisheye lens | 夸张变形、球面效果 | 创意、动感 |
| 长焦镜头 | telephoto, 85mm+ | 压缩空间、背景虚化 | 人像、运动 |
| 微距镜头 | macro lens | 微观细节 | 产品、自然、珠宝 |
| 移轴镜头 | tilt-shift | 微缩模型感 | 城市俯瞰、创意 |
| 变形镜头 | anamorphic lens | 电影宽银幕、光晕 | 电影感画面 |

---

## 7. 氛围情绪关键词

| 情绪 | 英文关键词 | 关联视觉元素 |
|------|------------|--------------|
| 宁静 | serene, peaceful, calm | 柔光、自然色、留白、水面 |
| 活力 | energetic, dynamic, vibrant | 高饱和、动态线条、强对比 |
| 神秘 | mysterious, enigmatic | 暗调、阴影、雾气、剪影 |
| 温馨 | warm, cozy, intimate | 暖色调、柔光、木质、布艺 |
| 忧郁 | melancholic, somber | 冷调、雨景、低饱和、灰色 |
| 梦幻 | ethereal, dreamy | 柔焦、光晕、淡彩、朦胧 |
| 戏剧 | dramatic, intense | 强对比、戏剧光线、饱和色 |
| 浪漫 | romantic | 粉色调、柔光、花卉、bokeh |
| 怀旧 | nostalgic, vintage | 褪色、胶片质感、暖黄 |
| 恐怖 | eerie, creepy, horror | 暗色、扭曲、雾气、冷调 |
| 欢快 | cheerful, joyful | 明亮、多彩、阳光 |
| 史诗 | epic, grand | 宽广场景、戏剧光线、低角度 |

---

## 8. 提示词结构模板

### 结构A：主体优先 (Subject-first)
**适用于**：简单直接的主题，主体是绝对焦点
```
[主体] + [状态/动作], [风格], [背景], [光线], [角度]
```
**示例**：
- `A golden retriever running on a beach, realistic, sunset, golden hour lighting, low angle`
- `A red sports car parked on a city street, cinematic, night, neon lights, wide shot`

### 结构B：场景设定 (Scene-setting)
**适用于**：环境氛围为主，主体融入场景
```
[场景/环境], with [主体], [元素1], [元素2], [光线条件]
```
**示例**：
- `An ancient library with tall dusty bookshelves, dimly lit by sunlight filtering through stained-glass windows`
- `A cozy coffee shop interior, with a young woman reading by the window, warm afternoon light`

### 结构C：动作中心 (Action-centric)
**适用于**：强调动态过程、正在发生的事件
```
[主体] + [正在做什么] + in [场景], [细节描述], [风格]
```
**示例**：
- `A chef preparing sushi in a modern kitchen, with fresh ingredients on the counter, realistic`
- `Children playing in autumn leaves in a park, laughing, warm golden hour light`

### 结构D：氛围导向 (Atmospheric)
**适用于**：情绪和感觉优先于具体内容
```
In the [氛围描述], [主体] [状态], surrounded by [环境元素]
```
**示例**：
- `In the soft glow of twilight, an old stone bridge crosses a tranquil river, surrounded by autumn trees`
- `In the misty morning, a lone fisherman stands on a wooden dock, surrounded by calm waters`

### 结构E：技术细节 (Technical)
**适用于**：摄影级专业需求、精确控制效果
```
[镜头] + [图片类型] of [主体], [技术参数], [光线], [角度]
```
**示例**：
- `85mm portrait photo of a young woman, shallow depth of field, natural window light, eye level`
- `Macro photography of a dewdrop on a leaf, extreme detail, soft morning light`

---

## 9. 常见问题修复

| 问题 | 可能原因 | 解决方案 |
|------|----------|----------|
| 某元素没出现 | 权重不足或位置靠后 | 将关键词移到提示词开头 |
| 画面太乱/杂乱 | 元素过多 | 减少到3-4个核心元素 |
| 风格不对 | 描述模糊 | 加入具体风格词或时代/流派参考 |
| 颜色不准 | 未明确指定 | 为每个物体单独指定颜色（如 "a **red** car"） |
| 主体变形 | 训练数据不足 | 换用更常见的主体描述 |
| 文字乱码 | AI 模型限制 | 避免要求生成文字，后期添加 |
| 手指/手部问题 | 模型通病 | 隐藏手部、用物体遮挡或裁切构图 |
| 比例失调 | 描述不清 | 明确大小关系或使用参照物 |
| 背景不符 | 描述过简 | 详细描述背景环境 |
| 光线平淡 | 未指定光线 | 添加具体光线描述词 |

---

## 10. 避坑指南

### 10.1 应避免的关键词类型

| 类型 | ❌ 避免 | ✅ 替代方案 |
|------|---------|-------------|
| 非视觉动词 | think, feel, believe | 用表情/姿态表达情绪 |
| 模糊代词 | it, they, this | 明确指出具体对象 |
| 抽象形容词 | beautiful, nice, good | 具体描述特征（如 "elegant curves"） |
| 否定词 | no, without, not | 直接描述想要的内容 |
| 精确文字 | "写着XXX的标牌" | 后期用设计软件添加 |

### 10.2 平台特定注意事项

| 平台 | 特点 | 提示词建议 |
|------|------|------------|
| Gemini / Imagen | 自然语言，支持多语言 | 使用完整句子，注重细节描述 |
| GPT-Image-1.5 / ChatGPT Images | 效果出色，自然语言理解强 | 使用完整句子描述 |
| Midjourney | 支持参数 | 可添加 `--ar 16:9` `--style raw` 等 |
| Stable Diffusion | 支持权重 | 可使用 `(keyword:1.5)` 调整权重 |
| Ideogram | 文字生成较好 | 适合需要文字的场景 |

---

## 附录：组装公式速查

```
[镜头(可选)] + [图片类型] + of + [风格] + [主体+颜色/材质] + [其他元素] + [背景环境] + [光线条件] + [角度]
```

**示例组装**：
```
Fisheye lens + photo + of + futuristic + a pink sofa and black chairs + a golden retriever on the floor + Mars colony through window + midday lighting + low angle
```

**输出**：
```
Fisheye lens photo of a futuristic room, a pink sofa and black chairs, a golden retriever on the floor, Mars colony visible through the window, midday lighting, low angle
```

