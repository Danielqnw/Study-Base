# .NET Core 技术体系 — 掌握度追踪

**Last Updated**: 2026-04-09
**Overall Progress**: 0% (0/52 topics)
**Knowledge Depth**: Not Started

---

## 当前目标

> 设定一个短期目标后，学习策略会围绕该目标调整（优先讲哪些模块、讲到什么深度、是否侧重实战或原理）。
> 没有短期目标时，按"系统化深度掌握"的总定位推进。

| 字段 | 内容 |
|------|------|
| **短期目标** | *未设定* |
| **目标描述** | — |
| **目标期限** | — |
| **对学习策略的影响** | 按总定位：系统化深度掌握，不赶进度 |

**历史目标记录**：

| 目标 | 设定日期 | 完成/取消日期 | 结果 |
|------|----------|---------------|------|
| （暂无） | — | — | — |

---

## Quick Stats

| 指标 | 数值 |
|------|------|
| 总知识点 | 52 |
| 已掌握（High） | 0 |
| 部分掌握（Medium） | 0 |
| 待学习 | 52 |
| 知识盲区（未解决） | 0 |
| 已完成学习会话 | 0 |

---

## 模块进度总览

| 模块 | 主题 | 知识点数 | 已掌握 | 进度 | 重要性 |
|------|------|----------|--------|------|--------|
| A | C# 语言核心 | 10 | 0 | 0% | 核心 |
| B | .NET Core 运行时与框架 | 8 | 0 | 0% | 核心 |
| C | ASP.NET Core Web 开发 | 12 | 0 | 0% | 核心 |
| D | 数据访问 | 11 | 0 | 0% | 重要 |
| E | 认证与安全 | 10 | 0 | 0% | 重要 |
| F | 架构设计与设计模式 | 9 | 0 | 0% | 重要 |
| G | 测试 | 7 | 0 | 0% | 进阶 |
| H | 性能、部署与工具 | 10 | 0 | 0% | 进阶 |

---

## 模块 A：C# 语言核心

| ID | 知识点 | 掌握度 | 最后学习日期 | 备注 |
|----|--------|--------|--------------|------|
| A.1 | async/await 底层原理（状态机、Task、ValueTask） | 待学习 | — | |
| A.2 | TPL（Task.Run、Parallel.ForEach、CancellationToken） | 待学习 | — | |
| A.3 | LINQ（延迟执行、表达式树、IEnumerable vs IQueryable） | 待学习 | — | |
| A.4 | 泛型（约束、协变/逆变） | 待学习 | — | |
| A.5 | 委托、事件、Func/Action/Predicate | 待学习 | — | |
| A.6 | 值类型 vs 引用类型（装箱拆箱、栈 vs 堆） | 待学习 | — | |
| A.7 | struct vs class（使用场景） | 待学习 | — | |
| A.8 | 现代 C# 特性（record、pattern matching、nullable、required） | 待学习 | — | |
| A.9 | 内存管理（GC、IDisposable、using、Span<T>） | 待学习 | — | |
| A.10 | 扩展方法、表达式体成员、元组 | 待学习 | — | |

**掌握度说明**：`高` / `中` / `待复习` / `待学习`

---

## 模块 B：.NET Core 运行时与框架

| ID | 知识点 | 掌握度 | 最后学习日期 | 备注 |
|----|--------|--------|--------------|------|
| B.1 | .NET Core vs .NET Framework 核心差异 | 待学习 | — | 有 .NET Framework 背景，重点看差异 |
| B.2 | .NET 版本策略（.NET 5/6/7/8，LTS vs 非LTS） | 待学习 | — | |
| B.3 | Generic Host（IHost、IHostBuilder）与生命周期 | 待学习 | — | 对比 Global.asax |
| B.4 | Program.cs 和 Startup.cs 演进（.NET 6+ 最小化托管） | 待学习 | — | |
| B.5 | 配置系统（appsettings.json、环境变量、IConfiguration） | 待学习 | — | 对比 web.config |
| B.6 | 内置日志系统（ILogger<T>、日志级别、Provider） | 待学习 | — | |
| B.7 | 依赖注入（IServiceCollection、服务生命周期） | 待学习 | — | 面试必考 |
| B.8 | Singleton/Scoped/Transient 区别与 Captured Dependency 问题 | 待学习 | — | 面试必考 |

---

## 模块 C：ASP.NET Core Web 开发

