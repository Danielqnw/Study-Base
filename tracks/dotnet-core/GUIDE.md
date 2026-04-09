# .NET Core 技术体系 — 方向指南

本文件定义 .NET Core 方向的知识领域、模块划分和教学上下文。
由根目录 `CLAUDE.md` 调度加载。

---

## 学习者背景

- **已有经验**：.NET Framework（WebForms, MVC, Web API）、Ruby on Rails
- **目标岗位**：.NET Core 后端开发工程师
- **教学策略**：主动对比 .NET Framework / Rails 中的对应概念，降低迁移成本

---

## 知识领域：8 大模块

### Module A: C# Language Core (High Frequency)

- **A.1** `async`/`await` internals — state machine, `Task`, `ValueTask`
- **A.2** TPL (Task Parallel Library) — `Task.Run`, `Parallel.ForEach`, cancellation tokens
- **A.3** LINQ — deferred execution, expression trees, `IEnumerable` vs `IQueryable`
- **A.4** Generics — constraints, covariance/contravariance
- **A.5** Delegates, events, `Func<>`, `Action<>`, `Predicate<>`
- **A.6** Value types vs reference types — boxing/unboxing, stack vs heap
- **A.7** `struct` vs `class` — when to use each
- **A.8** Modern C# features — `record`, pattern matching, `init`, nullable reference types, `required`
- **A.9** Memory management — GC, `IDisposable`, `using`, `Span<T>`
- **A.10** Extension methods, expression-bodied members, tuples

**Interview Priority**: A.1 (async/await), A.3 (LINQ), A.6 (value/reference types) are asked in almost every .NET interview.

---

### Module B: .NET Core Runtime & Framework (Migration Focus)

- **B.1** .NET Core vs .NET Framework — key differences, cross-platform, performance
- **B.2** .NET versioning — .NET 5/6/7/8, LTS vs non-LTS
- **B.3** Generic Host (`IHost`, `IHostBuilder`) vs old `HttpApplication` / Global.asax
- **B.4** `Program.cs` and `Startup.cs` evolution (minimal hosting model in .NET 6+)
- **B.5** Configuration system — `appsettings.json`, environment variables, `IConfiguration`
- **B.6** Built-in logging — `ILogger<T>`, log levels, providers (vs `log4net`/`NLog`)
- **B.7** Dependency Injection — built-in DI container, `IServiceCollection`, service lifetimes
- **B.8** `Singleton` vs `Scoped` vs `Transient` — definitions, gotchas, captured dependency problem

**Key .NET Framework → .NET Core Migrations:**
| .NET Framework | .NET Core Equivalent |
|----------------|----------------------|
| `web.config` | `appsettings.json` + env vars |
| `Global.asax` | `Program.cs` / `Startup.cs` |
| `HttpContext.Current` | Injected `IHttpContextAccessor` |
| `System.Web.Mvc` | `Microsoft.AspNetCore.Mvc` |
| Unity / Autofac (manual) | Built-in DI container |

---

### Module C: ASP.NET Core Web Development (Must-Know)

- **C.1** HTTP request pipeline — middleware order and execution flow
- **C.2** Writing custom middleware — `IMiddleware`, `Use`, `Run`, `Map`
- **C.3** Routing — attribute routing, conventional routing, route constraints
- **C.4** Controller and Action — model binding, `[FromBody]`, `[FromQuery]`, `[FromRoute]`
- **C.5** Action results — `IActionResult`, `ActionResult<T>`, status codes
- **C.6** Model validation — `DataAnnotations`, `IValidatableObject`, `FluentValidation`
- **C.7** Filters — `IActionFilter`, `IExceptionFilter`, `IAuthorizationFilter`, filter order
- **C.8** Minimal API (`.NET 6+`) — endpoint definition, route groups
- **C.9** Background services — `IHostedService`, `BackgroundService`, hosted service patterns
- **C.10** `HttpClient` best practices — `IHttpClientFactory`, typed clients, `HttpClientHandler`
- **C.11** Response caching and output caching
- **C.12** API versioning strategies

**Key Concept: Middleware Pipeline**
```
Request → [Middleware 1] → [Middleware 2] → [Routing] → [Controller] → [Middleware 2] → [Middleware 1] → Response
```
Middleware executes in registration order on the way in, reverse order on the way out.

---

### Module D: Data Access

