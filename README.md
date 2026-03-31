# 六层 AI Skill 体系 · AI Skill System

> **六个专职 AI 角色协作，覆盖 AI 项目从立项到上线的完整链路**
>
> System v1.2.0 · MIT License · 平台无关（GPT / Claude / 文心 / 通义 / 星火 / Gemini / CodeBuddy）

---

## 🚀 30 秒了解全貌

**[👉 点击查看在线思维导图](https://letplaylimited-mark.github.io/ai-skill-system/mindmap.html)** — 六个 Skill 的价值、使用时机、激活词、完整流程，一图全览。

---

## 体系架构

```
用户需求
   ↓
Skill 00 · Navigator      L0 路由层    → 意图识别，路由到正确 Skill
   ↓
Skill 01 · 超级提示词工程师  L1 理解层  → 设计/优化系统提示词
Skill 02 · SOP 工程师       L1 理解层  → 将想法工程化为 Skill 工程包
Skill 03 · Scout            L1 理解层  → 七维度开源技术选型
   ↓
Skill 04 · Planner          L2 构建层  → 生成 Phase/Task/Step 操作手册
   ↓
Skill 05 · Validator        L3 验收层  → 五维度质量验收 + 发布决策
   ↓
可发布的 AI 项目
```

---

## 📦 快速安装（CodeBuddy 用户）

```bash
# 克隆体系仓库
git clone https://github.com/letplaylimited-MARK/ai-skill-system.git

# 安装所有新 Skill 到 CodeBuddy
cp -r skill-00-navigator ~/.codebuddy/skills/
cp -r skill-03-scout     ~/.codebuddy/skills/
cp -r skill-04-planner   ~/.codebuddy/skills/
cp -r skill-05-validator ~/.codebuddy/skills/
```

> Skill 01（超级提示词工程师）和 Skill 02（SOP 工程师）已独立发布，见下方各仓库链接。

---

## 六个 Skill 详情

| Skill | 名称 | 核心职责 | 使用时机 | 仓库 |
|---|---|---|---|---|
| 00 | Navigator · 导航官 | 意图识别，路由到正确 Skill | 不知道从哪开始时 | [skill-00-navigator](https://github.com/letplaylimited-MARK/skill-00-navigator) |
| 01 | 超级提示词工程师 | 设计/优化系统提示词 | 提示词效果不好时 | [super-prompt-engineer-skill](https://github.com/letplaylimited-MARK/super-prompt-engineer-skill) |
| 02 | SOP 工程师 | 将想法打包为 Skill 工程包 | 想把提示词/想法工程化时 | [skill-dev-sop-skill](https://github.com/letplaylimited-MARK/skill-dev-sop-skill) |
| 03 | Scout · 开源侦察官 | 七维度开源方案评估 | 需要找开源库/技术选型时 | [skill-03-scout](https://github.com/letplaylimited-MARK/skill-03-scout) |
| 04 | Planner · 执行规划官 | 生成分阶段操作手册 | 需要把 SOP 落地执行时 | [skill-04-planner](https://github.com/letplaylimited-MARK/skill-04-planner) |
| 05 | Validator · 验收工程师 | 五维度质量验收 + 发布决策 | 项目上线前质量检查时 | [skill-05-validator](https://github.com/letplaylimited-MARK/skill-05-validator) |

---

## ⚡ 激活卡速查（复制到 AI 对话开头即可激活）

### Skill 00 · Navigator（不知道从哪开始？先用这个）

```
你是 Navigator，一个 AI Skill 路由引擎。用户输入意图后，你分析置信度并路由到正确 Skill（01需求分析/02SOP工程/03开源侦察/04执行规划/05测试验收）。置信度≥80%直接路由，60-79%先确认，<60%追问（≤3次）。输出标准化交接包YAML。禁止直接执行任务，只做路由。
```

### Skill 03 · Scout（找开源方案）

```
你是开源技能侦察官(v1.0.0)。将项目需求转化为开源技能选型方案，七维度评估（功能性30%/易用性20%/性能15%/可维护性10%/社区活跃度10%/兼容性10%/文档5%），输出标准交接包。4阶段：需求理解→开源搜索→七维评估→交接包输出。规则：实时数据标注[需用户核实]；门控不跳阶；技术栈未知必追问；找不到方案直言+3条降级路径。
```

### Skill 04 · Planner（生成操作手册）

```
你是AI项目执行规划官(v1.0.0)。将SOP工程包转化为分阶段操作手册，4阶段：SOP解析→Phase/Task/Step三层拆解（P1-T2-S3格式）→手册生成（含环境配置/检查点/断点恢复/FAQ）→交接包输出。版本号/API限制标注[需用户核实]，估时标注[估算]，不修改SOP技术决策，不跳阶。
```

### Skill 05 · Validator（验收上线）

```
你是AI项目测试验收工程师(v1.0.0)。执行五维度验收测试（功能40%/文档25%/可执行性20%/接口规范10%/安全5%），生成PASS/CONDITIONAL_PASS/FAIL发布决策。P0缺陷立即FAIL，P0=0且P1≤3且综合≥70%为CONDITIONAL_PASS，P0=0且P1=0且综合≥80%为PASS。所有缺陷必须有证据，输出飞轮改进建议。
```

---

## 🔁 常见使用路径

| 你想做什么 | 推荐路径 |
|---|---|
| AI 智能体从零开发 | 00 → 03 → 02 → 04 → 05 |
| 只需技术选型 | 03 → [04] |
| 提示词优化并打包 | 01 → 02 |
| 已有 SOP，生成操作手册 | 04 → 05 |
| 项目已完成，验收发布 | 05 |
| 不确定从哪里开始 | 00 |

---

## 📋 如何使用

### 方式一：在任意 AI 平台使用（无需安装）

1. 从上方「激活卡速查」复制对应 Skill 的激活提示词
2. 打开你使用的 AI 平台（ChatGPT / Claude / 文心 / 通义等），**新建一个对话**
3. 将激活卡内容粘贴到对话框发送
4. AI 回应激活确认后，描述你的需求开始工作
5. 完成后复制输出的「交接包 YAML」，粘贴到下一个 Skill 的对话开头

> **重要**：每个 Skill 请使用独立对话窗口，避免角色混淆。

### 方式二：CodeBuddy 用户直接调用

安装完成后，在 CodeBuddy 中直接输入触发词即可激活对应 Skill，无需手动粘贴激活卡。

---

## 📄 体系文档

| 文档 | 说明 | 链接 |
|---|---|---|
| 完整使用手册 | 9章节详细使用指南，含 FAQ | [USER-GUIDE.md](./USER-GUIDE.md) |
| 超级系统提示词 | 统一激活六个角色的 Meta-Prompt | [SUPER-SYSTEM-PROMPT.md](./SUPER-SYSTEM-PROMPT.md) |
| 交互式思维导图 | 可视化体系全貌（在线预览） | [mindmap.html](https://letplaylimited-mark.github.io/ai-skill-system/mindmap.html) |
| 接口契约 | 六个 Skill 间的数据交换协议 | [interface-contracts/](./interface-contracts/) |
| 集成测试报告 | 端到端链路验证报告（PASS，91.9/100） | [e2e-integration-test-report.md](./system/e2e-integration-test-report.md) |
| 体系变更日志 | System 版本历史 | [system-changelog.md](./system/system-changelog.md) |

---

## 🔗 交接包说明

Skill 之间通过「交接包（Handoff Payload）」传递上下文，格式为 YAML，结构如下：

```yaml
handoff:
  schema_version: "1.0"
  from_skill: "skill-XX-name"
  to_skill: "skill-YY-name"
  payload:
    # 核心数据（各 Skill 不同）
  user_action: "下一步操作说明"
  created_at: "YYYY-MM-DD"
```

完整模板见 [SUPER-SYSTEM-PROMPT.md · Part 7](./SUPER-SYSTEM-PROMPT.md)。

---

## ⚠️ 已知限制

| 限制 | 说明 | 建议 |
|---|---|---|
| 手动传递交接包 | Skill 间需用户复制粘贴 YAML | 保存每步输出，未来 v2.0 自动化 |
| 跨会话无记忆 | 中断后需重新提供上下文 | 保存交接包到本地文档 |
| 开源数据需核实 | Star 数/版本号由 AI 生成，可能不准 | 重要决策前访问 GitHub 核实 |
| 建议独立对话 | 同一对话切换多个 Skill 可能混淆 | 每个 Skill 开新对话 |

---

## 🖥️ Web 操作平台

本体系已配套开发了完整的 Web 应用，将六层 Skill 串联为可视化流水线：

**[ai-skill-web-app](https://github.com/letplaylimited-MARK/ai-skill-web-app)** — Next.js 16 + Prisma + PostgreSQL

- 五种执行模式（全自动 / 逐步审核 / 圆桌预检）
- 六角色圆桌审议机制（P0 风险门控）
- 步进式交接包审批与编辑
- JSON + Markdown 双格式报告导出
- 内置 OpenCode / Claude Code 智能体引导文件（`AGENT.md`）

> 适合本地部署后，配合 OpenCode 等本地 AI 编码工具继续迭代。

---

## License

MIT License · 完全免费，可商用

---

*维护者：[letplaylimited-MARK](https://github.com/letplaylimited-MARK)*
*System v1.5.0 · 2026年*
