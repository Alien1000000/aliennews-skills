# AlienNews Skills | ������ ������� �� AlienNews

A small, growing collection of advisory AI-agent workflows for [AlienNews](https://aliennews.co.il).

������ ���� ������� �� ������ ����� ������ AI, ���� [AlienNews](https://aliennews.co.il).

## Catalog | �������

- [Preserve Owner Intent](skills/preserve-owner-intent/SKILL.md): Preserve the user's latest authorized goal and constraints when changing approach. Respect changed instructions and explicit cancellation.
  - ����� �� ����� ��������� �������� �� ������ �� ������ ����� �� ��� ������, ��� ����� ����� ������ ������ �����.
- [Feedback to Fix](skills/feedback-to-fix/SKILL.md): Turn feedback into focused repairs and check the actual result.
  - ����� ���� ������ ����� ������ ������ �����.

## Use | �����

Read the relevant SKILL.md before using it. Each folder under skills/ is a self-contained skill with optional agent interface metadata in agents/openai.yaml. Import or copy the chosen folder using your assistant's supported skill installation workflow. Support and invocation syntax depend on the host application.

���� �� ���� SKILL.md �� ����� ���� ������. �� ������ ��� skills/ ��� ���� �����, �� ���� ���� ����������� �?agents/openai.yaml. ����� �� ������ �� ������� ������ ������� ����� ����� ������� ������ ���� ���� ��. ������ ���� ������ ������ ������.

Example prompts for assistants that support named skills:

- Use $preserve-owner-intent to continue this task while preserving my latest goals and constraints.
- Use $feedback-to-fix to revise this draft based on my feedback, then check that the stated requirements are satisfied.

������� ������:

- ����� �?$preserve-owner-intent ��� ������ ������ ��� ����� �� ������ ��������� �������� ���.
- ����� �?$feedback-to-fix ��� ���� �� ������ ��� ����� ���, ��� ���� ���� ����� ������� �������.

## Choosing a workflow | ����� �����

| Skill | Question it answers | Practical output |
| --- | --- | --- |
| Preserve Owner Intent | What work remains wanted and authorized after a change? | Updated task constraints, correct continuation or stop, evidence of completion |
| Feedback to Fix | What is defective and how will we know the repair works? | Corrected artifact, acceptance check, observed result or blocker |

For mixed feedback, resolve the task change first, then repair the remaining result. Neither skill requires the other to be installed. Optional short records help with long tasks; ordinary edits need no extra file.

������ ������, ����� ������ ���� ����� ����� ����� �������. ������ ����, ����� �� ���� ������� ������� ��� ����. ������� �������; ���� ���� ������. ����� ��� ��� ��� ��� ������� ������, �� ����� ��� �����.

Complete synthetic examples: [intent and boundaries](skills/preserve-owner-intent/references/worked-examples.md), [repair and verification](skills/feedback-to-fix/references/worked-examples.md).

������� ����� �������: [���� ������� �����](skills/preserve-owner-intent/references/worked-examples.md), [����� ������](skills/feedback-to-fix/references/worked-examples.md).

## Testing and learning | ����� ������

[Evaluation cases and observed results](evals/README.md) distinguish a documented expectation from an actual agent run. Structural validation cannot establish semantic correctness. To improve a skill: start with a realistic failing task, define observable success, change the instruction that affects the decision, and compare fresh runs with and without it. Keep outputs, including failures; do not infer reliability from one good answer.

[���� ������ �������� �����](evals/README.md) ������� ��� ������� ����� ���� ���� ������. ����� ���� ���� ������ ������ ��� ����. ��� ���� ����: ������ ������ �������� ������, ������ ����� �����, ��� ����� ������� �� ������, ����� ����� ����� �� ����� �������. ���� �� ��������; ����� ������ ��� ���� ������ ������.

Design reference: Anthropic's [Complete Guide to Building Skills for Claude](https://resources.anthropic.com/hubfs/The-Complete-Guide-to-Building-Skill-for-Claude.pdf), especially use cases, progressive disclosure, and testing (reviewed October 3, 2026). The workflows and examples here are original; host support varies.

## Limits and safety | ������ �������

These are text-based workflow aids, not executable integrations, security controls, or guarantees of correct behavior. They do not grant permissions or override higher-priority instructions, safety rules, or user approvals. Review outputs and use only the minimum permissions needed for a task.

These files require no credentials, API keys, or account connections. This repository contains the two public skills, their synthetic worked examples, and evaluation materials. Do not add private conversations, personal records, credentials, or production configuration when contributing examples. Use fictional examples instead.

��� ������ ����� ����������, ��� ������� ������ ��������. �� ���� ������ ����� ����� ������� ������� �����. �� ���� ������� ������ ����� ������ �� ������ ������� ����� ����, ���� ������ �� ������ ������. ���� �� ������� ������� �� �� ������� ������� ������.

������ ���� ������ �������, ������ API �� ����� ��������. ����� ���� �� ��� ������� ���������, ������� ������ ������ �����. ��� ������ �������� ����� ������, ���� ����, ���� ������� �� ������ ����� �����. ������ �������� ������.

## Credit | �����

Created by ��, an OpenAI-powered AI assistant, at Avi Moas's request. Original workflow content; not an official OpenAI product or endorsement.

���� �� ��� ��, ���� AI ������ ������� OpenAI, ����� ��� ���� (Avi Moas). ���� ����� �����; ���� ���� ���� �� OpenAI ����� ���� �� ����� �� ���� �����.
