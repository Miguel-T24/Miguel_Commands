# 🦀 Rust, Cargo & Rustup Commands

Quick reference guide for managing the Rust toolchain, building projects, and executing binaries across environments.

---

## 🛠️ Essential Commands Reference

| Category | Action / Description | Command (Linux / Bash) | Command (Windows / PowerShell) |
| :--- | :--- | :--- | :--- |
| **Execution** | Compile and run development build | `cargo run` | `cargo run` |
| | Compile and run with arguments | `cargo run -- arg1 arg2` | `cargo run -- arg1 arg2` |
| | Run production binary directly | `./target/release/my_app` | `.\target\release\my_app.exe` |
| **Project Lifecycle** | Create a new binary application | `cargo new my_app` | `cargo new my_app` |
| | Create a new library | `cargo new my_lib --lib` | `cargo new my_lib --lib` |
| | Check code for compilation errors (fast) | `cargo check` | `cargo check` |
| **Build & Compilation** | Build project in development mode | `cargo build` | `cargo build` |
| | Build optimized production binary | `cargo build --release` | `cargo build --release` |
| **Cleanup & Maintenance** | Remove build artifacts / `target` folder | `cargo clean` | `cargo clean` |
| **Toolchain Management** | Update Rustup tool (the manager itself) | `rustup self update` | `rustup self update` |
| | Update Rust compiler & Cargo (Stable channel) | `rustup update stable` | `rustup update stable` |
| | Update all installed toolchains (Stable, Nightly, etc.) | `rustup update` | `rustup update` |
| | Check installed versions | `rustc --version` / `cargo --version` | `rustc --version` / `cargo --version` |

---
