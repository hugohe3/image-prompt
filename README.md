# Image Prompt Master - AI 图像提示词智能生成系统

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

[English](./README_EN.md) | 中文

一个基于 AI 的智能图像提示词生成系统，通过多角色协作，将用户的创意想法转化为适用于各种 AI 图像生成工具（Gemini、ChatGPT Images、Midjourney、Stable Diffusion 等）的**优化提示词**。

> 🎯 **核心公式**：完美图像 = 好的主题 × 精心设计的提示

---

## 🚀 快速使用指南

### 两种使用方式

#### 方式一：在 AI 编辑器中使用（推荐）

克隆仓库到本地，在 Cursor / VS Code + Copilot / Antigravity 中打开，AI 会自动读取 `AGENTS.md` 并按角色定义工作。

#### 方式二：在 Web 版 AI 中直接使用

将以下文件复制到 ChatGPT / Gemini / Claude 等 Web 版中：

| 文件 | 用途 | 使用方式 |
|------|------|----------|
| [`image-prompt-architect.md`](./image-prompt-architect.md) | 系统提示词 | 复制全文到对话开头，让 AI 扮演提示词架构师 |
| [`image-prompt-reference-guide.md`](./image-prompt-reference-guide.md) | 速查参考 | 配合上面使用，提供详细的选项和模板 |

### 输出格式

本系统生成的是 **Markdown 格式的优化提示词**，你可以：

1. 📋 **复制到 Web 平台使用** - 将提示词粘贴到任意 AI 图像生成平台
2. 📁 **保存到 projects/ 目录** - 方便管理和复用
3. 🔌 **通过 MCP 直接生成** - 如果环境支持图像生成 MCP 工具，可直接调用生成图片

### 推荐的图像生成平台

