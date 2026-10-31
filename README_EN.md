# calculus-tutor-skill

[简体中文](README.md) · [Illustrative demo](DEMO.md) · [Contributing](CONTRIBUTING.md) · [Validation status](evals/STATUS.md)

**Understand an AI solution, but still cannot start the next problem?**

A calculus tutoring skill for university students. It helps an AI tutor identify where understanding breaks down, explain why a method comes to mind, and hand a meaningful next step back to the student.

The project grew out of its initiator's experience learning calculus with AI. Its central question is: **why did the student not think of this step?**

Status: preparing an unpublished `v0.1.0-alpha` preview. The entry-point format has been checked. A native mode-selection round trip and a short practice-mode interaction have been observed in the development chat. Full behavioral evaluation, cross-host compatibility, and learning outcomes remain unverified. Public examples are illustrative. Licensed under the [MIT License](LICENSE), copyright 2026 `zeyu-chen-dev`.

## Try it

1. Download or clone the repository, keeping `SKILL.md` and its supporting files together.
2. Ask a file-capable AI agent to read `SKILL.md`. In a plain chat environment, provide its body and the references relevant to your task manually.
3. Send a problem and choose a mode, or specify the mode in the first message. The mode stays active in that conversation until you change it.

Example request:

> Read SKILL.md in this folder and tutor me in practice mode, in English. Find lim(n→∞) (2^n+3^n)/(3^n+1). I can divide the numerator and denominator by 3^n, but I do not understand why I should think of doing that. Start with that difficulty.

This repository contains instructions and references; it does not require running an application or configuring an API key. File access, native choice controls, and persistent memory depend on the host. The core instructions and most reference material currently use Chinese; this English overview is not a full translation of the skill.

## Six modes

| Mode | Output |
| --- | --- |
| `beginner` | Explain required concepts and guide the student through manageable steps. |
| `practice` | Connect recently learned material to problem recognition and technique. |
| `master` | Keep basics concise, compare approaches, and label advanced extensions. |
| `deadliner` | For last-minute exam preparation: usable patterns, techniques, and complete worked solutions. |
| `previewer` | Introduce concepts and prerequisite connections through simple examples. |
| `straight` | Only a complete, copy-ready standard solution, without tutoring commentary. |

The first problem in a new conversation triggers mode selection unless a mode is already specified. Use a native single-choice prompt when the host permits it; otherwise use a numbered text menu. A preselected option is not a submitted choice. Users can change modes at any time; the tutor does not change modes on its own.

`straight` includes necessary calculations, case distinctions, and proof statements. It does not mean returning only the final value. Every mode must preserve mathematical correctness and applicable conditions.

## What guides the tutoring

- Distinguish calculation trouble, formula understanding, justification, and method selection.
- Explain both why a step is valid and why it is useful here.
- Return to the exact point a student identifies as confusing.
- Increase support when a hint is not enough; avoid endless questioning.
- Treat structural signals as candidate methods with conditions, including cancellation risks in equivalent infinitesimals.
- Distinguish assisted completion from independent transfer when organizing revision.

These tutoring behaviors apply according to the chosen mode. `deadliner` prioritizes patterns and worked solutions; `straight` follows its strict output contract.

## Files

- [SKILL.md](SKILL.md): authoritative tutoring instructions.
- [patterns.md](patterns.md): structural signals, candidate methods, conditions, and small student tasks.
- [mistakes.md](mistakes.md): common tutoring failures and corrections.
- [review-mode.md](review-mode.md): weak-point records, deferred problems, and revision.
- [DEMO.md](DEMO.md) and [examples/](examples/README.md): clearly labeled illustrative material.
- [evals/scenarios.md](evals/scenarios.md) and [evals/STATUS.md](evals/STATUS.md): intended checks and actual validation limits.

The first topic focus is limits and infinitesimals. Derivatives and integrals are planned expansions. There is no measured learning-effectiveness claim or universal host-compatibility claim.

## Contribute

Useful feedback describes a specific point where a mathematically correct answer failed to help the learner. Include the selected mode, the intended behavior, the observed behavior, and a minimal example you have permission to share. See [CONTRIBUTING.md](CONTRIBUTING.md).

Private learning records and raw conversations should stay out of public contributions. Persistent storage requires actual host support and the student's agreement.

If the project helps you, consider starring it, reporting a concrete failure, or contributing a pattern with its limits of applicability.

Licensed under the [MIT License](LICENSE). GitHub publication is pending. See [PUBLISHING.md](PUBLISHING.md) for the proposed preview release.
