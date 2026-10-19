---
marp: true
theme: default
paginate: true
size: 16:9
style: |
  :root {
    --cansino-navy: #0F172A;
    --cansino-navy-2: #1E293B;
    --cansino-indigo: #1E40AF;
    --cansino-blue: #2563EB;
    --cansino-cyan: #06B6D4;
    --cansino-mint: #0E9F6E;
    --cansino-mint-soft: #ECFDF5;
    --cansino-slate: #64748B;
    --cansino-slate-light: #94A3B8;
    --cansino-border: #E2E8F0;
    --cansino-bg-soft: #F8FAFC;
    --cansino-sky-soft: #F0F7FF;
    --radius-md: 10px;
    --shadow-sm: 0 1px 2px rgba(15,23,42,.06), 0 4px 12px rgba(15,23,42,.04);
    --shadow-md: 0 4px 16px rgba(15,23,42,.08);
  }
  section {
    width: 1280px;
    height: 720px;
    padding: 38px 56px 42px 56px;
    background: #FFFFFF;
    color: #1E293B;
    font-family: 'Inter', 'SF Pro Display', 'Helvetica Neue', 'PingFang SC', 'Microsoft YaHei', sans-serif;
    font-size: 20px;
    line-height: 1.5;
    letter-spacing: -0.01em;
    border-top: 3px solid var(--cansino-blue);
    box-sizing: border-box;
    overflow: hidden;
    position: relative;
  }
  section::before {
    content: '';
    position: absolute;
    inset: 0;
    background-image: radial-gradient(circle at 1px 1px, rgba(148,163,184,.18) 1px, transparent 0);
    background-size: 22px 22px;
    mask-image: radial-gradient(ellipse 80% 60% at 50% 0%, black 70%, transparent 110%);
    pointer-events: none;
    z-index: 0;
  }
  section > * { position: relative; z-index: 1; }
  section::after {
    content: attr(data-marpit-pagination) ' / ' attr(data-marpit-pagination-total);
    position: absolute;
    right: 28px;
    bottom: 14px;
    font-size: 11px;
    font-weight: 600;
    letter-spacing: .08em;
    color: var(--cansino-slate-light);
    background: rgba(255,255,255,.92);
    border: 1px solid var(--cansino-border);
    padding: 3px 9px;
    border-radius: 999px;
  }
  h1 {
    font-size: 38px;
    font-weight: 800;
    line-height: 1.05;
    letter-spacing: -0.03em;
    color: var(--cansino-navy);
    margin: 0 0 10px 0;
  }
  h2 {
    font-size: 22px;
    font-weight: 700;
    line-height: 1.3;
    color: var(--cansino-navy);
    margin: 18px 0 12px 0;
    padding: 0 0 0 14px;
    border-left: 4px solid var(--cansino-blue);
    border-bottom: none !important;
  }
  h3 {
    font-size: 17px;
    font-weight: 700;
    color: var(--cansino-indigo);
    margin: 14px 0 6px 0;
  }
  p { margin: 6px 0; }
  strong { color: var(--cansino-navy); }
  a { color: var(--cansino-blue); text-decoration: none; border-bottom: 1px solid rgba(37,99,235,.3); }
  ul, ol { margin: 6px 0; padding-left: 0; list-style: none; }
  ul li, ol li {
    position: relative;
    padding-left: 20px;
    margin: 5px 0;
    line-height: 1.45;
    font-size: 0.92em;
  }
  ul li::before {
    content: '';
    position: absolute;
    left: 0; top: .62em;
    width: 7px; height: 7px;
    background: var(--cansino-blue);
    border-radius: 999px;
    transform: translateY(-50%);
    box-shadow: 0 0 0 4px rgba(37,99,235,.12);
  }
  ol { counter-reset: ol; }
  ol li { counter-increment: ol; }
  ol li::before {
    content: counter(ol);
    position: absolute;
    left: 0; top: .1em;
    width: 20px; height: 20px;
    background: var(--cansino-navy);
    color: #fff;
    font-size: 11px;
    font-weight: 700;
    display: grid;
    place-items: center;
    border-radius: 999px;
  }
  ul ul li::before { background: var(--cansino-cyan); box-shadow: 0 0 0 4px rgba(6,182,214,.12); }
  li li { font-size: 0.95em; color: #334155; }
  table {
    width: 100%;
    margin: 12px 0;
    border-collapse: separate;
    border-spacing: 0;
    border: 1px solid var(--cansino-border);
    border-radius: var(--radius-md);
    overflow: hidden;
    box-shadow: var(--shadow-sm);
    font-size: 0.78em;
    background: #fff;
  }
  thead th {
    background: var(--cansino-navy);
    color: #fff;
    font-weight: 700;
    font-size: 0.9em;
    letter-spacing: .04em;
    text-transform: uppercase;
    padding: 9px 12px;
    text-align: left;
    white-space: nowrap;
  }
  tbody td {
    padding: 8px 12px;
    border-top: 1px solid var(--cansino-border);
    border-left: 1px solid var(--cansino-border);
    vertical-align: middle;
  }
  tbody td:first-child { border-left: none; }
  tbody tr:nth-child(even) td { background: var(--cansino-bg-soft); }
  blockquote {
    margin: 12px 0;
    padding: 12px 16px;
    background: var(--cansino-sky-soft);
    border: 1px solid #DBEAFE;
    border-left: 4px solid var(--cansino-blue);
    border-radius: 0 var(--radius-md) var(--radius-md) 0;
    color: #1E293B;
    font-size: 0.88em;
    line-height: 1.5;
    box-shadow: var(--shadow-sm);
  }
  blockquote strong { color: var(--cansino-blue); }
  code {
    font-family: 'JetBrains Mono', 'SF Mono', ui-monospace, monospace;
    font-size: 0.82em;
    background: #F1F5F9;
    color: #0F172A;
    padding: 2px 6px;
    border-radius: 6px;
    border: 1px solid #E2E8F0;
  }
  pre {
    background: #0F172A;
    color: #E2E8F0;
    padding: 16px 18px;
    border-radius: var(--radius-md);
    font-size: 0.72em;
    line-height: 1.6;
    overflow: auto;
    box-shadow: var(--shadow-md);
    border: 1px solid #1E293B;
  }
  pre code { background: transparent; border: none; padding: 0; color: inherit; }
  .columns {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 28px;
    margin: 8px 0;
  }
  .columns > div {
    background: #fff;
    border: 1px solid var(--cansino-border);
    border-radius: var(--radius-md);
    padding: 14px 16px;
    box-shadow: var(--shadow-sm);
  }
  .kpis {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 14px;
    margin: 14px 0;
  }
  .kpi {
    background: #fff;
    border: 1px solid var(--cansino-border);
    border-radius: var(--radius-md);
    padding: 14px 16px;
    box-shadow: var(--shadow-sm);
    text-align: center;
  }
  .kpi b { display: block; font-size: 28px; font-weight: 800; color: var(--cansino-blue); line-height: 1; }
  .kpi span { font-size: 12px; font-weight: 600; letter-spacing: .06em; text-transform: uppercase; color: var(--cansino-slate); }
  .pill {
    display: inline-block;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: .06em;
    text-transform: uppercase;
    color: var(--cansino-blue);
    background: var(--cansino-sky-soft);
    border: 1px solid #DBEAFE;
    padding: 4px 10px;
    border-radius: 999px;
  }
  section.lead {
    background: radial-gradient(1200px 600px at 80% -10%, #3B82F6 0%, transparent 60%),
                radial-gradient(900px 500px at -10% 30%, #06B6D4 0%, transparent 50%),
                linear-gradient(135deg, #020617 0%, #0F172A 40%, #1E3A8A 75%, #1E40AF 100%);
    border-top: none;
    color: #fff;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    text-align: left;
    padding: 56px 64px;
  }
  section.lead::before { opacity: .12; }
  section.lead::after {
    background: rgba(255,255,255,.12);
    border-color: rgba(255,255,255,.18);
    color: rgba(255,255,255,.85);
    backdrop-filter: blur(6px);
  }
  section.lead h1 { color: #fff; font-size: 52px; line-height: 0.95; letter-spacing: -0.04em; margin: 0; max-width: 880px; }
  section.lead h2 { color: rgba(255,255,255,.82); font-size: 20px; font-weight: 500; border: none; padding: 0; margin: 14px 0 0 0; }
  section.lead p, section.lead strong { color: rgba(255,255,255,.92); }
  section.lead blockquote {
    background: rgba(255,255,255,.08);
    border-color: rgba(255,255,255,.14);
    border-left-color: var(--cansino-cyan);
    color: #fff;
    backdrop-filter: blur(8px);
  }
  section.divider {
    background: var(--cansino-bg-soft);
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  section.divider h1 { font-size: 44px; }
  section.divider h1::after {
    content: '';
    display: block;
    width: 56px;
    height: 4px;
    background: var(--cansino-blue);
    border-radius: 999px;
    margin-top: 14px;
  }
  section.compact { font-size: 18px; padding-top: 28px; }
  section.compact h1 { font-size: 32px; }
  section.compact h2 { font-size: 19px; }
  section.compact table { font-size: 0.72em; }
  .eyebrow { display: inline-block; font-size: 11px; font-weight: 700; letter-spacing: .12em; text-transform: uppercase; color: var(--cansino-slate); margin-bottom: 8px; }
  .eyebrow em { font-style: normal; color: var(--cansino-mint); letter-spacing: .10em; }
  .pill-muted { background: #F1F5F9; border-color: #E2E8F0; color: var(--cansino-slate); }
  .tag { display: inline-block; font-size: 11px; font-weight: 700; letter-spacing: .04em; padding: 3px 8px; border-radius: 999px; border: 1px solid var(--cansino-border); line-height: 1.2; vertical-align: middle; }
  .tag-blue { background: var(--cansino-sky-soft); border-color: #DBEAFE; color: var(--cansino-blue); }
  .tag-mint { background: var(--cansino-mint-soft); border-color: #A7F3D0; color: #065F46; }
  .tag-slate { background: #F8FAFC; border-color: var(--cansino-border); color: var(--cansino-slate); }
  .tag-cyan { background: #ECFEFF; border-color: #A5F3FC; color: #0E7490; }
  .columns.ba { gap: 22px; }
  .columns.ba > div { position: relative; }
  .columns.ba .ba-before { background: #F8FAFC !important; border-top: 3px solid #CBD5E1 !important; }
  .columns.ba .ba-after { background: #fff !important; border-top: 3px solid var(--cansino-blue) !important; box-shadow: 0 4px 16px rgba(37,99,235,.08) !important; }
  .columns.ba .pill { margin-bottom: 10px; }
  section.lead::before, section.divider::before {
    background-image: radial-gradient(circle at 1px 1px, rgba(148,163,184,.14) 1px, transparent 0), linear-gradient(30deg, transparent 48%, rgba(14,159,110,.06) 50%, transparent 52%), linear-gradient(150deg, transparent 48%, rgba(14,159,110,.04) 50%, transparent 52%);
    background-size: 22px 22px, 48px 48px, 48px 48px;
  }
  .step-timeline { display: flex; align-items: flex-start; gap: 0; margin: 16px 0 8px 0; justify-content: space-between; }
  .step { flex: 1; text-align: center; position: relative; padding: 0 6px; }
  .step::after { content: '→'; position: absolute; right: -8px; top: 20px; color: var(--cansino-slate-light); font-size: 13px; font-weight: 700; }
  .step:last-child::after { display: none; }
  .step-head { width: 38px; height: 38px; border-radius: 999px; display: grid; place-items: center; margin: 0 auto 8px; font-size: 15px; background: #fff; border: 2px solid var(--cansino-blue); color: var(--cansino-blue); font-weight: 800; box-shadow: var(--shadow-sm); }
  .step.mint .step-head { border-color: var(--cansino-mint); color: var(--cansino-mint); background: var(--cansino-mint-soft); }
  .step-title { font-size: 12.5px; font-weight: 700; color: var(--cansino-navy); line-height: 1.2; }
  .step-sub { font-size: 11px; color: var(--cansino-slate); line-height: 1.3; margin-top: 3px; }
  .layer-stack { display: flex; flex-direction: column; gap: 8px; margin: 12px 0; }
  .layer { display: flex; align-items: center; gap: 14px; background: #fff; border: 1px solid var(--cansino-border); border-radius: var(--radius-md); padding: 10px 14px; box-shadow: var(--shadow-sm); border-left: 4px solid var(--cansino-blue); font-size: 0.88em; }
  .layer.mint { border-left-color: var(--cansino-mint); }
  .layer.cyan { border-left-color: var(--cansino-cyan); }
  .layer.indigo { border-left-color: var(--cansino-indigo); }
  .layer-label { font-size: 11px; font-weight: 700; letter-spacing: .06em; text-transform: uppercase; color: var(--cansino-slate); min-width: 92px; }
  .card-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; margin: 10px 0; }
  .mini-card { background: #fff; border: 1px solid var(--cansino-border); border-radius: var(--radius-md); padding: 12px 14px; box-shadow: var(--shadow-sm); position: relative; }
  .mini-card::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 3px; background: var(--cansino-border); border-radius: var(--radius-md) var(--radius-md) 0 0; }
  .mini-card.accent-blue::before { background: var(--cansino-blue); }
  .mini-card.accent-mint::before { background: var(--cansino-mint); }
  .mini-card b { display: block; font-size: 13px; color: var(--cansino-navy); margin-bottom: 4px; }
  .mini-card span { font-size: 12.5px; color: #334155; line-height: 1.4; }
  .metric { display: inline-flex; align-items: baseline; gap: 6px; font-weight: 800; color: var(--cansino-blue); }
  .metric.mint { color: var(--cansino-mint); }
  .metric small { font-size: 12px; font-weight: 600; color: var(--cansino-slate); letter-spacing: .04em; }
  /* 防止插图溢出：内容图限高，封面 bg 不受影响 */
  section img { max-width: 100%; height: auto; object-fit: contain; }
  section img[alt*="w:"] { max-height: 300px; }
  /* 表格+图同页时，图再压一点 */
  section:has(table) img { max-height: 260px; }
---

<!-- _class: lead -->

# 康希诺生物数字化落地方案

## AI驱动研发效能提升

**康希诺生物股份有限公司**

![bg right:40% 86%](assets/cover-hero.svg)

---

<span class="eyebrow">Agenda · <em>Vaccine Intelligence</em></span>

# 议程

| 序号 | 主题 | 重点 |
|:---:|------|------|
| 01 | 四大建设方向概览 | 全局视角 |
| 02 | **AI全面助力研发流程** | <span class="tag tag-mint">核心重点</span> |
| 03 | 研发支撑体系 | CI/CD、质量、效能 |
| 04 | AI能力平台与场景 | 平台化能力建设 |
| 05 | 实施路径与保障 | 落地策略 |

> **本次重点**：AI如何贯穿软件开发生命周期，从需求到交付

---

<span class="eyebrow">Context · 01</span>

# 背景与机遇

<div class="card-grid">
<div class="mini-card accent-blue"><b>行业趋势</b><span>生物医药数字化加速 · AI成为研发效率核心驱动 · 合规（GMP/数据安全法）倒逼基座升级</span></div>
<div class="mini-card accent-mint"><b>康希诺机遇</b><span>多年信息化打底 · 核心系统已就绪 · 具备向深水区迈进的条件</span></div>
</div>

- 数字化不再是“可选”，而是疫苗研发与合规的**必答题**

---

<span class="eyebrow">Where we are · <em>Systems Ready</em></span>

# 现状与起点

| 系统 | 覆盖环节 | 状态 |
|------|----------|------|
| SAP | ERP、财务、供应链 | ✅ 已运行 |
| MES | 生产执行 | ✅ 已运行 |
| LIMS | 实验室管理 | ✅ 已运行 |
| WMS | 仓储物流 | ✅ 已运行 |
| QMS | 质量管理 | ✅ 已运行 |

<div class="card-grid">
<div class="mini-card"><b>⬡ 数据治理</b><span>主数据统一 · 数据贯通</span></div>
<div class="mini-card"><b>⬢ AI复用</b><span>从项目制到平台制</span></div>
<div class="mini-card"><b>⬣ 基座统一</b><span>私有云 · 合规底座</span></div>
<div class="mini-card accent-mint"><b>✦ 研发效能</b><span>ELN · 流程数字化</span></div>
</div>

---

<span class="eyebrow">Data & BI · 痛点</span>

# 数据治理+BI：痛点

<div class="card-grid">
<div class="mini-card"><b>⬡ 主数据不统一</b><span>编码规则不一致 · 跨系统对账依赖人工</span></div>
<div class="mini-card"><b>◐ 取数周期长</b><span>数据分散 · 时效性差 · 决策滞后</span></div>
<div class="mini-card"><b>⬢ 质量难追溯</b><span>无统一度量 · 问题难定位根因</span></div>
<div class="mini-card accent-blue"><b>✦ 决策靠经验</b><span>“事后报表”而非“实时洞察”</span></div>
</div>

---

<span class="eyebrow">Data & BI · 方案</span>

# 数据治理+BI：方案

| 模块 | 内容 | 效果 |
|------|------|------|
| **主数据统一** | 物料、人员、设备、客户统一编码 | <span class="tag tag-blue">一致性</span> |
| **数据汇聚** | 打通SAP/MES/LIMS/WMS数据链路 | <span class="tag tag-mint">自动贯通</span> |
| **指标中心** | 统一经营指标体系 | <span class="tag tag-cyan">多维洞察</span> |
| **经营看板** | 可视化分析看板 | <span class="tag tag-slate">实时呈现</span> |

> <span class="metric">3 项</span> 核心转变：贯通 · 可追溯 · 实时洞察

---

<span class="eyebrow">AI Infra · 平台化</span>

# AI基建概览

<span class="pill pill-muted">痛点</span> AI项目各自独立 · 模型/数据/接口无法跨场景复用 → <span class="pill">方案 · 统一AI能力平台</span>

| 能力 | 说明 | 复用 |
|------|------|------|
| 文档解析OCR | 实验报告、合同等文档自动解析 | <span class="tag tag-blue">高</span> |
| 图像质检 | 产品外观检测、缺陷识别 | <span class="tag tag-blue">高</span> |
| 时序预测 | 产能预测、库存预测 | <span class="tag tag-cyan">中</span> |
| 流程自动化RPA | 重复性流程自动执行 | <span class="tag tag-slate">中</span> |
| 大模型网关 | 兼容本地私有化与第三方API | <span class="tag tag-mint">关键</span> |

> <span class="metric">一次建设 · 多处复用</span> <small>业务系统快速接入</small>

---

<span class="eyebrow">Private Cloud · 合规底座</span>

# 私有云基座

| 模块 | 内容 | 合规 |
|------|------|------|
| **容器化** | 统一资源编排与调度 | <span class="tag tag-slate">弹性</span> |
| **网络安全** | 访问控制、入侵检测 | <span class="tag tag-blue">等保</span> |
| **数据加密** | 分级分类，敏感数据加密 | <span class="tag tag-cyan">数据安全法</span> |
| **灾备恢复** | 数据备份与灾难恢复 | <span class="tag tag-slate">连续性</span> |
| **审计堡垒机** | 统一操作审计 | <span class="tag tag-mint">GMP CSV</span> |

<span class="pill">核心价值</span> 为数据治理 · AI基建 · 业务系统提供统一运行底座

---

<span class="eyebrow">Architecture · 目标总览</span>

# 目标架构总览

![w:1100px](assets/arch-banner.svg)

> 协同层 → 业务系统群 → 能力层（数据+AI）→ 私有云基座 → 配套体系 · 横幅线框（1340×126）

---

<span class="eyebrow">R&D Efficiency · 痛点</span>

# 研发效能管理（1/2）：痛点

<div class="card-grid">
<div class="mini-card"><b>⬡ 数据分散</b><span>实验数据难检索 · 难复用</span></div>
<div class="mini-card"><b>◐ 进度不透明</b><span>项目/资源无统一视图</span></div>
<div class="mini-card"><b>⬢ 申报分散</b><span>文档管理 · 流程靠人工</span></div>
<div class="mini-card accent-mint"><b>✦ 知识流失</b><span>人员流动带来资产流失</span></div>
</div>

> 4 类痛点制约研发知识资产沉淀

---

<span class="eyebrow">R&D Efficiency · 方案</span>

# 研发效能管理（2/2）：建设内容

| 模块 | 功能 | 价值 |
|------|------|------|
| **电子实验记录本** | 结构化存储、模板化记录、数据检索 | <span class="tag tag-blue">复用</span> |
| **研发项目管理** | 项目组合、资源分配、进度跟踪 | <span class="tag tag-cyan">透明</span> |
| **注册申报** | 文档统一管理、流程跟踪 | <span class="tag tag-slate">规范</span> |
| **知识管理** | 工艺参数、实验数据、技术文档沉淀 | <span class="tag tag-mint">沉淀</span> |

<span class="pill">效果</span> 实验可检索 · 项目可视化 · 申报标准化 · 知识资产化

---

<!-- _class: lead -->

# AI全面助力研发流程

## 从需求到交付，AI贯穿全流程

---

<span class="eyebrow">AI Dev Lifecycle · 全景</span>

# AI研发全景图

![w:880px](assets/lifecycle.svg)

> <span class="metric">6 阶段</span> <small>蓝框=核心编码 · 绿框=知识沉淀 · 线框风格统一</small>

---

<span class="eyebrow">Stage 01 · 需求梳理</span>

# 需求梳理阶段

<div class="columns ba">
<div class="ba-before">

<span class="pill pill-muted">Before · 痛点</span>

- 需求模糊、歧义多，反复沟通确认
- 用户故事编写耗时
- 验收标准不清晰
- 竞品分析依赖人工

</div>
<div class="ba-after">

<span class="pill">After · AI赋能</span>

- **AI需求澄清**：模糊描述→结构化需求
- **AI用户故事**：自动生成用户故事、验收标准
- **AI竞品分析**：自动收集和分析竞品信息

</div>
</div>

> <span class="metric">50%+ <small>周期缩短</small></span> · 模糊需求一键结构化

---

<span class="eyebrow">Stage 02 · 蓝图/架构</span>

# 蓝图/架构设计

<div class="columns ba">
<div class="ba-before">

<span class="pill pill-muted">Before · 痛点</span>

- 架构方案依赖个人经验
- 技术选型缺乏系统评估
- 技术风险识别不全面
- 方案对比文档编写耗时

</div>
<div class="ba-after">

<span class="pill">After · AI赋能</span>

- **AI架构方案**：生成多种架构方案
- **AI技术选型**：分析各技术栈优劣
- **AI风险识别**：识别潜在技术风险
- **AI方案对比**：自动生成对比矩阵

</div>
</div>

> <span class="metric">40%+ <small>周期缩短</small></span> · 方案生成与风险前置

---

<span class="eyebrow">Stage 03 · 功能设计</span>

# 功能设计

<div class="columns ba">
<div class="ba-before">

<span class="pill pill-muted">Before · 痛点</span>

- PRD编写耗时，细节容易遗漏
- 接口设计依赖人工，联调问题多
- 数据模型设计反复迭代

</div>
<div class="ba-after">

<span class="pill">After · AI赋能</span>

- **AI PRD生成**：自动生成PRD初稿
- **AI接口设计**：自动生成API契约
- **AI数据模型**：生成数据模型建议

</div>
</div>

> <span class="metric">45%+ <small>周期缩短</small></span> · 契约与模型一次成型

---

<span class="eyebrow">Stage 04a · 编码生成</span>

# 编码实现：代码生成

<div class="columns ba">
<div class="ba-before">

<span class="pill pill-muted">Before · 痛点</span>

- 大量重复性代码编写
- 新技术学习曲线陡峭
- 代码风格不一致
- 开发者疲于写代码

</div>
<div class="ba-after">

<span class="pill">After · AI赋能</span>

- **AI代码生成**：根据需求生成代码框架
- **AI代码补全**：上下文感知的智能补全
- **AI代码解释**：快速理解遗留代码
- **AI代码翻译**：跨语言代码转换

</div>
</div>

> <span class="metric">30%+ <small>编码效率提升</small></span> · 从写代码到审代码

---

<span class="eyebrow">Stage 04b · 代码质量</span>

# 编码实现：代码质量

<div class="columns ba">
<div class="ba-before">

<span class="pill pill-muted">Before · 痛点</span>

- 代码审查依赖人工，效率低
- 技术债积累，难以量化管理
- 安全漏洞发现滞后
- 代码规范执行不一致

</div>
<div class="ba-after">

<span class="pill">After · AI赋能</span>

- **AI代码审查**：自动识别问题、规范违规
- **AI重构建议**：识别代码坏味道
- **AI技术债识别**：量化技术债，优先级排序
- **AI安全扫描**：识别潜在安全漏洞

</div>
</div>

> <span class="metric mint">60%+ <small>审查效率提升</small></span> · 规范与安全左移

---

<span class="eyebrow">Stage 05 · 测试验证</span>

# 测试验证

<div class="columns ba">
<div class="ba-before">

<span class="pill pill-muted">Before · 痛点</span>

- 测试用例编写耗时，覆盖率不足
- 自动化测试脚本维护成本高
- 缺陷根因分析依赖经验
- 回归测试范围选择困难

</div>
<div class="ba-after">

<span class="pill">After · AI赋能</span>

- **AI测试用例**：自动生成测试用例
- **AI自动化测试**：自动生成测试脚本
- **AI缺陷分析**：分析缺陷模式，识别根因
- **AI回归测试**：智能选择回归范围

</div>
</div>

> <span class="metric">50%+ <small>用例编写提效</small></span> · 覆盖率与回归更智能

---

<span class="eyebrow">Stage 06 · 文档交付</span>

# 文档与交付

<div class="columns ba">
<div class="ba-before">

<span class="pill pill-muted">Before · 痛点</span>

- 文档编写滞后，与代码不同步
- API文档维护成本高
- 知识散落在个人笔记中
- 变更日志容易遗漏

</div>
<div class="ba-after">

<span class="pill">After · AI赋能</span>

- **AI API文档**：基于代码自动生成
- **AI用户手册**：基于功能描述生成
- **AI变更日志**：自动生成版本变更
- **AI知识沉淀**：自动提取和整理知识

</div>
</div>

> <span class="metric mint">70%+ <small>文档提效</small></span> · 代码与知识同频沉淀

---

<!-- _class: compact -->

<span class="eyebrow">Case · 疫苗批次追溯（1/2）</span>

# 端到端案例：效率对比

**场景：疫苗批次追溯 — 40天 → 21天** <span class="tag tag-mint">↓ 47%</span>

![w:640px h:200px](assets/case.svg)

> 蓝=传统 · 深蓝=AI辅助 · 绿=关键提升点 · 横幅显示

---

<!-- _class: compact -->

<span class="eyebrow">Case · 疫苗批次追溯（2/2）</span>

# 端到端案例：分阶段数据

| 阶段 | 传统 | AI辅助 | 提升 |
|------|------|--------|------|
| 需求梳理 | 3天 | 1天 | <span class="tag tag-mint">66%</span> |
| 架构设计 | 5天 | 3天 | <span class="tag tag-blue">40%</span> |
| 功能设计 | 4天 | 2天 | <span class="tag tag-blue">50%</span> |
| 编码实现 | 15天 | 10天 | <span class="tag tag-slate">33%</span> |
| 测试验证 | 8天 | 4天 | <span class="tag tag-blue">50%</span> |
| 文档交付 | 5天 | 1天 | <span class="tag tag-mint">80%</span> |
| **总计** | **40天** | **21天** | <span class="tag tag-mint">47%</span> |

---

<span class="eyebrow">Value · 放大器而非替代者</span>

# AI研发价值总结

<div class="kpis">
<div class="kpi"><b>30-70%</b><span>效率提升</span></div>
<div class="kpi"><b style="color: var(--cansino-mint)">显著 ↑</b><span>质量改善</span></div>
<div class="kpi"><b>持续</b><span>知识沉淀</span></div>
</div>

| 价值维度 | 具体效果 |
|----------|----------|
| **效率提升** | 需求、架构、编码、测试、文档 |
| **质量改善** | 代码规范 · 测试覆盖 · 安全左移 |
| **知识沉淀** | 最佳实践沉淀 · 新人上手加快 |

> <span class="tag tag-blue">AI是放大器</span> 团队判断力仍是根基

---

<span class="eyebrow">R&D Support · CI/CD</span>

# CI/CD流水线

![w:860px](assets/pipeline.svg)

| 模块 | 内容 | 价值 |
|------|------|------|
| **自动化构建** | 代码提交自动触发构建 | <span class="tag tag-blue">快速反馈</span> |
| **自动化测试** | 单元测试、集成测试自动执行 | <span class="tag tag-mint">质量保障</span> |
| **自动化部署** | 一键部署到各环境 | <span class="tag tag-cyan">效率提升</span> |
| **流水线管控** | 质量门禁、审批流程、发布策略 | <span class="tag tag-slate">风险控制</span> |

---

<span class="eyebrow">Quality · 内建质量</span>

# 代码质量管控

| 维度 | 内容 | 指标 |
|------|------|------|
| **静态分析** | 代码规范、复杂度、重复率 | <span class="tag tag-slate">违规率</span> |
| **质量门禁** | 构建失败条件、合并前检查 | <span class="tag tag-blue">通过率</span> |
| **技术债管理** | 量化跟踪、优先级排序 | <span class="tag tag-cyan">技术债指数</span> |
| **代码评审** | 标准化评审流程、AI辅助评审 | <span class="tag tag-mint">覆盖率</span> |

> <span class="metric">质量是内建的</span> <small>不是测试出来的</small>

---

<span class="eyebrow">Metrics · 度量改进</span>

# 研发效能度量

| 指标 | 定义 | 目标 |
|------|------|------|
| **需求吞吐量** | 单位时间交付需求数 | <span class="tag tag-mint">提升</span> |
| **交付周期** | 从需求提出到上线的时间 | <span class="tag tag-blue">缩短</span> |
| **缺陷率** | 千行代码缺陷数 | <span class="tag tag-cyan">降低</span> |
| **代码覆盖率** | 测试覆盖的代码比例 | <span class="tag tag-mint">提升</span> |
| **变更失败率** | 部署后回滚或修复的比例 | <span class="tag tag-slate">降低</span> |

> <span class="pill pill-muted">原则</span> 度量是为了**改进**，不是为了**考核**

---

<span class="eyebrow">DevOps · 一体化</span>

# DevOps实践

| 模块 | 内容 | 关注 |
|------|------|------|
| **环境管理** | 开发、测试、预发、生产标准化 | <span class="tag tag-slate">一致性</span> |
| **配置管理** | 配置与代码分离 | <span class="tag tag-blue">可追溯</span> |
| **监控告警** | 应用性能监控、异常告警 | <span class="tag tag-cyan">可观测</span> |
| **发布策略** | 蓝绿 · 金丝雀 · 灰度 | <span class="tag tag-mint">低风险</span> |

<span class="pill">与AI结合</span> 异常检测 · 容量预测 · 日志分析

---

<!-- _class: compact -->

<span class="eyebrow">Platform · 一次建设 多处复用</span>

# AI能力平台架构

![w:1000px](assets/platform-banner.svg)

<span class="pill">分层解耦</span> 业务层 → AI能力层 → 网关层 → 基座层（绿底合规）· 横幅 653×69

---

<span class="eyebrow">Use Cases · 全价值链</span>

# AI应用场景矩阵

| 环节 | 应用场景 | AI能力 | 价值 |
|------|----------|--------|------|
| ![w:22px](assets/icons/domain-rd.svg) **研发** | 方案筛选、工艺优化、文献分析 | ML、NLP | <span class="tag tag-mint">周期缩短</span> |
| ![w:22px](assets/icons/domain-prod.svg) **生产** | 预测性维护、过程优化、智能检测 | 时序预测、图像识别 | <span class="tag tag-blue">良率提升</span> |
| ![w:22px](assets/icons/domain-supply.svg) **供应链** | 需求预测、库存优化、物流调度 | 预测模型、优化算法 | <span class="tag tag-cyan">成本降低</span> |
| ![w:22px](assets/icons/domain-sales.svg) **销售** | 销售预测、客户洞察、内容生成 | 预测模型、NLP | <span class="tag tag-slate">精准营销</span> |
| ![w:22px](assets/icons/domain-support.svg) **支撑** | 财务分析、合规监控、知识管理 | 异常检测、NLP | <span class="tag tag-slate">效率提升</span> |

> <span class="metric mint">一次建设 · 多处复用</span> · 线框图标统一描边 1.5px

---

<!-- _class: compact -->

<span class="eyebrow">Value Chain · 建设→能力→效果</span>

# 业务价值链路

![w:900px](assets/value-banner.svg)

> 建设方向 → 能力提升 → 业务效果 · 横幅 385×69 · 闭环传导

---

<span class="eyebrow">Landing · 技术+组织</span>

# AI落地关键要素

| 要素 | 说明 | 常见误区 |
|------|------|----------|
| **数据准备** | 数据质量是AI效果的基础 | <span class="tag tag-slate">工具即得</span> |
| **模型选型** | 场景驱动的模型选择与调优 | <span class="tag tag-slate">追新</span> |
| **安全合规** | 数据安全、模型安全、GMP合规 | <span class="tag tag-blue">忽视合规</span> |
| **团队能力** | AI理解力、应用能力、判断能力 | <span class="tag tag-mint">过度依赖</span> |

> <span class="pill">关键提醒</span> AI落地是**技术+组织**的双重变革

---

<span class="eyebrow">Roadmap · 分步推进</span>

# 三步走实施路径

![w:860px](assets/roadmap.svg)

| 阶段 | 目标 |
|------|------|
| **基础先行** | 6-12月 · 统一主数据 · 打通数据链路 |
| **能力扩展** | 12-24月 · 建设AI能力平台 |
| **成熟化** | 24-36月 · 规模化推广 · 沉淀资产 |

> <span class="tag tag-blue">分步推进</span> 降低风险 · 快速见效

---

<span class="eyebrow">Team · 工具 vs 根基</span>

# 团队能力建设

<div class="card-grid">
<div class="mini-card"><b>AI不能完全依赖</b><span>生成内容需人工校验 · 业务决策需专家把关 · 质量安全需人工兜底</span></div>
<div class="mini-card accent-mint"><b>核心理念</b><span><span class="metric">AI是工具</span> · 团队能力是<b>根基</b></span></div>
</div>

| 能力层次 | 内容 | 重点 |
|----------|------|------|
| **工具使用** | AI工具的基本操作和最佳实践 | <span class="tag tag-slate">必备</span> |
| **输出判断** | AI输出的校验、筛选和优化 | <span class="tag tag-blue">关键</span> |
| **业务结合** | AI与业务场景的深度融合 | <span class="tag tag-cyan">核心</span> |
| **战略决策** | AI应用的优先级和资源分配 | <span class="tag tag-mint">高阶</span> |

---

<span class="eyebrow">Risk · 提前应对</span>

# 风险与应对

| 风险类型 | 具体风险 | 应对策略 |
|----------|----------|----------|
| **技术风险** | AI效果不达预期 | <span class="tag tag-blue">小试点 · 快迭代</span> |
| **组织风险** | 团队接受度低 | <span class="tag tag-cyan">培训先行</span> |
| **合规风险** | 数据安全、GMP合规 | <span class="tag tag-mint">合规审查</span> |
| **供应商风险** | 技术锁定 | <span class="tag tag-slate">多供应商</span> |

> <span class="pill pill-muted">原则</span> 识别风险 · 提前应对 · 分步验证

---

<span class="eyebrow">Outcome · 核心资产</span>

# 预期效果

<div class="kpis" style="grid-template-columns: repeat(4, 1fr);">
<div class="kpi"><b>30-70%</b><span>效率提升</span></div>
<div class="kpi"><b>↓ 成本</b><span>IT成本优化</span></div>
<div class="kpi"><b style="color: var(--cansino-mint)">沉淀</b><span>数据与AI资产</span></div>
<div class="kpi"><b>实时</b><span>决策支撑</span></div>
</div>

| 价值维度 | 具体效果 |
|----------|----------|
| **业务效率** | 跨系统数据贯通 · AI辅助研发 |
| **IT成本** | 系统整合 · 运维复杂度降低 |
| **能力沉淀** | 主数据统一 · AI平台制 · 知识沉淀 |
| **决策支撑** | “事后报表” → “实时洞察” |

> <span class="tag tag-mint">长期价值</span> 数字化能力成为企业**核心资产**

---

<span class="eyebrow">Next Steps · 从研发效能切入</span>

# 下一步行动

<div class="step-timeline" style="margin-bottom: 10px;">
<div class="step"><div class="step-head">1</div><div class="step-title">启动诊断</div><div class="step-sub">1-2周</div></div>
<div class="step"><div class="step-head">2</div><div class="step-title">试点选择</div><div class="step-sub">2-4周</div></div>
<div class="step"><div class="step-head">3</div><div class="step-title">基础建设</div><div class="step-sub">3-6月</div></div>
<div class="step"><div class="step-head">4</div><div class="step-title">AI试点</div><div class="step-sub">6-12月</div></div>
<div class="step mint"><div class="step-head">5</div><div class="step-title">规模推广</div><div class="step-sub">12月+</div></div>
</div>

| 阶段 | 行动 |
|------|------|
| **启动诊断** | 现状评估，明确优先级 |
| **试点选择** | 1-2个高价值场景 |
| **基础建设** | 数据治理 + 私有云基座 |
| **AI试点** | AI能力平台 + 研发效能 |
| **规模推广** | 全面推广，持续优化 |

---

<!-- _class: lead -->

# 谢谢

## 康希诺生物数字化落地方案

**AI驱动研发效能提升**
