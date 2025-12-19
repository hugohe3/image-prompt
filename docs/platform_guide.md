# 🎛️ 平台适配指南

> 本文档提供各主流 AI 图像生成平台的适配建议和格式规范。

---

## 平台概览

| 平台 | 特点 | 推荐场景 |
|------|------|----------|
| **Gemini / Imagen** | 自然语言理解强，支持多语言 | 通用场景，中文描述 |
| **GPT-Image-1.5 / ChatGPT Images** | 自然语言描述，效果出色 | 商业用途，高质量需求 |
| **Midjourney** | 艺术风格强，支持参数调节 | 艺术创作，概念设计 |
| **Stable Diffusion** | 高度可控，支持权重和负面提示 | 专业用户，精细控制 |
| **Ideogram** | 文字生成能力强 | 需要包含文字的图像 |

---

## Gemini / Imagen

### 特点
- 自然语言理解能力强
- 支持中英文混合描述
- 注重场景细节和氛围营造

### 格式建议
```
使用完整的描述性句子，可以像讲故事一样描述场景。
支持中英文，关键词可用英文以提高准确度。
```

### 示例
```
一只橘色的猫咪蜷缩在窗台上晒太阳，阳光透过白色纱帘洒进来，
营造出温暖慵懒的午后氛围。背景是模糊的室内场景，
可以看到绿植和书架。整体风格温馨治愈，像一幅水彩画。
```

或：
```
An orange cat curled up on a windowsill basking in sunlight,
warm afternoon atmosphere, soft daylight filtering through white curtains,
cozy indoor background with plants and bookshelves, watercolor style
```

---

## GPT-Image-1.5 / ChatGPT Images

### 特点
- 自然语言理解能力强
- 图像质量出色
- 支持复杂场景描述

### 格式建议
```
使用完整的英文句子描述
保持描述清晰具体
可以描述复杂的场景和细节
```

### 示例
```
A photorealistic image of a modern coffee shop interior during golden hour.
Warm sunlight streams through large windows, illuminating wooden tables
and comfortable armchairs. A barista is preparing a latte behind
a sleek espresso machine. The atmosphere is cozy and inviting.
```

---

## Midjourney

### 特点
- 艺术风格表现力强
- 支持多种参数调节
- 社区氛围活跃

### 常用参数

| 参数 | 说明 | 示例 |
|------|------|------|
| `--ar` | 宽高比 | `--ar 16:9`, `--ar 1:1`, `--ar 9:16` |
| `--v` | 版本 | `--v 6`, `--v 5.2` |
| `--style` | 风格 | `--style raw` (更真实) |
| `--q` | 质量 | `--q 2` (更高质量，更慢) |
| `--s` | 风格化程度 | `--s 250` (0-1000) |
| `--c` | 混乱度 | `--c 50` (0-100) |
| `--no` | 排除元素 | `--no text, watermark` |

### 格式模板
```
[描述内容] --ar [比例] --style raw --v 6
```

### 示例
```
A serene Japanese garden with a koi pond, cherry blossoms falling,
soft morning mist, traditional wooden bridge, peaceful atmosphere
--ar 16:9 --style raw --v 6
```

```
Portrait of a cyberpunk character with neon makeup, futuristic city background,
dramatic lighting, highly detailed --ar 2:3 --v 6 --s 500
```

---

## Stable Diffusion

### 特点
- 高度可定制
- 支持权重调节
- 支持负面提示词 (Negative Prompt)

### 权重语法

| 语法 | 效果 |
|------|------|
| `(keyword:1.5)` | 增强权重 1.5 倍 |
| `(keyword:0.5)` | 降低权重 0.5 倍 |
| `[keyword]` | 降低权重 |
| `keyword1 AND keyword2` | 融合概念 |

### 格式模板
```
Positive: [正面提示词，用逗号分隔]

Negative: [负面提示词，用逗号分隔]
```

### 示例

**正面提示词：**
```
(masterpiece:1.2), best quality, ultra detailed,
a beautiful sunset over the ocean, golden hour lighting,
dramatic clouds, calm waves, (vibrant colors:1.3),
professional photography, 8K resolution
```

**负面提示词：**
```
lowres, bad anatomy, bad hands, text, error, missing fingers,
extra digit, fewer digits, cropped, worst quality, low quality,
normal quality, jpeg artifacts, signature, watermark, username, blurry
```

### 常用负面提示词模板
```
lowres, bad anatomy, bad hands, text, error, missing fingers,
extra digit, fewer digits, cropped, worst quality, low quality,
jpeg artifacts, signature, watermark, blurry, deformed, disfigured
```

---

## Ideogram

### 特点
- 文字生成能力出色
- 适合需要准确文字的图像
- 支持多种字体风格

### 格式建议
```
描述图像内容，并明确指出需要显示的文字。
使用引号包裹需要生成的文字内容。
```

### 示例
```
A modern minimalist poster design with the text "DREAM BIG" in bold sans-serif font,
gradient background from deep purple to soft pink, clean typography,
professional graphic design style
```

```
A vintage coffee shop sign that says "CAFÉ LUNA" in elegant script font,
warm wooden background, soft lighting, rustic aesthetic
```

---

## 通用版本

当用户未指定平台时，使用通用格式：

### 格式
```
[主体描述], [风格], [环境/背景], [光线], [视角], [质量词]
```

### 示例
```
A majestic lion standing on a rocky cliff at sunset,
photorealistic style, African savanna in the background,
golden hour lighting, low angle shot, highly detailed, 8K quality
```

---

## 平台选择建议

| 需求场景 | 推荐平台 |
|----------|----------|
| 快速出图、自然语言描述 | Gemini, ChatGPT Images |
| 艺术创作、概念设计 | Midjourney |
| 精细控制、批量生成 | Stable Diffusion |
| 包含文字的设计 | Ideogram |
| 中文描述、日常使用 | Gemini |
| 高质量商业用途 | GPT-Image-1.5 |

---

## 跨平台转换技巧

### 从自然语言到 Midjourney
```
原始：一只可爱的柴犬在樱花树下奔跑，春天的氛围，阳光明媚

转换：A cute Shiba Inu running under cherry blossom trees,
spring atmosphere, bright sunny day, joyful mood,
soft pink petals falling --ar 16:9 --v 6
```

### 从 Midjourney 到 Stable Diffusion
```
原始：cyberpunk city street, neon lights, rain --ar 16:9 --v 6

转换：
Positive: (cyberpunk city street:1.2), neon lights, rain, wet pavement,
reflections, night scene, futuristic, highly detailed, 8K

Negative: daytime, sunny, bright, low quality, blurry
```