- **D.1** EF Core vs EF6 — differences, performance improvements
- **D.2** Code First approach — `DbContext`, `DbSet<T>`, fluent API vs data annotations
- **D.3** Migrations — `Add-Migration`, `Update-Database`, migration history
- **D.4** Relationships — one-to-many, many-to-many (join entity), one-to-one
- **D.5** Querying — `Include` (eager loading), lazy loading, explicit loading
- **D.6** N+1 problem — detection and prevention with `.Include()`
- **D.7** Tracking vs no-tracking queries — `AsNoTracking()`
- **D.8** Raw SQL and stored procedures in EF Core
- **D.9** Dapper — when to use over EF Core, multi-mapping, dynamic queries
- **D.10** Repository pattern — interface, implementation, benefits and criticisms
- **D.11** Unit of Work pattern — coordinating multiple repositories

**Rails → EF Core Comparison:**
| Rails ActiveRecord | EF Core Equivalent |
|--------------------|--------------------|
| `db/migrate/` | EF Migrations |
| `has_many :orders` | `.HasMany(u => u.Orders)` |
| `User.where(active: true)` | `dbContext.Users.Where(u => u.Active)` |
| `User.includes(:orders)` | `dbContext.Users.Include(u => u.Orders)` |
| `User.find(id)` | `dbContext.Users.FindAsync(id)` |

---

### Module E: Authentication & Security

- **E.1** JWT authentication — structure (header.payload.signature), generation, validation
- **E.2** Refresh token pattern — storage, rotation, revocation
- **E.3** ASP.NET Core Identity — `UserManager`, `SignInManager`, password hashing
- **E.4** OAuth 2.0 / OIDC — flows (Authorization Code, Client Credentials), when to use each
- **E.5** Policy-based authorization — `[Authorize(Policy = "...")]`, `IAuthorizationRequirement`
- **E.6** Role-based vs claims-based authorization
- **E.7** CORS — configuration, preflight requests, `AllowAnyOrigin` pitfalls
- **E.8** HTTPS enforcement — HSTS, `UseHttpsRedirection`
- **E.9** Data protection API — `IDataProtector`, key management
- **E.10** Common security pitfalls — SQL injection (via EF/parameterized), XSS, CSRF tokens

---

### Module F: Architecture & Design Patterns (Senior-Level)

- **F.1** SOLID principles — each principle with a C# example
- **F.2** Common design patterns — Factory, Singleton (DI vs static), Observer, Strategy, Decorator
- **F.3** Repository pattern — interface-based, testability
- **F.4** Clean Architecture / Onion Architecture — layers, dependency rule
- **F.5** CQRS — command/query separation, with and without event sourcing
- **F.6** MediatR — `IRequest`, `IRequestHandler`, pipeline behaviors
- **F.7** Microservices concepts — service boundaries, API Gateway, inter-service communication
- **F.8** Event-driven architecture basics — message queues, eventual consistency
- **F.9** Domain-Driven Design (DDD) concepts — aggregate, entity, value object, domain event

---

### Module G: Testing

- **G.1** xUnit basics — `[Fact]`, `[Theory]`, `[InlineData]`, test organization
- **G.2** AAA pattern — Arrange, Act, Assert
- **G.3** Mocking with Moq — `Mock<T>`, `Setup`, `Verify`, `It.IsAny<>()`
- **G.4** Testing ASP.NET Core — `WebApplicationFactory`, `TestServer`
- **G.5** Integration testing strategies — in-memory database, test containers
- **G.6** TDD workflow — red-green-refactor
- **G.7** Testing with DI — service registration in test context

---

### Module H: Performance, Deployment & Tooling

- **H.1** In-memory caching — `IMemoryCache`, cache expiration, eviction
- **H.2** Distributed caching — Redis with `StackExchange.Redis`, `IDistributedCache`
- **H.3** Async best practices — avoid `async void`, `ConfigureAwait(false)`, deadlocks
- **H.4** Common async pitfalls — blocking on async (`.Result`, `.Wait()`), thread pool starvation
- **H.5** Docker basics — Dockerfile for .NET Core app, multi-stage builds
- **H.6** `docker-compose` — multi-service setup (API + DB + Redis)
- **H.7** CI/CD basics — GitHub Actions workflow for build/test/deploy
- **H.8** Application performance — profiling, `BenchmarkDotNet`, response time
- **H.9** Health checks — `IHealthCheck`, `/health` endpoint
- **H.10** Azure basics — App Service, Azure SQL, Key Vault, Application Insights

