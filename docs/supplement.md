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
  }
  section {
    width: 1280px; height: 720px;
    padding: 38px 56px 42px 56px;
    background: #fff; color: #1E293B;
    font-family: 'Inter','SF Pro Display','Helvetica Neue','PingFang SC','Microsoft YaHei',sans-serif;
    font-size: 20px; line-height: 1.5; letter-spacing: -0.01em;
    border-top: 3px solid var(--cansino-blue);
    box-sizing: border-box; overflow: hidden; position: relative;
  }
  section::before {
    content: ''; position: absolute; inset: 0;
    background-image: radial-gradient(circle at 1px 1px, rgba(148,163,184,.14) 1px, transparent 0), linear-gradient(30deg, transparent 48%, rgba(14,159,110,.06) 50%, transparent 52%), linear-gradient(150deg, transparent 48%, rgba(14,159,110,.04) 50%, transparent 52%);
    background-size: 22px 22px, 48px 48px, 48px 48px;
    mask-image: radial-gradient(ellipse 80% 60% at 50% 0%, black 70%, transparent 110%);
    pointer-events: none; z-index: 0;
  }
  section > * { position: relative; z-index: 1; }
  section::after {
    content: attr(data-marpit-pagination) ' / ' attr(data-marpit-pagination-total);
    position: absolute; right: 28px; bottom: 14px;
    font-size: 11px; font-weight: 600; letter-spacing: .08em;
    color: var(--cansino-slate-light);
    background: rgba(255,255,255,.92); border: 1px solid var(--cansino-border);
    padding: 3px 9px; border-radius: 999px;
  }
  h1 { font-size: 36px; font-weight: 800; line-height: 1.05; letter-spacing: -0.03em; color: var(--cansino-navy); margin: 0 0 10px 0; }
  h2 { font-size: 21px; font-weight: 700; color: var(--cansino-navy); margin: 14px 0 10px 0; padding-left: 14px; border-left: 4px solid var(--cansino-blue); }
  ul,ol { margin: 6px 0; padding-left: 0; list-style: none; }
  ul li { position: relative; padding-left: 20px; margin: 4px 0; line-height: 1.45; font-size: 0.90em; }
  ul li::before { content: ''; position: absolute; left:0; top:.62em; width:7px; height:7px; background: var(--cansino-blue); border-radius: 999px; box-shadow: 0 0 0 4px rgba(37,99,235,.12); }
  .eyebrow { display:inline-block; font-size:11px; font-weight:700; letter-spacing:.12em; text-transform:uppercase; color:var(--cansino-slate); margin-bottom:8px; }
  .eyebrow em { font-style:normal; color:var(--cansino-mint); }
  .pill { display:inline-block; font-size:11px; font-weight:700; letter-spacing:.06em; text-transform:uppercase; color:var(--cansino-blue); background:var(--cansino-sky-soft); border:1px solid #DBEAFE; padding:4px 10px; border-radius:999px; }
  .pill-muted { background:#F1F5F9; border-color:#E2E8F0; color:var(--cansino-slate); }
  .tag { display:inline-block; font-size:11px; font-weight:700; letter-spacing:.04em; padding:3px 8px; border-radius:999px; border:1px solid var(--cansino-border); }
  .tag-mint { background:var(--cansino-mint-soft); border-color:#A7F3D0; color:#065F46; }
  .columns { display:grid; grid-template-columns:1fr 1fr; gap:22px; margin: 8px 0; }
  .columns.ba > div { background:#fff; border:1px solid var(--cansino-border); border-radius:10px; padding:14px 16px; box-shadow:var(--shadow-sm); }
  .columns.ba .ba-before { background:#F8FAFC !important; border-top:3px solid #CBD5E1 !important; }
  .columns.ba .ba-after { background:#fff !important; border-top:3px solid var(--cansino-blue) !important; box-shadow:0 4px 16px rgba(37,99,235,.08) !important; }
  .columns.ba .pill { margin-bottom:8px; }
  .metric { display:inline-flex; align-items:baseline; gap:6px; font-weight:800; color:var(--cansino-blue); }
  .metric.mint { color: var(--cansino-mint); }
  .metric small { font-size:12px; font-weight:600; color:var(--cansino-slate); }
  section img { max-width:100%; height:auto; object-fit:contain; }
  section img[alt*="w:"] { max-height: 260px; }
  .shot-placeholder { display:flex; align-items:center; justify-content:center; height: 220px; border:1px dashed #CBD5E1; border-radius:10px; background:#F8FAFC; color:#94A3B8; font-size:13px; font-weight:600; letter-spacing:.04em; margin: 8px 0 4px 0; }
  .caption { font-size:11px; color:var(--cansino-slate); text-align:center; margin: 2px 0 0 0; }
  section.lead {
    background: radial-gradient(1200px 600px at 80% -10%, #3B82F6 0%, transparent 60%), radial-gradient(900px 500px at -10% 30%, #06B6D4 0%, transparent 50%), linear-gradient(135deg, #020617 0%, #0F172A 40%, #1E3A8A 75%, #1E40AF 100%);
    border-top:none; color:#fff; display:flex; flex-direction:column; justify-content:center; align-items:flex-start; text-align:left; padding:56px 64px;
  }
  section.lead h1 { color:#fff; font-size:48px; max-width:860px; }
  section.lead h2 { color:rgba(255,255,255,.82); font-size:18px; font-weight:500; border:none; padding:0; }
  section.lead::after { background:rgba(255,255,255,.12); border-color:rgba(255,255,255,.18); color:rgba(255,255,255,.85); }
  section.compact { font-size:18px; padding-top:28px; }
  section.compact h1 { font-size:32px; }
---

<!-- _class: lead -->

# AI 助力开发流程 · 实战证据

## 主篇附录 · 按需插播

本篇为 `slide.pptx` 的补充弹药库<br/>7 个环节均预留真实工作截图占位（`assets/shots/`），后续替换即得

---

<!-- _class: compact -->

<span class="eyebrow">Stage 01 · 需求梳理</span>

# 需求梳理 · 实战

<div class="columns ba">
<div class="ba-before">

<span class="pill pill-muted">Before</span>

- 需求模糊，反复沟通
- 用户故事耗时
- 验收标准缺失

</div>
<div class="ba-after">

<span class="pill">After · AI赋能</span>

- 模糊描述→结构化需求
- 自动生成用户故事
- 验收标准一键补齐

</div>
</div>

<!-- TODO: 待补充真实截图 assets/shots/req-01.png -->
<div class="shot-placeholder">截图占位 · req-01.png（待补充）</div>
<p class="caption">示例：AI 需求澄清对话 · 输入模糊描述 → 输出结构化需求</p>

---

<!-- _class: compact -->

<span class="eyebrow">Stage 02 · 蓝图/架构 <span class="tag tag-mint">重点</span></span>

# 蓝图设计 · 实战

<div class="columns ba">
<div class="ba-before">

<span class="pill pill-muted">Before</span>

- 依赖个人经验
- 选型无系统评估
- 风险识别不全

</div>
<div class="ba-after">

<span class="pill">After · AI赋能</span>

- 多方案生成
- 技术栈优劣分析
- 风险前置识别

</div>
</div>

<!-- TODO: 待补充真实截图 assets/shots/arch-01.png -->
<div class="shot-placeholder">截图占位 · arch-01.png（待补充）</div>
<p class="caption">示例：AI 架构方案对比 / 技术选型问答 · 重点环节</p>

---

<!-- _class: compact -->

<span class="eyebrow">Stage 03 · 功能设计</span>

# 功能设计 · 实战

<div class="columns ba">
<div class="ba-before">

<span class="pill pill-muted">Before</span>

- PRD 易遗漏细节
- 接口人工设计
- 模型反复迭代

</div>
<div class="ba-after">

<span class="pill">After · AI赋能</span>

- PRD 初稿生成
- API 契约生成
- 数据模型建议

</div>
</div>

<!-- TODO: 待补充真实截图 assets/shots/func-01.png -->
<div class="shot-placeholder">截图占位 · func-01.png（待补充）</div>
<p class="caption">示例：AI 生成 PRD 片段 / OpenAPI 契约</p>

---

<!-- _class: compact -->

<span class="eyebrow">Stage 04a · 编码生成 <span class="tag tag-mint">重点</span></span>

# 代码编写 · 实战

<div class="columns ba">
<div class="ba-before">

<span class="pill pill-muted">Before</span>

- 重复代码多
- 学习曲线陡
- 风格不一致

</div>
<div class="ba-after">

<span class="pill">After · AI赋能</span>

- 代码框架生成
- 上下文补全
- 遗留代码解释

</div>
</div>

<!-- TODO: 待补充真实截图 assets/shots/code-gen-01.png -->
<div class="shot-placeholder">截图占位 · code-gen-01.png（待补充）</div>
<p class="caption">示例：IDE 内 AI 生成 / diff 对比 · 重点环节</p>

---

<!-- _class: compact -->

<span class="eyebrow">Stage 04b · 代码质量</span>

# 代码质量 · 实战

<div class="columns ba">
<div class="ba-before">

<span class="pill pill-muted">Before</span>

- 审查靠人工
- 技术债难量化
- 漏洞滞后

</div>
<div class="ba-after">

<span class="pill">After · AI赋能</span>

- 规范违规识别
- 重构建议
- 安全扫描

</div>
</div>

<!-- TODO: 待补充真实截图 assets/shots/code-review-01.png -->
<div class="shot-placeholder">截图占位 · code-review-01.png（待补充）</div>
<p class="caption">示例：AI Code Review 评论 / 重构建议</p>

---

<!-- _class: compact -->

<span class="eyebrow">Stage 05 · 测试验证 <span class="tag tag-mint">重点</span></span>

# 测试验证 · 实战

<div class="columns ba">
<div class="ba-before">

<span class="pill pill-muted">Before</span>

- 用例耗时
- 覆盖率不足
- 根因靠经验

</div>
<div class="ba-after">

<span class="pill">After · AI赋能</span>

- 用例自动生成
- 测试脚本生成
- 缺陷根因分析

</div>
</div>

<!-- TODO: 待补充真实截图 assets/shots/test-01.png -->
<div class="shot-placeholder">截图占位 · test-01.png（待补充）</div>
<p class="caption">示例：AI 生成用例 / 测试报告 · 重点环节</p>

---

<!-- _class: compact -->

<span class="eyebrow">Stage 06 · 文档交付</span>

# 文档交付 · 实战

<div class="columns ba">
<div class="ba-before">

<span class="pill pill-muted">Before</span>

- 文档滞后
- 维护成本高
- 知识零散

</div>
<div class="ba-after">

<span class="pill">After · AI赋能</span>

- API 文档生成
- 用户手册生成
- 知识沉淀

</div>
</div>

<!-- TODO: 待补充真实截图 assets/shots/docs-01.png -->
<div class="shot-placeholder">截图占位 · docs-01.png（待补充）</div>
<p class="caption">示例：代码→API 文档 自动生成前后对比</p>

---

<span class="eyebrow">Bridge · 从单点到平台</span>

# 过渡：从单点提效到平台沉淀

<div class="columns">
<div>

**前面 7 个环节已证明**
- 需求→文档，AI 均可提效 30-70%
- 但能力分散在各工具/项目中

</div>
<div style="background:#F0F7FF; border-color:#1E40AF;">

**下一步：统一沉淀**
- 能力需沉淀为**可复用平台**
- 请回看主篇 **P29 AI能力平台架构**

</div>
</div>

> <span class="metric mint">单点验证 → 平台复用</span> <small>解决“突兀”问题</small>

---

<span class="eyebrow">Team · 回归 IT 团队</span>

# AI 对康希诺 IT 团队的价值

<div class="columns">
<div>

**AI 提效**
- 工具层：需求/编码/测试提效

</div>
<div>

**团队成长**
- 能力层：判断 / 业务理解

</div>
</div>

| 维度 | 团队获得 |
|------|----------|
| **独立承接** | 从“依赖外包”到独立承接需求 |
| **人员成长** | 3个月内掌握方案对比/选型能力 |
| **知识留存** | 代码/文档归康希诺，人员流动不流失 |

> <span class="tag tag-mint">强有力的开发团队</span> · AI 是放大器，团队是根基

---

<!-- _class: lead -->

# 让 AI 成为团队的放大器

## 回到助力开发团队建设

> 详见主篇 `slide.pptx` 完整方案 · 本篇为实战证据附录
