---
name: steelman-decision
description: Stress-test a consequential idea, proposal, or decision by surfacing hidden assumptions, steelmanning the strongest case for and against it, isolating the decisive variables, and asking exactly one high-leverage question before giving a verdict after the user replies. Use for explicit requests for dual steelman analysis, adversarial decision review, or one-question decision calibration. Do not use for simple factual questions, routine edits, or requests already reduced to execution.
---

# Steelman Decision

Improve the quality of an important decision without turning the exchange into an endless interview. Respond in the user's language.

## Interaction Contract

Use two phases:

1. **Analysis and one question.** Examine the decision from both sides, ask exactly one decision-changing question, then stop.
2. **Judgment after the reply.** Incorporate the user's answer, make a clear judgment, and recommend the next action.

Do not give the final verdict during Phase 1. Do not ask a second question before the verdict. If the user explicitly asks to skip the question or decide immediately, give a conditional verdict from the available evidence instead.

## Phase 1: Analyze, Ask, Stop

### 1. Reconstruct the real problem

Restate the strongest, most complete version of what the user is trying to solve. Separate:

- the surface question;
- the underlying goal;
- the result that would make the decision useful.

Do not silently broaden the scope or replace the user's objective with a preferred one.

### 2. Audit the premises

Separate what is known from what is assumed:

- **Facts:** explicitly provided or verified evidence.
- **Inferences:** unstated premises, causal beliefs, forecasts, or constraints being treated as true.
- **Missing information:** unknowns that could materially change the recommendation, including how each direction would affect it.

Verify inexpensive, accessible facts with available tools instead of asking the user to retrieve them. Do not present an inference as a fact.

### 3. Steelman both sides

Present:

- **Strongest case for:** the most coherent version of the user's current position, using its best evidence and assumptions.
- **Strongest case against:** the most coherent alternative or objection, including opportunity cost and failure modes.

Do not use weak objections, moralize, or force a false 50/50 balance. Steelmanning improves each argument; it does not make them equally credible.

### 4. Identify the crux

State where the two sides actually disagree. Classify the disagreement when useful:

- facts or forecasts;
- goals or success criteria;
- risk tolerance or reversibility;
- time horizon;
- resource or opportunity cost;
- stakeholder impact.

Rank only the variables most likely to flip the decision. Also identify one common mistake that is specifically relevant to this case, not a generic warning.

### 5. Ask exactly one decisive question

Ask the single question with the highest expected value of information. A good answer should change the verdict, confidence, or next action.

The question must:

- resolve the most consequential remaining uncertainty;
- be answerable by the user rather than by accessible evidence;
- avoid bundling multiple independent questions;
- avoid asking for background that will not affect the decision.

End the response immediately after the question. Do not add a preliminary recommendation, closing summary, or extra prompt.

## Phase 2: Judge and Act

After the user answers:

1. Explain which assumptions or variables changed.
2. Give a clear judgment: proceed, reject, modify, defer, or run a bounded test.
3. Give the strongest reasons and acknowledge the strongest remaining counterargument.
4. Recommend the smallest useful next action, with a success signal and a stop or reversal condition when risk warrants it.
5. State what new evidence would materially change the judgment.

Do not restart the interview. If the answer remains incomplete, make the best conditional judgment available and label the uncertainty.

## Phase 1 Output Shape

Use this compact structure unless the user requests another format:

```markdown
## The real problem

## Premise audit
- Facts:
- Inferences:
- Missing information and impact:

## Strongest case for

## Strongest case against

## The real crux
- Decisive variables:
- Common mistake:

## One decisive question
<exactly one question>
```

## Phase 2 Output Shape

```markdown
## Judgment

## Why

## Strongest remaining objection

## Next action

## What would change the judgment
```

## Boundaries

- Do not invoke this workflow for trivial, factual, or already-decided execution requests.
- Do not turn one-question calibration into exhaustive discovery or requirements gathering.
- Do not take external actions, edit files, publish, commit, or deploy unless the user separately authorizes them.
- Do not use certainty language when the evidence supports only a conditional judgment.