| ID   | 知识点                                                           | 掌握度 | 最后学习日期 | 备注   |
| ---- | ------------------------------------------------------------- | --- | ------ | ---- |
| C.1  | HTTP 请求管道（中间件顺序与执行流程）                                         | 待学习 | —      | 面试必考 |
| C.2  | 自定义中间件（IMiddleware、Use/Run/Map）                               | 待学习 | —      |      |
| C.3  | 路由（属性路由、约定路由、路由约束）                                            | 待学习 | —      |      |
| C.4  | Controller 和 Action（模型绑定、FromBody/FromQuery/FromRoute）        | 待学习 | —      |      |
| C.5  | Action 返回值（IActionResult、ActionResult<T>、状态码）                 | 待学习 | —      |      |
| C.6  | 模型验证（DataAnnotations、IValidatableObject、FluentValidation）     | 待学习 | —      |      |
| C.7  | Filter（ActionFilter、ExceptionFilter、AuthorizationFilter、执行顺序） | 待学习 | —      |      |
| C.8  | Minimal API（.NET 6+，端点定义，路由分组）                                | 待学习 | —      |      |
| C.9  | 后台服务（IHostedService、BackgroundService）                        | 待学习 | —      |      |
| C.10 | HttpClient 最佳实践（IHttpClientFactory、类型化客户端）                    | 待学习 | —      |      |
| C.11 | 响应缓存与输出缓存                                                     | 待学习 | —      |      |
| C.12 | API 版本控制策略                                                    | 待学习 | —      |      |

---

## 模块 D：数据访问

| ID | 知识点 | 掌握度 | 最后学习日期 | 备注 |
|----|--------|--------|--------------|------|
| D.1 | EF Core vs EF6（差异、性能改进） | 待学习 | — | |
| D.2 | Code First（DbContext、DbSet<T>、Fluent API vs 注解） | 待学习 | — | |
| D.3 | 迁移（Add-Migration、Update-Database、迁移历史） | 待学习 | — | 对比 Rails db:migrate |
| D.4 | 关系映射（一对多、多对多、一对一） | 待学习 | — | |
| D.5 | 查询方式（Include 预加载、懒加载、显式加载） | 待学习 | — | |
| D.6 | N+1 问题（识别与用 Include 解决） | 待学习 | — | 面试常考 |
| D.7 | 追踪 vs 不追踪查询（AsNoTracking） | 待学习 | — | |
| D.8 | EF Core 中的原始 SQL 与存储过程 | 待学习 | — | |
| D.9 | Dapper（使用场景、多映射、动态查询） | 待学习 | — | |
| D.10 | Repository 模式（接口、实现、优缺点） | 待学习 | — | |
| D.11 | Unit of Work 模式 | 待学习 | — | |

---

## 模块 E：认证与安全

| ID | 知识点 | 掌握度 | 最后学习日期 | 备注 |
|----|--------|--------|--------------|------|
| E.1 | JWT 认证（结构、生成、验证） | 待学习 | — | |
| E.2 | Refresh Token 模式（存储、轮换、撤销） | 待学习 | — | |
| E.3 | ASP.NET Core Identity（UserManager、SignInManager、密码哈希） | 待学习 | — | |
| E.4 | OAuth 2.0 / OIDC（授权码流、客户端凭证流） | 待学习 | — | |
| E.5 | 基于策略的授权（Authorize Policy、IAuthorizationRequirement） | 待学习 | — | |
| E.6 | 基于角色 vs 基于声明的授权 | 待学习 | — | |
| E.7 | CORS（配置、预检请求、AllowAnyOrigin 的坑） | 待学习 | — | |
| E.8 | HTTPS 强制（HSTS、UseHttpsRedirection） | 待学习 | — | |
| E.9 | Data Protection API（IDataProtector、密钥管理） | 待学习 | — | |
| E.10 | 常见安全漏洞（SQL注入防护、XSS、CSRF） | 待学习 | — | |

---

## 模块 F：架构设计与设计模式

