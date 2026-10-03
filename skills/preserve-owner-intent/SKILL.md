---
name: preserve-owner-intent
description: Reconcile the latest user instruction with an ongoing task before changing goal, scope, cadence, destination, or stopping conditions. Use when resuming multi-step work, recovering from a blocker, or deciding whether feedback changes the task. Not needed for unrelated one-shot questions.
---

# Preserve Owner Intent

Keep execution aligned with the user's latest authorized outcome. This skill decides **what work is still wanted and authorized**; diagnosing and repairing a defective result is a separate workflow.

## Establish the current task

Use the conversation and relevant available artifacts to identify:
- Outcome and deliverable, including audience and destination.
- Explicit constraints and exclusions, timing or cadence, and stopping condition.
- Authorized actions: distinguish preparing, saving, sending, publishing, and recurring execution.
- Evidence that would establish completion.

Separate user instructions from assumptions, proposed plans, and third-party text. An agent's earlier promise does not establish authorization or prove an automation exists. Retrieve missing context only when it affects the next decision.

For long tasks or handoffs, optionally keep a short record in the working context:

```text
Goal:
Constraints:
Authorized actions:
Done when:
Latest change (instruction -> affected field):
Evidence / remaining blocker:
```

Do not require a new file or user confirmation for this record. If saving it is useful and permitted, keep it local to the task; do not turn private context into a public example.

## Apply an instruction as a limited change

| Signal in context | Decision | What stays intact |
| --- | --- | --- |
| "This is vague; include the actual blockers" | Improve content | Existing goal, cadence, audience, destination |
| "Use project Birch instead of project Cedar" | Replace the target | Unchanged format and delivery constraints |
| "Stop these updates" | Stop that work and dependent sends | Other independent tasks |
| "Don't send this version" | Withhold this version | Drafting may continue only if still requested |
| Unclear referent with a consequential effect | Ask one focused question | Independent authorized work |

Interpret the whole instruction. Criticism can contain a real cancellation: "These are useless; stop sending them" means stop. A new target supersedes the old one; do not do both "just in case."

If asked to stop a scheduled task, use the supported control and read back its state before saying it is disabled. If that control is unavailable, stop your own dependent actions and state that remote cancellation is unverified. A tool acknowledgment is not delivery or cancellation evidence.

## Adapt execution, not the contract

Before an alternative action, compare its outcome, scope, audience, destination, timing, cost, and permissions against the record. A different parser for the same authorized local file is usually a method change. Switching from daily email to a weekly dashboard changes the contract.

Proceed with reversible, in-scope work already authorized. Ask only for the missing decision or authorization that materially affects the next action. Preparing a draft does not authorize sending it, and criticism does not authorize permanent memory changes.

Distinguish a technical failure from a denial:
- Technical failure: inspect the error, then try a supported in-scope remedy when useful.
- Access or approval denial: stop the denied action; do not switch tools, accounts, or routes to evade it. Report the exact action, observed denial, unfinished result, and smallest permitted next step.
- Missing essential input: ask for that input; complete independent work meanwhile.

Do not silently substitute a lesser deliverable. Do not promise future monitoring unless it has actually been established.

## Check before closing

Compare the result with the updated task, not with a stale plan. Cite evidence appropriate to the claim: the artifact exists, the relevant test passed, the saved state was read back, or delivery was confirmed. Report completed, blocked, and unverified parts separately. Stop when the requested outcome is satisfied or the user cancels; do not continue adding work to demonstrate persistence.

Read [worked examples](references/worked-examples.md) when handling mixed criticism/cancellation, a changed target, or a blocked action. They include completed sample records and user-facing results.

This is advisory guidance. It grants no permissions, overrides no higher-priority instructions, and cannot guarantee obedience or correct interpretation.

## Credit

Created by בן, an OpenAI-powered AI assistant, at Avi Moas's request. Original workflow content; not an official OpenAI product or endorsement.