---

## 知识重要性分级

| 重要性 | Module | 说明 |
|--------|--------|------|
| 核心 | A, C, B | .NET Core 开发的基石，日常工作和面试都绑定这些模块 |
| 重要 | D, F | 数据访问和架构设计体现技术深度 |
| 进阶 | E, G | 安全和测试体现工程专业度 |
| 拓展 | H | DevOps 知识体现现代工程文化素养 |

---

## 建议学习路径

基于 .NET Framework + Rails 的背景，推荐按以下顺序：

```
你的起点（.NET Framework + Rails）
    ↓
模块 B：.NET Core vs .NET Framework 核心差异  ← 先建立迁移认知
    ↓
模块 C：ASP.NET Core Web 开发                ← 日常开发最频繁接触
    ↓
模块 A：C# 现代语法特性                      ← 语言层面查漏补缺
    ↓
模块 D：EF Core 数据访问                     ← 对比 Rails ActiveRecord
    ↓
模块 E：认证与安全
    ↓
模块 F：架构设计模式                         ← 深入理解系统设计
    ↓
模块 G：测试
    ↓
模块 H：性能与部署
```

---

## 自测 & 面试模拟

当学习者要求"考考我"、"模拟面试"或想检验掌握深度时：

1. 从 tracker 中的薄弱领域选题（或指定模块）
2. 提出层层递进的问题 — 从基础到深入
3. 回答后给出结构化反馈：正确点、遗漏点、更深层的理解是什么
4. 追问更深层问题检验真正理解
5. 评分：**Strong / Acceptable / Needs Work**

**示例：**

> **问题**: "能解释一下 ASP.NET Core 中的依赖注入是怎么工作的吗？"
>
> [学习者回答]
>
> **反馈**: "不错 — 你正确描述了三种生命周期。但更深层的理解还需要包括 Captured Dependency 问题：如果把 Scoped 服务注入到 Singleton 中，Scoped 服务实际上变成了 Singleton，这可能导致 bug。这也是面试中非常常见的追问。"

---

## 深度检验问题参考

**C# 核心概念：**
- `async`/`await` 的底层原理是什么？`Task` 和 `Thread` 的区别？
- `IEnumerable<T>` 的延迟执行如何工作？
- `struct` 和 `class` 的本质区别？什么时候用 `struct`？

**ASP.NET Core 核心概念：**
- 请描述 HTTP 请求在 ASP.NET Core 中的完整处理流程
- `Singleton`、`Scoped`、`Transient` 各适用什么场景？搞错了会出什么问题？
- 中间件和 Filter 的区别是什么？

**架构设计：**
- 什么是 SOLID 原则？举例说明你在项目中如何应用的
- Repository 模式解决了什么问题？
- 什么是 CQRS？什么场景下适合使用？

---

## 权威知识来源

> AI 在教学中应优先参考以下来源，确保内容准确。学习者可随时补充。

### 官方文档
- [Microsoft Learn — ASP.NET Core](https://learn.microsoft.com/en-us/aspnet/core/)
- [Microsoft Learn — C# Guide](https://learn.microsoft.com/en-us/dotnet/csharp/)
- [Microsoft Learn — EF Core](https://learn.microsoft.com/en-us/ef/core/)
- [.NET API Browser](https://learn.microsoft.com/en-us/dotnet/api/)

### 经典书籍
- *C# in Depth* — Jon Skeet
- *CLR via C#* — Jeffrey Richter
- *Dependency Injection Principles, Practices, and Patterns* — Steven van Deursen & Mark Seemann
- *Designing Data-Intensive Applications* — Martin Kleppmann（架构通用）

### 权威博客 / 作者
- [Andrew Lock (.NET Escapades)](https://andrewlock.net/)
- [Stephen Cleary (async/await 权威)](https://blog.stephencleary.com/)
- [Nick Chapsas (YouTube)](https://www.youtube.com/@nickchapsas)
- [Microsoft .NET Blog](https://devblogs.microsoft.com/dotnet/)

### 社区资源
- [Stack Overflow — .NET Core 标签](https://stackoverflow.com/questions/tagged/.net-core)
- [GitHub — ASP.NET Core 源码](https://github.com/dotnet/aspnetcore)

### 学习者补充的来源
（你发现的好资源可以随时加在这里）
