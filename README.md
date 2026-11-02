<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/banner-dark.svg">
  <img src="assets/banner-light.svg" width="100%" alt="Michael Blauberg: Technical Co-founder and Lead Engineer at App Stack. Agentic engineering.">
</picture>

I'm the Technical Co-founder and Lead Engineer of App Stack Pty Ltd, where I lead
development of [Sealle](https://sealle.com.au), practice management software for
accounting firms. I'm based in Brisbane.

Most of my engineering now runs through coding agents. My job is the system
around them: the specs, tests, review gates and routing that let agents do real
product work. My personal harness for this is
[Provenant](https://github.com/mblauberg/provenant).

## How I work with agents

- **Spec first.** Work starts with acceptance criteria and a risk tier before
  an agent writes code.
- **Isolated writers.** Each agent writes in its own git worktree, one writer per
  worktree, sandboxed to the paths it was given.
- **Review scales with risk.** Routine changes need passing checks. Larger
  changes get independent review, by a different model family from the author
  where one is available, and the riskiest need my sign-off before merge.
- **Right model for the task.** Work is routed by difficulty and remaining quota
  across Claude, Codex and other providers.
- **Knowledge in the repo.** Lasting decisions go in `AGENTS.md`, ADRs and
  runbooks, where the next agent will find them, not in chat history.

## Provenant

[**Provenant**](https://github.com/mblauberg/provenant) is my open-source
(MIT) agent harness. From a Claude Code, Codex, Cursor, Agy or OpenCode session,
it hands tasks to other agents. For each task it picks a model, checks account
quota, runs the agent in a sandboxed worktree and keeps a full record of the run.

- 20 workflow skills (scope, implement, diagnose, code review, release and more)
  and 8 library skills.
- Presets for fan-out research, review councils, generator–evaluator loops and
  CI-gated delivery.
- Fabric, a layer for passing messages, tasks and claims between agent sessions,
  including on other machines.
- Written in Rust and released under semantic versioning (currently v1.4.2).
  I develop it using Provenant itself.

## Selected work

- [**PureMouse**](https://github.com/mblauberg/PureMouse): a native, offline
  alternative to Logi Options+ on macOS. It talks HID++ directly to Logitech MX
  mice and handles button mapping, gestures, smooth scrolling, DPI and per-app
  profiles in under 20 MB of memory. Built in Swift 6 with no third-party
  dependencies.
- [**RAG-as-a-Service**](https://github.com/mblauberg/rag-as-a-service):
  answers questions about uploaded documents and cites its sources. Retrieval
  combines Postgres keyword search with Qdrant vector search, merges the results
  with reciprocal rank fusion and reranks them with a cross-encoder. It runs as
  containerised FastAPI and React services, with Kubernetes manifests.
- [**My Boardgame Collection**](https://github.com/mblauberg/my-boardgame-collection):
  a full-stack app built with React 19, TypeScript and Supabase. It has passkey
  sign-in, row-level security and BoardGameGeek integration, and is
  [live on Vercel](https://my-boardgame-collection.vercel.app).
- [**Table tennis stroke classification**](https://github.com/mblauberg/table-tennis-ml-classification):
  classifies strokes from IMU sensor data. Train and test sets are split by
  player so no player's data leaks between them. The tuned random forest
  reaches a macro F1 of 0.957 on held-out players.

### Earlier team projects

- **GlassChain**: a read-only blockchain wallet intelligence system. It is a
  TypeScript monorepo with CI and load testing, deployed on AWS. I designed its
  microkernel plugin architecture. (Private repo.)
- **Nova Edge**: an underwater glider simulator in Unreal Engine (C++), built
  for Flying Fish Technologies. I built the physics: hydrodynamics,
  PID-controlled attitude and spring-damper cable towing. (Private repo.)
- [**Beast Breakout**](https://github.com/UQcsse3200/2024-studio-1): a Java and
  libGDX game built by more than 40 developers. I merged 19 pull requests
  covering NPC and boss AI, effects, refactoring and tests.

## Tools I reach for

Rust · TypeScript · React · TanStack · Swift (macOS) · Python · PostgreSQL ·
AWS · Cloudflare · Claude Code · Codex

I choose languages with strict types and fast compilers and test runners. They
give agents quick, clear feedback when something is wrong.

---

[LinkedIn](https://www.linkedin.com/in/mblauberg/) ·
[Sealle](https://sealle.com.au) ·
[Provenant](https://github.com/mblauberg/provenant)
