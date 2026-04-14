<div align="center">
  <h1>rustic compiler</h1>
  <p>Compile Rust into C -- no LLVM required.</p>
</div>

**rustic compiler** is an alternative Rust compilation toolchain that transpiles
Rust's MIR into portable C source code, then compiles it with a standard C
compiler (gcc or clang). This enables Rust on platforms where LLVM is
unavailable but a C11-compliant compiler exists.

The core of the project is
[`rustc_codegen_c`](https://github.com/rustic-compiler/rustc_codegen_c), a
rustc codegen backend that replaces the LLVM backend entirely. A Rust compiler
built with this backend passes **99.2%** of the official `rustc` UI test suite,
confirming high-fidelity preservation of Rust semantics at the MIR level.

## Repositories

| Repository | Description |
|---|---|
| [rustc_codegen_c](https://github.com/rustic-compiler/rustc_codegen_c) | The Rust-to-C codegen backend |
| [rust](https://github.com/rustic-compiler/rust) | Fork of rust-lang/rust with rustc_codegen_c integration |

## Getting started

See the [rustc_codegen_c](https://github.com/rustic-compiler/rustc_codegen_c)
repository for quick start instructions, supported platforms, and build guides.
