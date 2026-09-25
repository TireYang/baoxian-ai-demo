# 保E通 AI · 保险中介 AI Native 双版本演示

在线演示（GitHub Pages）：**https://tireyang.github.io/baoxian-ai-demo/**

保险中介数字化系统的两个版本对照演示。全部为**单文件、零依赖**的静态页面，双击即可离线打开，所有数据均为演示用模拟数据。

---

## 在线访问

| 方式 | 地址 | 适用 |
|---|---|---|
| 站点首页 | https://tireyang.github.io/baoxian-ai-demo/ | 默认，GitHub Pages（海外节点） |
| 新版演示（桌面） | https://tireyang.github.io/baoxian-ai-demo/demo/index-ai.html | 直接进入新版 |
| 新版演示（手机） | https://tireyang.github.io/baoxian-ai-demo/demo/index-ai.html?mobile=1 | 手机 / 真机 |
| 上一版演示 | https://tireyang.github.io/baoxian-ai-demo/demo/index.html | 数字化系统对照 |
| **离线包下载** | [baoxian-ai-demo-static.zip](https://tireyang.github.io/baoxian-ai-demo/baoxian-ai-demo-static.zip) | 国内网络 / 微信转发 / 内网 |
| 离线包备用地址 | [raw.githubusercontent（国内较快）](https://raw.githubusercontent.com/TireYang/baoxian-ai-demo/main/baoxian-ai-demo-static.zip) · [GitHub Release](https://github.com/TireYang/baoxian-ai-demo/releases/latest) | 上一个打不开时用 |

> **访问不了 `*.github.io` 或 `github.com`？** 国内网络对 GitHub 各域名屏蔽情况不同（实测 `github.com` 与 Release 资源域名经常超时，而 `*.github.io` / `raw.githubusercontent.com` 通常可用）。三种绕过方式：
> 1. 从 [Pages 站点直接下载离线包](https://tireyang.github.io/baoxian-ai-demo/baoxian-ai-demo-static.zip)（走 `*.github.io`，通常可用）；
> 2. 换 [raw.githubusercontent 备用地址](https://raw.githubusercontent.com/TireYang/baoxian-ai-demo/main/baoxian-ai-demo-static.zip)（国内一般较快）；
> 3. 直接把 **`demo/index-ai.html` 单文件**发给对方（约 200 KB），双击就是完整演示，含手机版。

本地运行无需构建、无依赖：

```bash
open index.html            # macOS，双击同理
python3 -m http.server 8080   # 或者起个静态服务
```

---

## 两个版本

| 版本 | 入口 | 说明 |
|---|---|---|
| ✦ **新版 · AI Native** | [`demo/index-ai.html`](demo/index-ai.html) | 10 个页面 + 完整手机版。AI 是能干活的数字员工，人只处理例外与审批，价值可算账 |
| 上一版 · 数字化系统（备胎） | [`demo/index.html`](demo/index.html) | 9 个业务页面的数字化台账系统 + 四角色权限演示 |

首页 `index.html` 是一个入口页，可对比进入两个版本。

---

## 新版（AI Native）包含什么

**AI 工作台**
- **AI 指挥中心** — 6 个 AI 数字员工的舰队视图（今日处理量 / 自动完成率 / 需人工 / 省工时）、实时执行流、待我决策的例外队列、风险拦截与合规闸门
- **Copilot 工作台** — 一个对话框跑完跨系统任务：AI 给计划 → 调用工具 → 产出结果 → 关键动作交人批准；含工具权限表、人审闸门策略、`ai_actions` 审计日志

**业务作业（AI 已接管大部分）**
- **客户经营 360** — 保障缺口雷达（现有保障充足度）+ 缺口量化 + 三档方案 + 建议书生成 + 埋点条款引用与合规护栏
- **续保 Agent** — 续保概率预测 × 分层策略 × 自动多轮触达 × A/B 话术实验
- **线索 Agent** — 智能评分与归因 + 5 分钟首触 + 自动分配路由 + 长尾培育序列
- **理赔 AI** — 8 段单证流水线：OCR → 要素抽取 → 责任判定 → 完整性 → 反欺诈 → 金额预估 → 人工复核

**风控中枢**
- **核保与合规** — 双录全量 AI 质检（含转写证据与时间戳）+ 智能核保预审（结论 + 依据条款 + 置信度）
- **对话式 BI** — 自然语言问经营 → 生成 SQL → 出图 → 归因 → 建议动作

**经营与平台**
- **AI 价值看板** — AI 自动完成率 / 节省工时 / 人力成本 / ROI，假设可拖滑块实时复算
- **AI 员工管理** — 每个 Agent 的技能、知识库、护栏、审批权限、SLA，以及全局人审闸门三档策略

**全局能力**：`⌘K` / `Ctrl+K` 指令中枢 · 右侧常驻 Copilot（含执行轨迹与审批卡片）· 四角色视角切换（总经理 / 客户经理 / 运营 / 合规风控）

---

## 手机版

新版 10 个页面**全部有对应的手机版本**，同一份数据、同一套 AI 语义，但是按「随手可用、一眼决策」重新设计：

- **三种查看方式**：桌面顶栏「📱 手机版」内嵌真机框 · 直接开 `demo/index-ai.html?mobile=1` · 浏览器窗口 ≤ 900px 自动切换
- **手机端专属设计**：底部 5 Tab（+「更多」抽屉装全部 10 项）· 顶部通栏「问 AI 或下指令」· 右下 AI 浮球唤起全屏 Copilot · 宽表改卡片流 · 长 AI 文本改左对齐块 · KPI 改横滑指标条 · 按钮 ≥ 37px 拇指可及 · 详情全屏抽屉 · Toast 下移避开 Tab 栏 · `env(safe-area-inset-bottom)` 适配全面屏
- **双端互跳**：手机端「更多 → 切换到桌面版」

---

## 关键价值口径（模拟数据）

| 指标 | 数值 |
|---|---|
| AI 自动完成率 | 82.4%（680 项任务中 560 项无人干预完成） |
| 每日节省人工工时 | 37.3 h ≈ 4.9 FTE/月 |
| 月节省人力成本 | ¥98,472（按 ¥120/h 综合人力成本） |
| AI 平台 + 模型月成本 | ¥18,600 |
| 月净收益 / ROI | ¥79,872 / **5.3×** |
| 增效侧 | 线索 5 分钟首触率 31%→100% · 续保率 68%→79% · 理赔结案 5.2→2.8 天 · 合规质检覆盖率 5%→100% · 交叉销售 +23% |

> 价值口径与假设的方法论说明见 [`demo/AI_NATIVE_ANALYSIS.md`](demo/AI_NATIVE_ANALYSIS.md)（含 7 个角色的 AI 赋能分析、AI Native 五原则、双端设计决策、落地建议）。页面中的滑块可以现场改假设复算。

---

## 目录结构

```
.
├── index.html                      # 双版本入口页（Pages 首页）
├── demo/
│   ├── index-ai.html               # ✦ 新版：AI Native（桌面版 + 手机版，10 个页面）
│   ├── index.html                  # 上一版：数字化系统（9 个页面）
│   └── AI_NATIVE_ANALYSIS.md       # 角色分析 / 设计原则 / 价值模型 / 落地建议
├── favicon.svg / favicon.ico       # 站点图标
├── .nojekyll                       # 关闭 Jekyll 处理，直接静态托管
└── README.md
```

---

## 说明

- 所有业务数据（客户、保单、线索、理赔、渠道、分成、ROI 数字）均为**演示用模拟数据**，不代表真实业绩，也不含任何真实个人信息。
- 页面为单文件 HTML，零外部依赖，可离线打开。
- 本仓库只托管静态演示页；可运行的全栈版本（Node + SQLite + Vue）与实现计划不在本仓库内。
