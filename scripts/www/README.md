# 潮汐与尘埃 - 深空方舟

一款基于Web的太空生存游戏，融合了《60秒》、《Phigros》等游戏的特色玩法。

## 项目结构

```
潮汐与尘埃/
├── index.html          # 前端游戏界面
├── server.js           # 后端服务器
├── package.json        # 项目配置
├── data/               # 数据存储目录（自动创建）
│   └── users.json      # 用户数据文件
├── music/              # 背景音乐
├── MV/                 # 视频资源
├── noise/              # 音效
└── sound/              # 语音资源
```

## 快速开始

### 1. 安装依赖

```bash
npm install
```

### 2. 启动服务器

```bash
# 开发模式
npm run dev

# 生产模式
npm run prod

# 或直接启动
npm start
```

服务器将在 `http://localhost:3000` 启动。

## 环境变量

- `PORT`: 服务器端口（默认: 3000）
- `NODE_ENV`: 环境模式（development/production）

## 安全注意事项

⚠️ **重要**: 此版本使用简单哈希密码，仅用于演示和开发目的！

生产环境请：
1. 使用 `bcrypt` 或 `argon2` 进行密码哈希
2. 添加 HTTPS 支持
3. 实现适当的速率限制
4. 添加输入验证和清理

## 游戏特色

- 🚀 太空生存玩法
- 👥 船员管理系统
- 💰 资源管理（金币/钻石）
- 📊 排行榜系统
- 🎯 每日签到
- 🏆 成就系统
- 🎮 多种游戏模式

## API 接口

### 用户系统
- `POST /api/register` - 用户注册
- `POST /api/login` - 用户登录
- `POST /api/verify` - Token验证

### 资源管理
- `POST /api/spend-coins` - 金币消耗
- `POST /api/spend-diamonds` - 钻石消耗
- `POST /api/earn-coins` - 金币收入
- `POST /api/earn-diamonds` - 钻石收入

### 游戏统计
- `POST /api/game-played` - 游戏次数统计
- `GET /api/stats` - 用户统计
- `GET /api/leaderboard` - 排行榜

### 其他功能
- `POST /api/signin` - 每日签到
- `GET /api/signin-info` - 签到信息
- `POST /api/claim-activity` - 活动领取
- `POST /api/update-achievement` - 更新成就
- `GET /api/player-data` - 玩家数据

## 开发说明

### 前端架构
- 纯HTML/CSS/JavaScript实现
- 响应式设计，支持移动端和桌面端
- Phigros风格UI设计
- 60秒游戏机制融合

### 后端架构
- Node.js原生HTTP服务器
- 文件系统数据存储
- RESTful API设计
- CORS支持

## 许可证

MIT License

## 贡献

欢迎提交Issue和Pull Request！