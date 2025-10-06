# Assemblers
[Wikipedia](https://en.wikipedia.org/wiki/Assembly_language#Assembler)

Assemblers, 汇编引擎

- [→iced](#iced)
- [→Intel XED](#intel-xed)
- [→LLVM](#llvm)

Assembling-only:
- [Keystone assembler framework: Core (Arm, Arm64, Hexagon, Mips, PowerPC, Sparc, SystemZ & X86) + bindings](https://github.com/keystone-engine/keystone)

  [Keystone -- The Ultimate Assembler](http://www.keystone-engine.org/)

  - [keystone-engine/keypatch: Multi-architecture assembler for IDA Pro. Powered by Keystone Engine.](https://github.com/keystone-engine/keypatch)

- FASM
- NASM
- MASM
- TASM
- CE

  汇编器没有单独打包

  [CeAutoAsm-x64dbg Plugin - atom0s.com](http://atom0s.com/forums/viewtopic.php?f=2&t=206&sid=94b23e2b89491cd398abf57e098c110f)

  https://github.com/atom0s/CeAutoAsm-x64dbg

- [x64dbg/XEDParse: A MASM-like, single-line plaintext assembler](https://github.com/x64dbg/XEDParse) (discontinued)

  停止更新

  指令集支持似乎不佳，连 movss 都不支持
- [StanfordPL/x64asm: x86-64 assembler library](https://github.com/StanfordPL/x64asm) (discontinued)
  - Rust: [jxors/x64asm-rs: Rust bindings for x64asm](https://github.com/jxors/x64asm-rs)
- [Midi12/cx\_assembler: A c++20 constexpr x86 assembler](https://github.com/Midi12/cx_assembler) (discontinued)
- OD
- VMProtect

[Comparison of assemblers - Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_assemblers)

[\[原创\]各种开源汇编、反汇编引擎的非专业比较-『软件逆向』-看雪安全论坛](https://bbs.pediy.com/thread-205590.htm)

[2 assembler & 2 disassembler\_运维\_Starr - CSDN 博客](https://blog.csdn.net/Ga4ra/article/details/101533322)

[如何编写将汇编代码翻译成机器码的程序？ - 知乎](https://www.zhihu.com/question/26659135)

[\[求助\]谁能推荐一个强大的反汇编及汇编引擎-『软件逆向』-看雪安全论坛](https://bbs.pediy.com/thread-149956.htm)

## Benchmarks
N/A，比解码应该性能差异小得多。

## JIT
- [AsmJit: Low-latency machine code generation](https://github.com/asmjit/asmjit)

  > Complete x86/x64 JIT and AOT Assembler for C++

  [谈谈AsmJit - \_懒人 - 博客园](https://www.cnblogs.com/lanrenxinxin/p/5021641.html)

- [Xbyak: a JIT assembler for x86(IA-32)/x64(AMD64, x86-64) MMX/SSE/SSE2/SSE3/SSSE3/SSE4/FPU/AVX/AVX2/AVX-512 by C++ header](https://github.com/herumi/xbyak)
- [DynASM](https://luajit.org/dynasm.html)
  - Rust: [dynasm-rs: A dynasm-like tool for rust.](https://github.com/CensoredUsername/dynasm-rs)

## Rust
- [→iced](#iced)
- [playX18/asmkit: Assembler toolkit: encoding and decoding of various architectures](https://github.com/playX18/asmkit) (discontinued)
  - JIT

  [asmkit: assembler and disassembler for X64, RISCV64, ARM64(WIP) and potentially more architectures : r/rust](https://www.reddit.com/r/rust/comments/1gpnw1e/asmkit_assembler_and_disassembler_for_x64_riscv64/)
  > The only noticeable difference is probably how API is done: Iced has kind of Intel-syntax API where you use correct registers to determine reigster size e.g EAX is 32-bit and RAX is 64-bit register and asmkit has `mov64`,`mov32` etc and also has a postfix of `rr` for register-register operation, `rm` for register-memory and so on. In Iced you would write `asm.mov(RAX, RDI)` and in asmkit: `asm.mov64rr(RAX, RDI)`.
- [abgros/awsm: A simple and beginner-friendly assembler for x86-64](https://github.com/abgros/awsm)

  [I'm creating an assembler to make writing x86-64 assembly easy : r/rust](https://www.reddit.com/r/rust/comments/1kdv1w1/im_creating_an_assembler_to_make_writing_x8664/)
- [Cr0a3/asc: The compiler for the ASM++ language](https://github.com/Cr0a3/asc)

[Suggestions for Rust crates to generate x86 Assembly (for a small compiler) : r/rust](https://www.reddit.com/r/rust/comments/13xip0c/suggestions_for_rust_crates_to_generate_x86/)

## .NET
- [AsmArm64: The most powerful ARM 64 (v8, v9) Assembler / Disassembler for .NET](https://github.com/xoofx/AsmArm64)

## Intel XED
[intelxed/xed: The X86 Encoder Decoder (XED), is a software library for encoding and decoding X86 (IA32 and Intel64) instructions](https://github.com/intelxed/xed)

- Rust
  - [xed-sys: Rust FFI bindings for Intel XED](https://github.com/rust-xed/xed-sys)
    - [libLISA/rusty-xed: High-level, safe, bindings for XED](https://github.com/libLISA/rusty-xed)
  - [roeeshoshani/xed-sys2](https://github.com/roeeshoshani/xed-sys2)

## [iced](https://github.com/icedland/iced)
> Blazing fast and correct x86/x64 disassembler, assembler, decoder, encoder for Rust, .NET, Java, Python, Lua

- The same author of dnSpy
- Have even Java and Lua bindings, but no C/C++.
- [icedland/iced-cpuid: Shows CPUID features and instruction encodings used by x86/x64 binaries](https://github.com/icedland/iced-cpuid)
- [backengineering/iced: private ice fork](https://github.com/backengineering/iced)

## LLVM
- [Nyxstone: assembly / disassembly library based on LLVM, implemented in C++ with Rust and Python bindings, maintained by emproof.com](https://github.com/emproof-com/nyxstone)

## Tools
Web:
- [Online x86 and x64 Intel Instruction Assembler](https://defuse.ca/online-x86-assembler.htm)
