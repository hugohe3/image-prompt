# 🎯 提示词结构模板

> 本文档提供多种提示词结构模板，帮助快速组装高质量的图像提示词。

---

## 核心公式

```
完美图像 = 好的主题 × 精心设计的提示
```

---

## 通用组装公式

```
[镜头(可选)] + [图片类型] + of + [风格] + [主体+颜色/材质] + [其他元素] + [背景环境] + [光线条件] + [角度]
```

---

## 结构模板

### 结构A：主体优先 (Subject-first)

**适用于**：简单直接的主题，主体是绝对焦点

**公式**：
```
[主体] + [状态/动作], [风格], [背景], [光线], [角度]
```

**示例**：
```
A golden retriever running on a beach, realistic, sunset, golden hour lighting, low angle
```
```
A red sports car parked on a city street, cinematic, night, neon lights, wide shot
```
```
An elderly man reading a book, oil painting style, cozy library, warm candlelight, medium shot
```

---

### 结构B：场景设定 (Scene-setting)

**适用于**：环境氛围为主，主体融入场景

**公式**：
```
[场景/环境], with [主体], [元素1], [元素2], [光线条件]
```

**示例**：
```
An ancient library with tall dusty bookshelves, dimly lit by sunlight filtering through stained-glass windows
```
```
A cozy coffee shop interior, with a young woman reading by the window, warm afternoon light
```
```
A futuristic space station corridor, with floating holographic displays, blue ambient lighting
```

---

### 结构C：动作中心 (Action-centric)

**适用于**：强调动态过程、正在发生的事件

**公式**：
```
[主体] + [正在做什么] + in [场景], [细节描述], [风格]
```

**示例**：
```
A chef preparing sushi in a modern kitchen, with fresh ingredients on the counter, realistic
```
```
Children playing in autumn leaves in a park, laughing, warm golden hour light
```
```
A dancer leaping through the air in an empty studio, dramatic spotlight, black and white photography
```

---

### 结构D：氛围导向 (Atmospheric)

**适用于**：情绪和感觉优先于具体内容

**公式**：
```
In the [氛围描述], [主体] [状态], surrounded by [环境元素]
```

**示例**：
```
In the soft glow of twilight, an old stone bridge crosses a tranquil river, surrounded by autumn trees
```
```
In the misty morning, a lone fisherman stands on a wooden dock, surrounded by calm waters
```
```
In the ethereal moonlight, a white fox sits on a snow-covered hill, surrounded by falling snowflakes
```

---

### 结构E：技术细节 (Technical)

**适用于**：摄影级专业需求、精确控制效果

**公式**：
```
[镜头] + [图片类型] of [主体], [技术参数], [光线], [角度]
```

**示例**：
```
85mm portrait photo of a young woman, shallow depth of field, natural window light, eye level
```
```
Macro photography of a dewdrop on a leaf, extreme detail, soft morning light
```
```
Wide-angle architectural photo of a modern skyscraper, leading lines, blue hour, low angle
```

---

## 组装实例

### 实例1：产品摄影

**需求**：一双运动鞋的产品照

**组装**：
```
镜头: macro lens
图片类型: product photo
主体: white running shoes with neon green accents
背景: clean white studio background
光线: soft studio lighting
角度: 45-degree angle
```

**输出**：
```
Macro lens product photo of white running shoes with neon green accents, clean white studio background, soft studio lighting, 45-degree angle, highly detailed
```

---

### 实例2：概念艺术

**需求**：一座未来城市的概念图

**组装**：
```
图片类型: digital art
风格: futuristic, cyberpunk
主体: a massive metropolis with flying vehicles
元素: holographic billboards, neon signs
背景: dark cloudy sky
光线: neon lights, volumetric fog
角度: wide shot, bird's eye view
```

**输出**：
```
Digital art of a futuristic cyberpunk metropolis with flying vehicles, holographic billboards and neon signs everywhere, dark cloudy sky, neon lights with volumetric fog, wide shot bird's eye view
```

---

### 实例3：人物肖像

**需求**：一位年轻女性的艺术肖像

**组装**：
```
镜头: 85mm
图片类型: portrait photo
主体: a young woman with freckles
状态: looking directly at camera, slight smile
光线: golden hour, backlit
角度: eye level, close-up
```

**输出**：
```
85mm portrait photo of a young woman with freckles, looking directly at camera with a slight smile, golden hour backlit, eye level close-up, shallow depth of field
```

---

## 质量增强词

在任何提示词末尾添加以下词汇可提升整体质量：

### 通用质量词
- `highly detailed`
- `sharp focus`
- `professional`
- `masterpiece`
- `award-winning`

### 摄影质量词
- `8K resolution`
- `DSLR quality`
- `sharp focus`
- `bokeh background`
- `professional photography`

### 艺术质量词
- `trending on artstation`
- `concept art`
- `digital painting`
- `highly detailed illustration`
- `masterpiece`

---

## 常见错误与修正

| 错误写法 | 问题 | 正确写法 |
|----------|------|----------|
| `a beautiful sunset` | "beautiful"太抽象 | `a vibrant orange and pink sunset with scattered clouds` |
| `a nice house` | "nice"无视觉意义 | `a modern two-story house with large windows and a green lawn` |
| `no people in the scene` | 否定词无效 | `an empty street, abandoned atmosphere` |
| `it looks peaceful` | "it"指代不明 | `a peaceful lakeside scene` |

