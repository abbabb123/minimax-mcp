---
name: MiniMax-kantu
description: 当需要识别图片分析图片内容是使用此skill，适用于：图片分析、视觉问答、图像内容提取。
metadata: {"openclaw":{"requires":{"bins":["mcporter"]}}}
---



## 功能特性

- 🖼️ **图片分析** - AI理解图片内容，回答关于图像的问题
- 🔍 **视觉问答** - 基于图片进行问答交互


## 使用方法

### 图片分析
```bash
# 分析图片URL
mcporter call 'MiniMax.understand_image(imageUrl: "https://example.com/image.jpg", prompt: "描述这张图片的内容")'

# 分析本地图片
mcporter call 'MiniMax.understand_image(imagePath: "/path/to/image.png", prompt: "这张图片里有什么")'
```


## 查看工具详情
```bash
mcporter list MiniMax --schema
```

## 文件结构

```
minimax-mcp/
├── SKILL.md  # Skill说明文档
└── README.md # 使用指南
```

## 相关资源

- **MiniMax官网**：https://www.minimax.io
- **MiniMax开放平台**：https://platform.minimaxi.com
- **GitHub**：https://github.com/MiniMax-AI/MiniMax-Coding-Plan-MCP

## License

MIT
