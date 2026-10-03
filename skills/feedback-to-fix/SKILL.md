---
name: feedback-to-fix
description: Diagnose and repair an existing result after criticism, a rejected draft, or a failed check. Use for feedback such as vague, wrong, incomplete, off-tone, or still broken. Produce a revised result and evidence; a pure cancellation needs no repair workflow.
---

# Feedback to Fix

Turn feedback into an observable correction. This skill decides **what is defective, how to repair it, and how to check the repair**. It does not redefine the user's goal.

## Diagnose against the actual result

Read the feedback, artifact, latest request, and relevant source together. Classify each material point as:
- Supported defect: identify where the result violates a requirement or source.
- Preference or new requirement: apply it to the affected part.
- Unverified claim: inspect evidence before accepting or rejecting it.
- Changed target or cancellation: update or stop the affected work before repairing anything.

Acknowledge only what the evidence supports. For false criticism, show the calculation, source, or reproduction briefly; do not introduce an error to agree. For subjective feedback, translate the preference into a concrete edit rather than pretending it has an objective score.

When "still broken" lacks enough information to reproduce, inspect available logs or artifacts first. Ask for the missing input or failing path only when it materially changes the repair.

## Choose an acceptance check before editing

Write a short check that could fail on the old result and pass on the corrected result. Use the smallest effective repair, which may require replacing a flawed approach.

| Defect | Repair | Useful check |
| --- | --- | --- |
| Vague status | Replace generalities with supported blocker, impact, next action | Each claim traces to supplied notes; unknown owner/date stays unknown |
| Incorrect total | Recompute from original inputs and units | Independent arithmetic, including the disputed row |
| Broken interaction | Reproduce the reported path and repair its cause | Run that path and one nearby unaffected path |
| Off-tone message | Change wording for the intended reader | Preserve factual claims, commitments, length, and send boundary |
| Missing requirement | Add the missing content or behavior | Check the requirement directly and one constraint the addition might disturb |

For multi-step or repeated repairs, optionally keep this record in the task context:

```text
Feedback:
Evidence and diagnosis:
Unchanged constraints:
Repair:
Acceptance check:
Observed result:
Status: proposed / applied / verified / blocked
```

Use it to track unresolved claims, not as mandatory ceremony or a substitute for doing the repair.

## Repair within authorization

Apply reversible authorized edits. Preserve unaffected requirements, including cadence, destination, audience, and stop conditions. A request to fix a draft authorizes a corrected draft, not sending it. Do not cancel a service because its quality was criticized; do honor an actual stop.

Do not expand scope, alter permissions, save lasting preferences, or make external commitments without applicable authorization. If access is denied, stop that action and report the denial. Changing tools to evade it is not a repair.

## Verify and decide what remains

Run the chosen check on the actual revised result. Inspect the check's output, not just whether it started. Check an adjacent requirement when the repair could break it.

If verification fails:
1. Use the observed failure to revise the diagnosis.
2. Make another authorized repair only when there is a concrete reason it should help.
3. Rerun the relevant check after that change.
4. Stop blind retries when no justified next fix exists, required access/input is missing, or the user cancels. Preserve useful work and report the remaining failure.

A passing syntax or format check does not prove behavior, factual accuracy, saving, or delivery. If the needed environment is unavailable, say "applied, unverified" and name the missing check. Never relabel a failed check as success.

## Return the repaired result

Provide the corrected artifact or content, the material change, and actual verification or remaining blocker. When a claim was mistaken, provide the evidence and any clarification that improves the artifact. Avoid replacing the repair with an apology or promising permanent learning.

Read [worked examples](references/worked-examples.md) for a complete vague-update repair, a disputed calculation, or an applied fix whose behavioral check fails.

This is advisory guidance. It grants no permissions, overrides no higher-priority instructions, and does not guarantee that future defects will be prevented.

## Credit

Created by בן, an OpenAI-powered AI assistant, at Avi Moas's request. Original workflow content; not an official OpenAI product or endorsement.
