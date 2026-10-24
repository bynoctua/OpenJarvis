# Personal JARVIS — Development Roadmap

> Personal Windows assistant built as a maintained fork of [OpenJarvis](https://github.com/open-jarvis/OpenJarvis). This roadmap describes planned extensions, not verified existing capabilities.

## Goals

Build a personal assistant capable of understanding instructions, observing the active Windows desktop with explicit consent, and carrying out permitted tasks in selected applications. Spanish voice interaction and a compact notch-style interface are later milestones.

## Rules

1. Keep `main` as a clean baseline; work on `dev/personal-jarvis` and feature branches.
2. Preserve Apache-2.0 notices and upstream attribution.
3. Check upstream changes before integrating; do not overwrite customizations.
4. Least privilege by default. Never require elevated administrator rights for normal agent operation.
5. Screen access and action execution require explicit, revocable permission. Show a visible indicator when screen capture is active.
6. Human approval for each potentially consequential action, including editing or deleting files, command execution, sending messages, sharing data, and account actions.
7. Add emergency stop, action log, dry-run previews and an allowlist of applications.
8. No secrets, tokens, screenshots, recordings, or personal data in Git history.

## Milestones

| Phase | Deliverable | Acceptance criteria |
| --- | --- | --- |
| 0. Baseline | Audit current Windows install/build/test pathways | Reproducible setup and documented test results |
| 1. Desktop capabilities | Inventory of existing UI, agents, tools and permissions | Capability matrix identifies native vs missing features |
| 2. Windows control | Approved desktop observation + narrowly scoped mouse/keyboard actions | Operates a disposable Notepad document with approval and audit trail |
| 3. AI integration | Pluggable local/cloud model selection | Compatible model works with visual/tool workflow |
| 4. Voice | Spanish speech recognition and speech output | Voice task can be completed reliably without privileged operations |
| 5. Compact UI | Notch-style optional overlay | Keyboard-accessible, dismissible and does not obscure apps |
| 6. Personal context | Local memory with inspect/delete controls | Memory has explicit retention and permission boundaries |

## First development task

Audit the fork before modifying behavior:
- Document Windows prerequisites, packaging and application entrypoints.
- Verify automated tests and build instructions.
- Inventory agent tools, model adapters and permission gates.
- Identify screen capture, UI automation and voice dependencies if present.
- Propose the smallest safe Windows-only proof of concept.

**Out of scope initially:** unattended agent control, irreversible system changes, financial transactions, automatic outbound communication, and always-on screen recording.
