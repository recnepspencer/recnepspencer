# Spencer Hepworth

I build software systems for scaling AI engineering without blindly trusting model output.

My main project is **Worth** — a multi-million-line Rust/WebAssembly platform designed to let humans and AI agents safely build and modify software far beyond normal application complexity.

Today I run parallel AI engineering workflows producing roughly **60–80 aggregate agent-hours of software work per day**. The hard problem is no longer generating code. It is making that amount of generated work safe to accept.

Worth attacks that problem at the infrastructure layer.

It includes:

- **Authoritative state and history** — MVCC, snapshots, branching, lineage, replay, transactional state, and change propagation
- **Incremental computation** — dependency tracking, fine-grained invalidation, reactive execution, and deterministic recomputation
- **Database/storage infrastructure** — WAL, bounded buffer management, durability, crash recovery, and physical verification
- **Typed application runtime** — explicit authority, queries, state transitions, idempotency, and recovery
- **Rust/WebAssembly delivery** — browser integration, React bindings, and native UI infrastructure
- **AI verification infrastructure** — independent test oracles, specialized reviewers, architecture contracts, and adversarial certification

The verification side is especially important.

I build tests designed to break implementations that merely *look* correct: crash seams, fresh-process recovery, invalid-authority scenarios, mutation tests, independently derived oracles, and replayable evidence.

The goal is to keep **implementation and proof of correctness decoupled**. AI agents can generate enormous amounts of work, but they do not get to decide whether their own work is correct.

I’m applying the same philosophy to regulated software and engineering systems. One system I built reduced an **~80-hour medical-device software validation process to ~20 minutes of quality review** by mechanically linking SOP requirements to exact code enforcement points, executable tests, and evidence.

Long term, I’m interested in software where AI can safely operate on much harder domains — CAD, physical systems, simulation, mathematics, and other software where “looks right” is nowhere near good enough.
