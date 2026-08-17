# AGENTS.md

## Project purpose

本仓库（cansino）用于创建「康希诺（CanSino Biologics）数字化落地方案」文档 — a digital implementation/落地 plan for CanSino.

- 主要交付物：数字化落地方案文档，存放于 `docs/`。
- 参考输入：仓库根目录的 `intro.docx` 与 `artifact.pptx` 是用户提供的既有资料，方案起草前必须通读。
- 当前阶段：交互式设计（interactive design）—— 与用户澄清方案范围、文档形态、技术栈与时间框架；需求确定后再起草正文。
- 文档语言：中文；技术名词保留英文惯用写法。
- 若后续进入原型/实施：先确认技术栈，并把真实 build/test 命令记录到本文件（替换下方 Repo state 的状态说明）。

## Repo state

No source code, no manifests, and no build/test/lint configuration. Verified facts:

- Git initialized 2026-08-17 (branch `main`) to track the document deliverable; no code toolchain exists — no build/test/lint commands.
- Deliverable structure: `docs/康希诺数字化落地方案.md`（主文档）+ `docs/diagrams/*.mmd`（可编辑架构图源文件）。
- Work layout: `.omo/research/`（事实核查研究输入）、`.omo/drafts/`（章节草稿、样式规范与验收清单，作为事实纪律证据链保留）、`.omo/` 为 OpenCode agent session state — 不属于最终交付物。

## Working rules for this repo

- Do not assume or invent a toolchain (language, framework, package manager, test runner). None exists yet. When the user asks to scaffold, confirm the stack first, then update this file with the real commands.
- There are no build, test, lint, or typecheck commands to run. Do not guess them — once a manifest (`package.json`, `go.mod`, `pyproject.toml`, etc.) appears, derive commands from that file and record them here.
- Treat this file as living documentation: the first session that adds real tooling must replace this "Repo state" section with the verified commands and structure.
