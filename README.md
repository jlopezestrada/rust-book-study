# Rust Programming Language Study Examples

## Overview
This repository serves as a practical study guide and implementation environment for [The Rust Programming Language](https://doc.rust-lang.org/book/). It contains the practice code, chapter examples, and project solutions developed while working through the text.

## Project Structure
The repository is organized as a Cargo Workspace. This architectural choice ensures that each chapter, exercise, or major project remains strictly isolated as an independent package (crate) within its own subdirectory. This isolation prevents dependency conflicts and reflects idiomatic Rust project management.

## Compilation and Execution
As a Cargo Workspace, builds and tests can be executed globally across all packages or isolated to specific projects. Ensure you have the standard Rust toolchain installed (via rustup) before proceeding.

### Global Commands
Run these commands from the root directory to affect all workspace members:
*   Build the entire workspace:
    ```sh
    cargo build
    ```
*   Execute all tests across all packages:
    ```sh
    cargo test
    ```
*   Validate the codebase without compiling:
    ```sh
    cargo check
    ```

### Package-Specific Commands
To target an individual chapter's code, use the `-p` (package) flag followed by the crate name defined in its respective `Cargo.toml`.
*   Run a specific chapter (e.g., Chapter 2's Guessing Game):
    ```sh
    cargo run -p ch02_guessing_game
    ```

## Extending the Workspace
To create a new project for a subsequent chapter, initialize a new package within the root directory:
```sh
cargo new ch03_common_concepts
```
Cargo will automatically append the newly created directory to the `[workspace.members]` array in the root `Cargo.toml`.

## License
This repository contains my personal practice code and solutions based on The Rust Programming Language book. 

The original code examples are (c) The Rust Project Developers and are licensed under the MIT/Apache 2.0 licenses.