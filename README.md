# Steelman Decision

[English](#english) | [简体中文](#简体中文)

## English

A two-phase agent skill for dual steelman analysis and one-question decision calibration.

It reconstructs the real problem, audits hidden assumptions, builds the strongest case both for and against the current idea, identifies the variables most likely to change the conclusion, and asks exactly one decisive question. It waits for the answer before giving a clear judgment and next action.

### Why this skill exists

Decision prompts often fail in one of two ways:

- they answer too early and inherit the user's untested assumptions;
- they ask a long list of questions without identifying which uncertainty actually matters.

Steelman Decision uses a stricter contract: analyze both sides, ask one high-value question, stop, then judge after the reply.

### Use it for

- product and strategy choices;
- architecture and technical trade-offs;
- business and resource-allocation decisions;
- career and operating decisions;
- explicit requests for dual steelman or adversarial analysis.

Do not use it for simple facts, routine edits, or tasks where the decision is already settled and only execution remains.

### How it works

#### Phase 1 — Analyze, ask, stop

1. Reconstruct the real problem.
2. Separate facts, inferences, and missing information.
3. Steelman the strongest case for and against.
4. Identify the real disagreement and decisive variables.
5. Ask exactly one decision-changing question and stop.

#### Phase 2 — Judge and act

1. Update the assumptions from the answer.
2. Give a clear judgment.
3. Explain the reasons and strongest remaining objection.
4. Recommend the smallest useful next action.
5. State what evidence would change the judgment.

### Installation

Install with the Skills CLI:

```bash
npx skills add https://github.com/aiirux-opc/steelman-decision
```

Or clone it directly into Codex:

```bash
git clone https://github.com/aiirux-opc/steelman-decision.git \
  ~/.codex/skills/steelman-decision
```

### Usage

```text
$steelman-decision I am considering replacing our services business with a standard SaaS product. Stress-test the decision before recommending a direction.
```

The first response performs the analysis and ends with one question. After the user replies, the second response gives the judgment and action plan.

## 简体中文

一个用于“双向钢人论证”和“单问题决策校准”的双阶段 Agent Skill。

它会重新梳理真正需要解决的问题，检查未经验证的默认假设，分别构建支持与反对当前想法的最强论证，找出最可能改变结论的关键变量，并且只提出一个决定性问题。收到回答后，它才会给出明确判断和下一步行动。

### 为什么需要这个 Skill

常见的决策类 Prompt 容易走向两个极端：

- 过早回答，直接继承用户尚未验证的前提；
- 提出大量问题，却没有识别真正影响结论的不确定性。

Steelman Decision 使用更严格的交互契约：先分析正反双方，只问一个高价值问题并停止，等用户回答后再完成判断。

### 适用场景

- 产品方向和战略选择；
- 架构方案和技术权衡；
- 商业判断和资源分配；
- 职业发展和经营决策；
- 用户明确要求双向钢人论证或反证分析。

它不适用于简单事实查询、常规修改，以及已经完成决策、只剩具体执行的任务。

### 工作方式

#### 第一阶段——分析、提问、停止

1. 重构真正需要解决的问题；
2. 区分事实、推断和缺失信息；
3. 分别构建支持与反对的最强论证；
4. 找出真正分歧和决定性变量；
5. 只问一个足以改变结论的问题，然后停止。

#### 第二阶段——判断与行动

1. 根据用户回答更新关键假设；
2. 给出明确判断；
3. 说明理由和仍然成立的最强反对意见；
4. 推荐最小但有效的下一步行动；
5. 说明什么新证据会改变当前判断。

### 安装

通过 Skills CLI 安装：

```bash
npx skills add https://github.com/aiirux-opc/steelman-decision
```

或者直接克隆到 Codex：

```bash
git clone https://github.com/aiirux-opc/steelman-decision.git \
  ~/.codex/skills/steelman-decision
```

### 使用

```text
$steelman-decision 我正在考虑把项目制定制业务转成标准 SaaS。先做双向钢人论证，只问我一个关键问题，等我回答后再判断。
```

第一次回复会完成分析，并以一个关键问题结束。用户回答后，第二次回复再给出判断和行动方案。

## License / 许可证

[MIT](LICENSE)
