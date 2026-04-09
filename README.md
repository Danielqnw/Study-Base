# 个人技术知识画像库

一个系统化记录技术学习深度与广度的个人知识库。配合 AI（Claude / Cursor）进行对话式学习，自动追踪每个方向的掌握情况，构建持续演进的技术能力画像。

> **理念**：不赶进度，每个概念掰开揉碎弄懂。面试、工作、技术分享都是知识画像的自然输出。

---

## 我的技术画像

| 方向 | 知识点 | 掌握进度 | 状态 | 入口 |
|------|--------|----------|------|------|
| **.NET Core** | 52 | 0% | 学习中 | [`tracks/dotnet-core/`](tracks/dotnet-core/) |
| **前端开发** | 68 | 0% | 学习中 | [`tracks/frontend/`](tracks/frontend/) |
| **CFP 理财规划师** | 73 | 82% | 已完成 | [`tracks/cfp/`](tracks/cfp/) |

---

## 仓库结构

```
Study-Base/
├── CLAUDE.md                    # AI 学习伙伴指令（教学框架 + 方向调度）
├── PROFILE.md                   # 我的学习者画像（偏好、习惯、优缺点）
├── README.md                    # 本文件
│
├── templates/                   # 共享模板
│   ├── GUIDE-TEMPLATE.md        # 新方向指南模板
│   ├── TRACKER-TEMPLATE.md      # 新方向掌握度追踪模板
│   └── SESSION-TEMPLATE.md      # 学习会话记录模板
│
└── tracks/                      # 各学习方向（核心）
    ├── dotnet-core/             # .NET Core 技术体系
    │   ├── GUIDE.md             # 知识领域、模块定义、学习路径
    │   ├── tracker.md           # 掌握度追踪（AI 自动维护）
    │   └── sessions/            # 按日期的学习会话记录
    │       └── YYYY-MM-DD/
    │           └── session-notes.md
    │
    ├── frontend/                # 前端开发技术体系
    │   ├── GUIDE.md
    │   ├── tracker.md
    │   └── sessions/
    │
    └── cfp/                     # CFP 理财规划师（存档）
        ├── GUIDE.md
        ├── tracker.md
        └── sessions/
```

---

## 使用方式

### 日常学习

1. 在此仓库中打开 Cursor / Claude Code
2. 直接提问，AI 会自动识别你在学哪个方向：
   - "给我讲讲 .NET Core 的中间件管道" → 自动进入 .NET Core 方向
   - "React 的 useEffect 到底怎么工作的？" → 自动进入前端方向
   - "今天想学前端" → 明确切换方向
3. AI 会用"掰开揉碎"的方式深入讲解，不赶进度
4. 每次会话结束后，AI 自动记录学习内容并更新掌握度

### 查看我的知识画像

- **某个方向的掌握情况**：打开 `tracks/<方向>/tracker.md`
- **所有方向的整体画像**：问 AI "我的知识画像整体情况怎么样？"
- **某个知识点的学习历程**：翻看 `tracks/<方向>/sessions/` 下的会话记录

### 复习与自测

```
"复习我之前标注的薄弱环节"
"我今天该重点看哪个模块？"
"模拟一场 .NET Core 技术面试"
"考考我 React Hooks 的知识"
```

---

## 新增一个学习方向

想要添加新方向（如系统设计、Go 语言、DevOps 等）？只需 4 步：

1. 创建文件夹 `tracks/<方向名>/sessions/`
2. 复制 `templates/GUIDE-TEMPLATE.md` → `tracks/<方向名>/GUIDE.md`，填入知识体系
3. 复制 `templates/TRACKER-TEMPLATE.md` → `tracks/<方向名>/tracker.md`，填入知识点
4. 在 `CLAUDE.md` 的"当前学习方向"表格中添加一行

或者直接告诉 AI："帮我创建一个 Go 语言方向"，它会自动完成上述步骤。

---

## 教学理念

- **掰开揉碎**：每个概念讲透再往下走，不赶进度
- **先直觉后原理**：先用类比建立感性认识，再逐步深入底层机制
- **对比已有经验**：主动关联你已经会的技术，降低理解成本
- **验证真懂**：讲完后用变体问题检验，不是"听懂了"就算掌握
- **记录一切**：每次学习自动生成会话记录和掌握度更新，形成可追溯的知识成长轨迹

---

## 各方向知识体系概览

### .NET Core（8 大模块，52 知识点）

| 模块 | 主题 | 重要性 |
|------|------|--------|
| A | C# 语言核心（async/await、LINQ、泛型、委托） | 核心 |
| B | .NET Core 运行时与框架（DI、配置、Host） | 核心 |
| C | ASP.NET Core Web 开发（中间件、路由、Controller） | 核心 |
| D | 数据访问（EF Core、Repository 模式、Dapper） | 重要 |
| E | 认证与安全（JWT、Identity、OAuth） | 重要 |
| F | 架构设计与设计模式（SOLID、Clean Architecture、CQRS） | 重要 |
| G | 测试（xUnit、Moq、集成测试） | 进阶 |
| H | 性能、部署与工具（缓存、Docker、CI/CD） | 进阶 |

### 前端开发（8 大模块，68 知识点）

| 模块 | 主题 | 重要性 |
|------|------|--------|
| A | HTML / CSS 基础与进阶 | 基础 |
| B | JavaScript 核心（闭包、原型链、this、Event Loop） | 核心 |
| C | 框架 — React（Hooks、虚拟 DOM、状态管理） | 核心 |
| D | 浏览器原理与网络（渲染流程、HTTP、跨域） | 核心 |
| E | 前端工程化（Webpack/Vite、TypeScript、CI/CD） | 重要 |
| F | 性能优化（Core Web Vitals、代码分割、缓存） | 重要 |
| G | 算法与数据结构（前端向 LeetCode 高频题） | 进阶 |
| H | 综合能力与软技能（系统设计、项目表述） | 进阶 |
