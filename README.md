# MiniMax 图片识别 MCP

使用MiniMax MCP进行AI图片分析和网络搜索。

## 功能特性

- 🖼️ **图片分析** - AI理解图片内容，回答关于图像的问题
- 🌐 **网络搜索** - 执行网络搜索并获取结构化结果
- 🔍 **视觉问答** - 基于图片进行问答交互

## 前置条件

### 1. uvx已安装
```bash
which uvx
# 应该显示：/root/.local/bin/uvx
```

### 2. API Key配置

从MiniMax开放平台获取API Key：
- 国内：https://platform.minimaxi.com/user-center/basic-information/interface-key
- 海外：https://www.minimax.io/platform/user-center/basic-information/interface-key

## MCP服务器配置

编辑 `<workspace>/config/mcporter.json`，添加MiniMax服务器：

```json
{
  "mcpServers": {
    "MiniMax": {
      "command": "uvx",
      "args": ["minimax-coding-plan-mcp", "-y"],
      "env": {
        "MINIMAX_API_KEY": "your-api-key",
        "MINIMAX_API_HOST": "https://api.minimaxi.com"
      }
    }
  }
}
```

## 验证配置

```bash
mcporter list
# 应该显示 MiniMax 服务器
```

## 使用方法

### 图片分析
```bash
mcporter call 'MiniMax.understand_image(imageUrl: "https://example.com/image.jpg", prompt: "描述这张图片")'
```

### 网络搜索
```bash
mcporter call 'MiniMax.web_search(query: "新闻", numResults: 5)'
```

## 查看工具详情
```bash
mcporter list MiniMax --schema
```

## 相关资源

- **MiniMax官网**：https://www.minimax.io
- **MiniMax开放平台**：https://platform.minimaxi.com
- **GitHub**：https://github.com/MiniMax-AI/MiniMax-Coding-Plan-MCP

## License

MIT
