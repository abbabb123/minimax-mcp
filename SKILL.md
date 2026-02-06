---
name: MiniMax图片识别
description: 使用MiniMax MCP进行AI图片分析和网络搜索。通过MiniMax API实现图片理解和网络搜索功能。适用于：图片分析、视觉问答、图像内容提取。
metadata: {"openclaw":{"requires":{"bins":["mcporter"]}}}
---

# MiniMax 图片识别 MCP

使用MiniMax MCP进行AI图片分析和网络搜索。

## 功能特性

- 🖼️ **图片分析** - AI理解图片内容，回答关于图像的问题
- 🌐 **网络搜索** - 执行网络搜索并获取结构化结果
- 🔍 **视觉问答** - 基于图片进行问答交互

## 必要配置

### 1. 安装uvx
```bash
# 安装uv (Python包管理器)
curl -LsSf https://astral.sh/uv/install.sh | sh
```

### 2. 配置mcporter.json

编辑 `<workspace>/config/mcporter.json`，添加MiniMax服务器：

```json
{
  "mcpServers": {
    "MiniMax": {
      "command": "uvx",
      "args": ["minimax-coding-plan-mcp", "-y"],
      "env": {
        "MINIMAX_API_KEY": "your-minimax-api-key",
        "MINIMAX_API_HOST": "https://api.minimaxi.com"
      }
    }
  }
}
```

### 3. 获取API Key

从MiniMax开放平台获取API Key：
- 国内：https://platform.minimaxi.com/user-center/basic-information/interface-key
- 海外：https://www.minimax.io/platform/user-center/basic-information/interface-key

### 4. 验证安装

```bash
mcporter list
# 应该显示 MiniMax 服务器
```

## 使用方法

### 图片分析
```bash
# 分析图片URL
mcporter call 'MiniMax.understand_image(imageUrl: "https://example.com/image.jpg", prompt: "描述这张图片的内容")'

# 分析本地图片
mcporter call 'MiniMax.understand_image(imagePath: "/path/to/image.png", prompt: "这张图片里有什么")'
```

### 网络搜索
```bash
mcporter call 'MiniMax.web_search(query: "大模型最新新闻", numResults: 5)'
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
