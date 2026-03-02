# 🦀 Rust Playground — Yuto Abe

> Flight-mode friendly Rust lab
> For learning, experimenting, and building small but meaningful tools.

This repository is a personal Rust playground for:

* 📚 Learning Rust deeply (ownership, lifetimes, async, traits)
* 🧪 Experimenting with performance and concurrency
* 🛠 Building small CLI/TUI tools useful for ASR / MLOps research
* 🚀 Prototyping future production-grade systems in Rust

---

# 📂 Directory Structure

```
rust-playground/
├── Cargo.toml          # Workspace definition
├── snippets/           # Small isolated experiments
│   └── rust-by-example/
├── katas/              # Algorithm & competitive practice
│   └── atcoder/
├── mini-projects/      # Practical tools & utilities
│   └── cli-todo/
├── bench/              # Performance experiments
├── notes/              # Markdown learning notes
└── README.md
```

---

# 🧱 Workspace Setup

This repository uses a Cargo workspace.

### Root `Cargo.toml`

```toml
[workspace]
members = [
  "mini-projects/cli-todo",
  "snippets/rust-by-example",
  "katas/atcoder",
]
resolver = "2"
```

---

# 🛠 Development Commands

Run from the root:

```bash
# Format all crates
cargo fmt

# Lint strictly
cargo clippy --workspace --all-targets -- -D warnings

# Run tests
cargo test --workspace

# Build everything
cargo build --workspace

# Run specific project
cargo run -p cli-todo
```

---

# 🎯 Learning Goals

This playground focuses on:

## 1️⃣ Core Rust Mastery

* Ownership & borrowing
* Lifetimes
* Traits & generics
* Pattern matching
* Error handling (`Result`, `thiserror`, `anyhow`)

## 2️⃣ Systems-Level Thinking

* Zero-cost abstractions
* Memory layout awareness
* Performance profiling
* Benchmarking

## 3️⃣ Concurrency & Async

* `rayon` (data parallelism)
* `tokio` (async runtime)
* Channels & synchronization

## 4️⃣ Practical Tooling

* `clap` for CLI
* `serde` for JSON
* `csv`
* `reqwest`
* `axum` (future web experiments)
* `ratatui` (TUI experiments)

---

# 🧪 Planned Mini Projects

## 1. 📊 jp-corpus-stats (ASR Utility)

CLI tool to analyze:

* Character distribution
* Token frequency
* Length statistics
* Overlap ratio
* Dialogue turn statistics

Useful for:

* FD-Bench Japanese experiments
* Corpus property analysis
* MLOps preprocessing validation

---

## 2. 📝 Research Log Formatter

* Input: JSON/CSV experiment logs
* Output: Markdown summary tables
* Future: automatic experiment report generation

---

## 3. ⚡ Parallel File Analyzer

* Process large corpora using `rayon`
* Benchmark sequential vs parallel performance

---

## 4. 🖥 TUI Missed Question Viewer

Terminal UI version of:

* `missed_questions`
* Lightweight local viewer before Supabase integration

---

# ✈️ Flight Mode Study Plan

When offline:

### Day 1

* Ownership deep dive
* Write examples in `snippets/`
* Implement custom iterator

### Day 2

* Build simple CLI with `clap`
* Parse JSON with `serde`
* Output formatted results

### Day 3

* Add parallel processing
* Benchmark improvements
* Refactor using traits

---

# 🧠 Why Rust?

Rust is interesting for future:

* High-performance MLOps tooling
* Data preprocessing pipelines
* Real-time systems
* Backend microservices
* Safe concurrent systems

Long-term possibility:

* ASR inference server in Rust
* Dialogue evaluation backend
* High-performance data pipeline tools

---

# 🧾 Notes

Learning notes go in:

```
notes/
```

Recommended format:

```
2026-03-Flight-Notes.md
ownership-deep-dive.md
async-vs-thread.md
```

---

# 🚀 Future Expansion

Potential future directions:

* WASM experiments
* Axum-based API server
* Rust + Python bridge for ML
* CLI tool suite for speech research
* Replacing some Node utilities with Rust

---

# 📌 Philosophy

This is not just “learning Rust”.

This is:

> Systems thinking training
> Performance intuition building
> Backend engineering practice
> MLOps foundation strengthening
