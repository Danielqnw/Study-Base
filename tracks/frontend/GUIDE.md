# 前端开发技术体系 — 方向指南

本文件定义前端开发方向的知识领域、模块划分和教学上下文。
由根目录 `CLAUDE.md` 调度加载。

---

## 学习者背景

- **已有经验**：（请补充你的前端经验背景）
- **目标岗位**：前端开发工程师
- **教学策略**：（根据背景调整，比如：从后端视角理解前端、对比 jQuery 与现代框架等）

---

## 知识领域：8 大模块

### Module A: HTML / CSS 基础与进阶

- **A.1** HTML5 语义化标签（header、nav、section、article 等的正确使用）
- **A.2** 表单与表单验证（原生验证 API、无障碍表单设计）
- **A.3** CSS 盒模型（content-box vs border-box、margin 折叠）
- **A.4** Flexbox 布局（主轴/交叉轴、常见布局模式）
- **A.5** Grid 布局（grid-template、fr 单位、响应式网格）
- **A.6** CSS 定位（static/relative/absolute/fixed/sticky 区别）
- **A.7** 响应式设计（媒体查询、移动优先、viewport 单位）
- **A.8** CSS 预处理器与现代方案（Sass/Less、CSS Modules、CSS-in-JS、Tailwind）
- **A.9** 动画与过渡（transition、animation、transform、requestAnimationFrame）
- **A.10** 无障碍（ARIA 属性、键盘导航、语义化 HTML 的重要性）

---

### Module B: JavaScript 核心

- **B.1** 数据类型与类型转换（== vs ===、隐式转换规则）
- **B.2** 作用域与闭包（词法作用域、闭包的应用与陷阱）
- **B.3** 原型链与继承（prototype、`__proto__`、class 语法糖）
- **B.4** this 指向规则（默认绑定、隐式绑定、显式绑定、new 绑定、箭头函数）
- **B.5** 异步编程（回调、Promise、async/await、事件循环/Event Loop）
- **B.6** ES6+ 新特性（let/const、解构、展开运算符、Map/Set、Symbol、Proxy）
- **B.7** 模块系统（CommonJS vs ESM、import/export、动态导入）
- **B.8** 错误处理（try/catch、Promise 错误链、全局错误捕获）
- **B.9** 正则表达式基础（常见匹配模式、面试常见正则题）
- **B.10** 手写实现系列（深拷贝、防抖节流、发布订阅、Promise.all 等）

**面试重点**: B.2 (闭包), B.4 (this), B.5 (事件循环), B.10 (手写题) 几乎每场面试必考。

---

### Module C: 框架 — React（或 Vue，根据目标调整）

- **C.1** 组件化思想（函数组件 vs 类组件、组件拆分原则）
- **C.2** JSX 原理（虚拟 DOM、React.createElement）
- **C.3** State 与 Props（单向数据流、不可变性原则）
- **C.4** Hooks 核心（useState、useEffect、useRef、useCallback、useMemo）
- **C.5** 自定义 Hooks（抽取逻辑复用、常见模式）
- **C.6** 组件通信（props drilling、Context、状态管理库）
- **C.7** 生命周期与副作用管理（useEffect 依赖数组、清理函数）
- **C.8** 列表渲染与 Key 的作用（Diff 算法基础、为什么不能用 index 做 key）
- **C.9** 受控组件与非受控组件（表单处理最佳实践）
- **C.10** React Router（路由配置、嵌套路由、路由守卫）
- **C.11** 状态管理（Redux/Zustand/Jotai 的选型与核心原理）
- **C.12** SSR / SSG 基础（Next.js 概念、getServerSideProps vs getStaticProps）

---

### Module D: 浏览器原理与网络

- **D.1** 浏览器渲染流程（解析 → DOM → CSSOM → 渲染树 → 布局 → 绘制 → 合成）
- **D.2** 重排与重绘（触发条件、优化策略）
- **D.3** 事件机制（捕获/冒泡/委托、stopPropagation vs preventDefault）
- **D.4** 浏览器存储（Cookie、localStorage、sessionStorage、IndexedDB 对比）
- **D.5** 跨域问题（同源策略、CORS、JSONP、代理方案）
- **D.6** HTTP 协议基础（请求方法、状态码、缓存策略 — 强缓存/协商缓存）
- **D.7** HTTPS 原理（TLS 握手、证书验证）
- **D.8** HTTP/2 和 HTTP/3 特性（多路复用、Server Push、QUIC）
- **D.9** WebSocket（与 HTTP 对比、使用场景、心跳机制）
- **D.10** 浏览器安全（XSS、CSRF、CSP、点击劫持防御）

---

### Module E: 前端工程化

- **E.1** 包管理器（npm/yarn/pnpm 的区别、lock 文件的作用）
- **E.2** 构建工具（Webpack 核心概念 — loader/plugin/chunk、Vite 为什么快）
- **E.3** Babel 与编译（AST、preset、polyfill）
- **E.4** 代码规范（ESLint、Prettier、Husky + lint-staged）
- **E.5** TypeScript 核心（类型系统、interface vs type、泛型、工具类型）
- **E.6** TypeScript 进阶（条件类型、映射类型、infer、声明文件）
- **E.7** 模块联邦 / 微前端（Module Federation、qiankun、single-spa）
- **E.8** Monorepo 管理（pnpm workspace、Turborepo、Nx）
- **E.9** CI/CD 与自动化部署（GitHub Actions、Vercel/Netlify）

