# Black God - 开源 AI Agent 框架

## 🚀 简介
Black God 是一个高性能、可扩展的 AI Agent 框架，支持多模型、多工具、自进化能力。

## ✨ 核心特性
1. **多模型支持** - OpenAI, Claude, Gemini, 本地模型
2. **工具调用** - 内置 50+ 工具，支持自定义扩展
3. **自进化系统** - 根据使用情况自动优化和扩展能力
4. **记忆系统** - 短期/长期记忆，用户偏好学习
5. **优化内核** - 8层优化架构，提升响应速度和准确性

## 🏗️ 架构
```
┌─────────────────────────────────────────┐
│            User Interface               │
│  (Web/iOS/Android/CLI/API)              │
├─────────────────────────────────────────┤
│            Agent Kernel                 │
│  (推理/决策/工具调用/记忆)               │
├─────────────────────────────────────────┤
│            Core Modules                 │
│  • Optimizer (优化器)                   │
│  • SelfEvolving (自进化)                │
│  • MemoryEngine (记忆引擎)              │
│  • ToolOrchestrator (工具编排)          │
├─────────────────────────────────────────┤
│            External Services            │
│  • AI Models (模型服务)                 │
│  • APIs (第三方API)                     │
│  • Databases (数据库)                   │
└─────────────────────────────────────────┘
```

## 📦 快速开始

### 安装
```bash
git clone https://github.com/BlackGod-B/Blackgod.git
cd Blackgod
pip install -r requirements.txt
```

### 配置
```bash
cp .env.example .env
# 编辑 .env 文件，填入你的 API 密钥
```

### 运行
```bash
# Web 界面
python server/server.py

# 或使用 Docker
docker-compose up
```

## 🔧 核心模块

### 1. Agent Kernel (`server/core/agent_kernel.py`)
核心推理引擎，支持：
- 多轮对话
- 工具调用
- 记忆管理
- 错误处理

### 2. Optimizer (`server/core/optimizer.py`)
8层优化架构：
1. 多轮对话记忆
2. 自我反思纠正
3. 智能任务分解
4. 学习和模式识别
5. 动态难度自适应
6. 性能监控增强
7. Extended Thinking
8. 多策略智能路由

### 3. Self Evolving (`server/core/self_evolving.py`)
自进化系统：
- 自动学习用户偏好
- 动态扩展技能
- 性能持续优化

### 4. Tool System (`server/core/tool_orchestrator.py`)
工具管理系统：
- 内置工具：文件操作、网络请求、数据分析等
- 自定义工具：支持 Python 函数注册
- 工具编排：智能组合多个工具

## 🌐 部署

### Docker 部署
```yaml
# docker-compose.yml
version: '3.8'
services:
  blackgod:
    build: .
    ports:
      - "8000:8000"
    environment:
      - OPENAI_API_KEY=${OPENAI_API_KEY}
```

### Cloudflare Workers
```bash
# 部署到 Cloudflare Workers
wrangler deploy
```

## 📚 文档
- [架构设计](./docs/ARCHITECTURE.md)
- [API 参考](./docs/API.md)
- [工具开发指南](./docs/TOOL_DEVELOPMENT.md)
- [部署指南](./docs/DEPLOYMENT.md)

## 🤝 贡献
欢迎提交 Issue 和 Pull Request！

1. Fork 项目
2. 创建功能分支
3. 提交更改
4. 推送到分支
5. 创建 Pull Request

## 📄 许可证
MIT License - 详见 [LICENSE](./LICENSE)

## 🏆 致谢
感谢所有贡献者和用户的支持！

---
**Black God** - 让 AI 更智能，让开发更简单