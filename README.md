# Grok 3.0 API

一个基于 Flask 和 Socket.IO 的现代化实时聊天应用，集成了 xAI 的 Grok 3.0 API 和 Live Search 功能。

[![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy)

## ✨ 功能特点

- 🤖 **Grok 3.0 AI 对话** - 集成最新的 xAI Grok 3.0 API
- 🔍 **Live Search 实时搜索** - 获取来自 X、网页、新闻和 RSS 源的最新信息
- 💬 **实时聊天界面** - 基于 WebSocket 的流畅对话体验
- 📱 **响应式设计** - 完美支持桌面端和移动端
- 🗂️ **会话历史管理** - 自动保存和管理对话历史
- 🔄 **自动重连机制** - 网络断开时自动重新连接
- 🎨 **现代化 UI** - 深色主题，优雅的用户界面
- ☁️ **云端部署优化** - 针对 Render、Heroku 等云平台优化

## 🔍 xAI Live Search 功能

本应用集成了 xAI 的 Live Search API，提供以下特性：

- **🧠 自动搜索决策** - Grok 根据对话上下文自动判断是否需要进行实时搜索
- **🌐 多样化数据源** - 支持从 X 平台、网页、新闻和 RSS 源获取信息
- **⚡ 实时信息** - 获取最新的24小时内的信息
- **🔗 智能集成** - 搜索结果自动整合到对话回复中

> **注意**: Live Search 功能目前处于免费公开测试阶段（截止到2025年6月5日）

## 🚀 快速开始

### 本地开发

1. **克隆仓库**
```bash
git clone https://github.com/ink1ing/grok3.0-api.git
cd grok3.0-api
```

2. **安装依赖**
```bash
pip install -r requirements.txt
```

3. **配置环境变量**
```bash
cp .env.example .env
# 编辑 .env 文件，添加您的配置
```

4. **启动应用**
```bash
python chat.py
```

应用将在 http://localhost:10000 启动

## 📋 环境变量配置

在 `.env` 文件中配置以下变量：

```env
# xAI API 配置
XAI_API_KEY=your-xai-api-key-here
API_URL=https://api.x.ai/v1/chat/completions
MODEL_NAME=grok-3-fast-latest
TEMPERATURE=0

# 应用配置
SECRET_KEY=your-secret-key-change-this-in-production
PORT=10000
DEBUG=False
```

## 🌐 部署

### Render 部署

点击上方的 "Deploy to Render" 按钮，或者：

1. Fork 这个仓库
2. 在 Render 中创建新的 Web Service
3. 连接您的 GitHub 仓库
4. 设置环境变量
5. 部署

### 手动部署

应用支持多种部署方式：

- **Render**: 使用 `render.yaml` 配置
- **Heroku**: 使用 `Procfile` 配置
- **Docker**: 支持容器化部署
- **传统服务器**: 使用 Gunicorn + Nginx

## 🛠️ 技术栈

- **后端**: Flask + Flask-SocketIO
- **前端**: HTML5 + CSS3 + JavaScript
- **实时通信**: WebSocket (Socket.IO)
- **AI API**: xAI Grok 3.0
- **部署**: Gunicorn + Eventlet

## 📁 项目结构

```
grok3.0-api/
├── chat.py              # 主应用文件
├── templates/
│   └── index.html       # 前端界面
├── requirements.txt     # Python 依赖
├── .env.example        # 环境变量示例
├── Procfile            # Heroku 部署配置
├── render.yaml         # Render 部署配置
└── README.md           # 项目说明
```

## 🔧 开发指南

### 添加新功能

1. 在 `chat.py` 中添加后端逻辑
2. 在 `templates/index.html` 中添加前端界面
3. 使用 Socket.IO 进行实时通信

### 调试模式

设置环境变量 `DEBUG=True` 启用调试模式，获取详细的日志信息。

## 📝 更新日志

### v1.2.0 (最新)
- 优化 Socket.IO 连接稳定性
- 改进错误处理和日志记录
- 增强移动端适配
- 添加连接状态检查

### v1.1.0
- 集成 xAI Live Search 功能
- 优化会话历史管理
- 改进 UI/UX 设计

### v1.0.0
- 基础聊天功能
- Grok 3.0 API 集成
- 响应式设计

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

## 📄 许可证

MIT License - 详见 [LICENSE](LICENSE) 文件

## 🔗 相关链接

- [xAI API 文档](https://docs.x.ai/)
- [Flask-SocketIO 文档](https://flask-socketio.readthedocs.io/)
- [Render 部署指南](https://render.com/docs)

---

如有问题，请提交 Issue 或联系开发者。