---

### Module F: 性能优化

- **F.1** 性能指标（FCP、LCP、CLS、TTI、Core Web Vitals）
- **F.2** 资源加载优化（代码分割、懒加载、预加载 preload/prefetch）
- **F.3** 图片优化（WebP/AVIF、响应式图片、懒加载）
- **F.4** 运行时性能（虚拟列表、防抖节流、requestIdleCallback）
- **F.5** React 性能优化（React.memo、useMemo、useCallback、代码分割）
- **F.6** 网络优化（CDN、HTTP 缓存策略、资源压缩 gzip/brotli）
- **F.7** 性能监控与分析工具（Lighthouse、Chrome DevTools Performance 面板）

---

### Module G: 算法与数据结构（前端向）

- **G.1** 数组常见操作（双指针、滑动窗口、排序算法）
- **G.2** 字符串处理（反转、回文、模式匹配）
- **G.3** 栈和队列（有效括号、单调栈、BFS）
- **G.4** 链表（反转、合并、环检测）
- **G.5** 树（遍历方式、DFS/BFS、二叉搜索树）
- **G.6** 哈希表（两数之和、字符频次统计）
- **G.7** 动态规划基础（爬楼梯、背包问题、最长子序列）
- **G.8** 常见 LeetCode 高频题型（Top 50 前端面试算法题）

---

### Module H: 综合能力与软技能

- **H.1** 系统设计（设计一个前端组件库、设计一个实时协作编辑器）
- **H.2** 项目经验表述（STAR 法则、如何讲清楚技术方案与取舍）
- **H.3** 调试能力（Chrome DevTools 高级用法、网络调试、内存泄漏排查）
- **H.4** Git 工作流（分支策略、rebase vs merge、Cherry-pick、冲突解决）
- **H.5** 移动端适配（rem/vw 方案、1px 问题、安全区域适配）
- **H.6** 跨端开发基础（React Native / Flutter / Taro / uni-app 了解）

---

## 知识重要性分级

| 重要性 | Module | 说明 |
|--------|--------|------|
| 核心 | B, C, D | JS 核心、框架原理、浏览器/网络 — 前端开发的基石 |
| 重要 | E, F | 工程化和性能优化体现工程素养和深度 |
| 基础/进阶 | A, G | CSS 布局是基本功，算法是进阶能力 |
| 拓展 | H | 系统设计和综合能力体现技术视野 |

---

## 自测 & 面试模拟

当学习者要求"考考我"、"模拟面试"或想检验掌握深度时：

1. 从 tracker 中的薄弱领域选题（或指定模块）
2. 提出层层递进的问题 — 从基础到深入
3. 回答后给出结构化反馈：正确点、遗漏点、更深层的理解是什么
4. 追问更深层问题检验真正理解
5. 评分：**Strong / Acceptable / Needs Work**

---

## 深度检验问题参考

**JavaScript 核心概念：**
- 解释一下闭包是什么？给个实际应用场景
- 说说事件循环（Event Loop）的执行机制，微任务和宏任务的区别？
- `this` 的指向规则是什么？箭头函数的 `this` 有什么特殊？

**React 核心概念：**
- 虚拟 DOM 是什么？Diff 算法是怎么工作的？
- useEffect 的依赖数组为空和不传有什么区别？
- React 中 key 的作用是什么？为什么不建议用 index？

**工程化核心概念：**
- Webpack 的 loader 和 plugin 有什么区别？
- Vite 为什么比 Webpack 快？
- TypeScript 中 interface 和 type 有什么区别？

---

## 权威知识来源

> AI 在教学中应优先参考以下来源，确保内容准确。学习者可随时补充。

### 官方文档
- [MDN Web Docs (HTML/CSS/JS 权威参考)](https://developer.mozilla.org/)
- [React 官方文档](https://react.dev/)
- [TypeScript 官方文档](https://www.typescriptlang.org/docs/)
- [Node.js 官方文档](https://nodejs.org/docs/)
- [Vite 官方文档](https://vitejs.dev/)
- [Webpack 官方文档](https://webpack.js.org/)

### 规范 / 标准
- [ECMAScript 规范 (TC39)](https://tc39.es/)
- [W3C 标准](https://www.w3.org/)
- [WHATWG (HTML Living Standard)](https://html.spec.whatwg.org/)

### 经典书籍
- *JavaScript 高级程序设计（红宝书）* — Matt Frisbie
- *你不知道的 JavaScript* — Kyle Simpson
- *JavaScript: The Good Parts* — Douglas Crockford
- *CSS 权威指南* — Eric Meyer & Estelle Weyl

### 权威博客 / 作者
- [Dan Abramov (overreacted.io)](https://overreacted.io/) — React 核心团队
- [Kent C. Dodds](https://kentcdodds.com/) — React 测试与最佳实践
- [Josh W. Comeau](https://www.joshwcomeau.com/) — CSS 与 React 深度文章
- [web.dev (Google)](https://web.dev/) — 性能与 Web 标准

### 社区资源
- [Can I Use (浏览器兼容性)](https://caniuse.com/)
- [State of JS (年度调查)](https://stateofjs.com/)
- [GitHub — React 源码](https://github.com/facebook/react)

### 学习者补充的来源
（你发现的好资源可以随时加在这里）