| ID | 知识点 | 掌握度 | 最后学习日期 | 备注 |
|----|--------|--------|--------------|------|
| F.1 | SOLID 原则（每条原则配 C# 示例） | 待学习 | — | 面试必考 |
| F.2 | 常见设计模式（Factory、Singleton、Observer、Strategy、Decorator） | 待学习 | — | |
| F.3 | Repository 模式（接口化、可测试性） | 待学习 | — | |
| F.4 | Clean Architecture / Onion Architecture（分层、依赖规则） | 待学习 | — | |
| F.5 | CQRS（命令/查询分离，有无事件溯源） | 待学习 | — | |
| F.6 | MediatR（IRequest、IRequestHandler、Pipeline Behavior） | 待学习 | — | |
| F.7 | 微服务基础概念（服务边界、API Gateway、服务间通信） | 待学习 | — | |
| F.8 | 事件驱动架构基础（消息队列、最终一致性） | 待学习 | — | |
| F.9 | DDD 基础概念（聚合、实体、值对象、领域事件） | 待学习 | — | |

---

## 模块 G：测试

| ID | 知识点 | 掌握度 | 最后学习日期 | 备注 |
|----|--------|--------|--------------|------|
| G.1 | xUnit 基础（Fact、Theory、InlineData、测试组织） | 待学习 | — | |
| G.2 | AAA 模式（Arrange、Act、Assert） | 待学习 | — | |
| G.3 | Moq 使用（Mock<T>、Setup、Verify、It.IsAny） | 待学习 | — | |
| G.4 | ASP.NET Core 测试（WebApplicationFactory、TestServer） | 待学习 | — | |
| G.5 | 集成测试策略（内存数据库、TestContainers） | 待学习 | — | |
| G.6 | TDD 工作流（红-绿-重构） | 待学习 | — | |
| G.7 | 测试中使用 DI（测试上下文中的服务注册） | 待学习 | — | |

---

## 模块 H：性能、部署与工具

| ID | 知识点 | 掌握度 | 最后学习日期 | 备注 |
|----|--------|--------|--------------|------|
| H.1 | 内存缓存（IMemoryCache、过期策略、驱逐） | 待学习 | — | |
| H.2 | 分布式缓存（Redis with StackExchange.Redis、IDistributedCache） | 待学习 | — | |
| H.3 | 异步最佳实践（避免 async void、ConfigureAwait(false)、死锁） | 待学习 | — | |
| H.4 | 常见异步陷阱（.Result/.Wait() 阻塞、线程池耗尽） | 待学习 | — | |
| H.5 | Docker 基础（.NET Core 应用 Dockerfile、多阶段构建） | 待学习 | — | |
| H.6 | docker-compose（多服务：API + DB + Redis） | 待学习 | — | |
| H.7 | CI/CD 基础（GitHub Actions 构建/测试/部署工作流） | 待学习 | — | |
| H.8 | 应用性能分析（BenchmarkDotNet、响应时间） | 待学习 | — | |
| H.9 | Health Checks（IHealthCheck、/health 端点） | 待学习 | — | |
| H.10 | Azure 基础服务（App Service、Azure SQL、Key Vault、App Insights） | 待学习 | — | |

---

## 知识盲区记录

> 由 Claude 在每次会话后自动更新。新增盲区按严重程度分级。

### 高优先级（面试即将考到，必须解决）

*暂无*

### 中优先级（重要但有时间消化）

*暂无*

### 低优先级（了解即可）

*暂无*

### 已解决的盲区

| 知识点 | 解决日期 | 说明 |
|--------|----------|------|
| （暂无） | — | — |

---

## 已掌握知识点

> 由 Claude 在每次会话后自动更新。

| 知识点 ID | 主题 | 掌握度 | 掌握日期 | 关键理解 |
|-----------|------|--------|----------|----------|
| （暂无） | — | — | — | — |

---

## 学习计划

### 第一周优先级（建议从这里开始）

基于 .NET Framework 背景，建议先建立"迁移认知"，快速定位熟悉 vs 陌生的部分：

1. **B.1** .NET Core vs .NET Framework — 先了解框架差异，建立整体认知
2. **B.7 + B.8** 依赖注入三种生命周期 — 理解 DI 是 .NET Core 一切的基础
3. **C.1** 中间件管道 — ASP.NET Core 最核心的概念之一
4. **A.1** async/await 底层原理 — C# 异步编程的基石

### 核心知识点清单（必须深度掌握）

- [ ] A.1 async/await 状态机原理
- [ ] A.3 LINQ 延迟执行
- [ ] A.6 值类型 vs 引用类型
- [ ] B.7 + B.8 DI 生命周期 + Captured Dependency 问题
- [ ] C.1 中间件管道执行顺序
- [ ] C.7 Filter 类型和执行顺序
- [ ] D.6 N+1 问题
- [ ] F.1 SOLID 原则

---

*此文件由 Claude 自动维护，每次学习会话后更新。*