| 平台 | 推荐度 | 特点 |
|------|:------:|------|
| **[Gemini](https://gemini.google.com/)** | ⭐⭐⭐ | 免费、支持中文、效果出色 |
| **[ChatGPT Images](https://chat.openai.com/)** | ⭐⭐⭐ | GPT-Image-1.5 效果优秀 |
| [Midjourney](https://www.midjourney.com/) | ⭐⭐ | 艺术风格强，需付费 |
| [Stable Diffusion](https://stability.ai/) | ⭐⭐ | 开源可控，本地部署 |
| [Ideogram](https://ideogram.ai/) | ⭐⭐ | 文字生成能力强 |

### 三步开始

```
1️⃣ 克隆仓库
   git clone https://github.com/your-username/image-prompt.git

2️⃣ 在 AI 编辑器中打开仓库
   使用 Cursor / VS Code + Copilot / Antigravity 等打开项目

3️⃣ 开始对话，获取优化提示词
   描述你想要的图像 → AI 引导确认需求 → 获得多版本提示词
   → 复制到上述图像生成平台使用
```

### 使用示例

```
用户：我想生成一张未来城市的概念图

AI（Strategist 角色）：
我理解您想要：生成一张未来城市的概念图

为了生成最佳提示词，请确认以下几点：

1. 图片类型
   - A) digital art（推荐 ✓）
   - B) 3D render
   - C) illustration
   - D) 其他：请说明

2. 视觉风格
   - A) futuristic（推荐 ✓）
   - B) cyberpunk
   - C) minimalist
   ...

用户：A, B

AI（Prompt_Architect 角色）：
📋 需求摘要
| 项目 | 确认结果 |
|------|----------|
| 主体 | 未来城市 |
| 图片类型 | digital art |
| 视觉风格 | cyberpunk |
...

🎨 优化提示词

**基础版**
Digital art of a futuristic cyberpunk city, neon lights, flying vehicles

**增强版**
Digital art of a sprawling futuristic cyberpunk metropolis at night,
towering skyscrapers with holographic billboards, flying vehicles,
neon lights reflecting on wet streets, atmospheric fog

**专业版**
...
```

💡 **使用方式**：将生成的提示词复制到 [Gemini](https://gemini.google.com/) 或 [ChatGPT](https://chat.openai.com/) 即可生成图片

---

## 📚 文档导航

| 文档 | 说明 |
|------|------|
| 🎭 [角色系统](./roles/README.md) | 了解 Strategist 和 Prompt_Architect 角色 |
| 📖 [参考指南](./docs/reference_guide.md) | 图片类型、风格、光线等速查表 |
| 🎯 [提示词模板](./docs/prompt_templates.md) | 5 种结构模板和组装公式 |
| 🎛️ [平台适配](./docs/platform_guide.md) | 各平台格式和参数指南 |
| 💡 [示例](./examples/README.md) | 实际生成效果展示 |

---

## 🎭 核心角色

> 系统包含 2 个专业角色，分工明确

### 1️⃣ Strategist (策略师)

**职责**：接收用户初步想法，通过结构化问答引导明确需求

**核心能力**：
- **意图理解**：快速复述用户的核心需求
- **难度评估**：基于 AI 训练数据评估主题成功率
- **结构化提问**：从 7 大维度提出确认问题
  - 图片类型、视觉风格、场景环境
  - 光线氛围、视角构图、色彩倾向、目标平台
- **智能推荐**：每个选项都标注专业建议

📄 [查看完整角色定义](./roles/Strategist.md)

### 2️⃣ Prompt_Architect (提示词架构师)

**职责**：根据确认的需求，生成多版本优化提示词

**核心能力**：
- **多版本输出**：基础版（15-25词）、增强版（30-50词）、专业版（50-80词）
- **平台适配**：Gemini、ChatGPT Images、Midjourney、Stable Diffusion 专属格式
- **5 种结构模板**：主体优先、场景设定、动作中心、氛围导向、技术细节
- **迭代优化**：根据生成结果反馈持续改进

📄 [查看完整角色定义](./roles/Prompt_Architect.md)

---

## 🔄 工作流程

```
用户描述初步想法
       │
       ▼
┌─────────────────────────────────┐
│  Strategist (策略师)             │
│  • 复述用户意图                  │
│  • 评估主题难度                  │
│  • 提出 3-5 个确认问题           │
│  • 提供选项和专业建议            │
└─────────────────────────────────┘
       │
       ▼ 用户确认完成
       │
┌─────────────────────────────────┐
│  Prompt_Architect (提示词架构师) │
│  • 生成需求摘要表                │
│  • 输出基础版/增强版/专业版      │
│  • 提供平台适配版本              │
│  • 支持迭代优化                  │
└─────────────────────────────────┘
       │
       ▼
  多版本优化 Prompt（Markdown 格式）
       │
       ├──→ 复制到 Web 图像生成平台使用
       │
       └──→ 如有 MCP 工具，可直接生成图片
```

---

## 📂 项目结构

```
image-prompt/
├── AGENTS.md                     # 智能体调用规范
├── README.md                     # 项目说明（本文件）
├── .gitignore                    # Git 忽略规则
├── roles/                        # 角色定义
│   ├── README.md                 # 角色概览
│   ├── Strategist.md             # 策略师角色
│   └── Prompt_Architect.md       # 提示词架构师角色
├── docs/                         # 参考文档
│   ├── reference_guide.md        # 完整参考指南（速查表）
│   ├── prompt_templates.md       # 提示词结构模板
│   └── platform_guide.md         # 平台适配指南
├── examples/                     # 使用示例说明
│   └── README.md                 # 示例索引
├── templates/                    # 模板库（参考示例）
│   ├── README.md                 # 模板说明
│   └── example_cat_portrait/     # 示例：猫咪肖像
│       └── prompt.md
├── projects/                     # 用户项目（存放生成的提示词）
│   ├── .gitkeep                  # 目录说明
│   └── YYYYMMDD_主题名称/        # 每次生成创建独立文件夹
│       ├── prompt.md             # 提示词文档
│       └── images/               # 生成的图片（可选）
│
│── 📋 Web 版直接使用的参考文档
├── image-prompt-architect.md     # 系统提示词（复制到 ChatGPT/Gemini 使用）
└── image-prompt-reference-guide.md # 速查参考（配合上面文件使用）
```

---

## 🎯 支持的 AI 图像生成平台

| 平台 | 特点 | 适用场景 |
|------|------|----------|
| **Gemini / Imagen** | 自然语言强，支持中文 | 通用场景 |
| **GPT-Image-1.5 / ChatGPT Images** | 效果出色，简洁易用 | 商业用途 |
| **Midjourney** | 艺术风格强 | 艺术创作 |
| **Stable Diffusion** | 高度可控 | 专业用户 |
| **Ideogram** | 文字生成强 | 含文字设计 |

---

## 💡 最佳实践

### 描述技巧

1. **具体胜于抽象** - 用 "vibrant orange sunset" 而非 "beautiful sunset"
2. **避免否定词** - 用 "empty street" 而非 "no people"
3. **前置重要元素** - 将最重要的描述放在开头
4. **限制元素数量** - 控制在 3-5 个核心元素

### 迭代优化

| 问题 | 解决方案 |
|------|----------|
| 某元素没出现 | 将关键词前置或增加权重 |
| 画面太乱 | 减少元素至 3-4 个 |
| 风格不对 | 加入具体风格参考词 |
| 颜色不准 | 为每个物体明确指定颜色 |

---

## ❓ 常见问题

<details>
<summary><b>Q: 如何让 AI 自动使用这些角色？</b></summary>

A: 克隆仓库后，在 AI 编辑器（Cursor/Antigravity）中打开项目，AI 会自动读取 roles/ 目录中的角色定义。直接在聊天窗口描述你的需求即可。

</details>

<details>
<summary><b>Q: 可以只用中文描述吗？</b></summary>

A: 可以！Strategist 支持中文对话。最终生成的提示词建议使用英文，因为大多数 AI 图像生成工具对英文支持更好。

</details>

<details>
<summary><b>Q: 生成的提示词可以直接使用吗？</b></summary>

A: 是的！Prompt_Architect 会根据你指定的平台输出适配格式，可以直接复制到对应平台使用。

</details>

---

## 🤝 贡献指南

欢迎贡献！你可以：

- 🎨 添加新的风格模板
- 📊 扩展参考指南
- 📝 完善文档
- 💡 分享你的提示词示例

### 如何贡献

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

---

## 📄 开源协议

本项目采用 [MIT License](LICENSE) 开源协议。

---

## 🙏 致谢

- 所有 AI 图像生成平台的开发者
- 社区贡献的提示词技巧和模板

---

Made with ❤️ for AI Art Creators

[⬆ 回到顶部](#image-prompt-master---ai-图像提示词智能生成系统)

