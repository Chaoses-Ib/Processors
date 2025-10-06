# Disassemblers
[Wikipedia](https://en.wikipedia.org/wiki/Disassembler)

Disassemblers (disasm), 反汇编引擎

[x86 Disassembly/Disassemblers and Decompilers - Wikibooks](https://en.wikibooks.org/wiki/X86_Disassembly/Disassemblers_and_Decompilers)

- [→iced](Assemblers.md#iced)
- [→Intel XED](Assemblers.md#intel-xed)
- [→LLVM](Assemblers.md#llvm)

Disassembling-only:
- [→Zydis](#zydis)
- yaxpeax
- [→Capstone](#capstone)

- [diStorm: Powerful Disassembler Library For x86/AMD64](https://github.com/gdabah/distorm) (discontinued)
- [bddisasm: A fast, lightweight, x86/x64 instruction decoder. The project also features a fast, basic, x86/x64 instruction emulator, designed specifically to detect shellcode-like behavior.](https://github.com/bitdefender/bddisasm)
  - Rust: [bddisasm](https://docs.rs/bddisasm/latest/bddisasm/)
- [udis86: Disassembler Library for x86 and x86-64](https://github.com/vmt/udis86) (discontinued)
  - 停止更新
  - Rust: [darfink/libudis86-sys](https://github.com/darfink/libudis86-sys)
- [BeaEngine: BeaEngine disasm project](https://github.com/BeaEngine/beaengine) (discontinued)
- [Fadec: A fast and lightweight decoder for x86 and x86-64 and encoder for x86-64.](https://github.com/aengelke/fadec)
  - Embedded

- CE
  - [AutoAssembler cannot encode vmovdqu correctly - Issue #3183](https://github.com/cheat-engine/cheat-engine/issues/3183)
  - > ce的反汇编好像有bug，会识别出超过15字节的指令，但实际上cpu只会执行15字节，导致后面全乱了，不知道ida会怎么样
- Binary Ninja
  - [→Intel XED](Assemblers.md#intel-xed)
  - [yrp604/bad64: Binja Arm64 Disassembler](https://github.com/yrp604/bad64)
- IDA
- OD
- VMProtect

## Testing
- [Mishegos: A differential fuzzer for x86 decoders](https://github.com/trailofbits/mishegos/)[^woodruffDifferentialAnalysisX86642021]

  [Destroying x86_64 instruction decoders with differential fuzzing -The Trail of Bits Blog](https://blog.trailofbits.com/2019/10/31/destroying-x86_64-instruction-decoders-with-differential-fuzzing/)
- [hint-break: Code proving a 25-year blind spot in all disassemblers. PoC for Intel x64/x86 "ghost instructions."](https://github.com/sapdragon/hint-break)
  - IDA, ~~[Binary Ninja](https://github.com/sapdragon/hint-break/issues/1)~~, ~~Ghidra~~

## Benchmarks
Can achieve 1~50M instructions per second.

[athre0z/disas-bench: X86 disassembler benchmark](https://github.com/athre0z/disas-bench)
- [icedland/disas-bench](https://github.com/icedland/disas-bench)
- iced > yaxpeax >> diStorm > udis86 > Zydis (min) > XED > bddisasm > Zydis (full) >> Capstone >> sleigh
- iced 比 Zydis (full) 快了六倍

## Length disassemblers
Length disassembler, length disassembler engine (LDE)

解析指令长度

- [gh-nomad/length-disassembler: A length disassembler for x86-32 and x86-64 written in C.](https://github.com/gh-nomad/length-disassembler) (discontinued)
  - [gh-nomad/nmd: set of single-header libraries for C/C++. The code is far from finished but some parts are quite usable.](https://github.com/gh-nomad/nmd)
- [CasualX/lde: Length disassembler for x86 and x86\_64 in Rust.](https://github.com/CasualX/lde)
- [lend: Tiny x86 Length Disassembler](https://github.com/greenbender/lend)
- [GiveMeZeny/fde64: Extended Length Disassembler Engine for x86-64 (1337 bytes in size)](https://github.com/GiveMeZeny/fde64) (discontinued)
- [Blackbone/LDasm.c at master - DarthTon/Blackbone - GitHub](https://github.com/DarthTon/Blackbone/blob/master/src/BlackBone/Asm/LDasm.c)

## Rust
- iced
- [yaxpeax-arch: fundamental traits to describe an architecture in the yaxpeax project](https://github.com/iximeow/yaxpeax-arch)
  - [yaxpeax-x86: x86 decoders for the yaxpeax project](https://github.com/iximeow/yaxpeax-x86)
  - [yaxpeax-dis: yaxdis, a small and naive disassembler using yaxpeax decoders](https://github.com/iximeow/yaxpeax-dis)
- [→Capstone](#capstone)
- [BiTE: Disassembler focused on comprehensive rust support.](https://github.com/WINSDK/bite)
- [endoli/burst.rs: A disassembler framework](https://github.com/endoli/burst.rs)
- [SMDA: a minimalist recursive disassembler library](https://github.com/marirs/smda-rs)
- [eqv/recursive\_disassembler: A very simple recursive disassembler based on capstone](https://github.com/eqv/recursive_disassembler)
- [kromych/disarm64: Instruction decoder generator](https://github.com/kromych/disarm64)
  - ARM
- [numas13/decodetree](https://github.com/numas13/decodetree)

ARM:
- [AetiasHax/unarm: Disassembler library for ARM](https://github.com/AetiasHax/unarm)

## .NET
- [AsmArm64: The most powerful ARM 64 (v8, v9) Assembler / Disassembler for .NET](https://github.com/xoofx/AsmArm64)

## [Zydis](https://github.com/zyantific/zydis)
> Fast and lightweight x86/x86-64 disassembler and code generation library

- Rust: [zyantific/zydis-rs](https://github.com/zyantific/zydis-rs/)
- [zyemu: x86-64 user mode emulation using Zydis](https://github.com/ZehMatt/zyemu)
- IDA: [zydisinfo](https://github.com/milankovo/zydisinfo)

  [Just put together the Zydisinfo plugin for IDA Pro! It gives you all the juicy details about the instruction at the current cursor position using the Zydis disassembler. #reversing #disassembly #IDAPro / X](https://x.com/Milankovo001/status/1889766957580161207)
- Used by x64dbg, Firefox, WebKit

## Capstone
[GitHub](https://github.com/capstone-engine/capstone)

> Capstone disassembly/disassembler framework for ARM, ARM64 (ARMv8), Alpha, BPF, Ethereum VM, HPPA, LoongArch, M68K, M680X, Mips, MOS65XX, PPC, RISC-V(rv32G/rv64G), SH, Sparc, SystemZ, TMS320C64X, TriCore, Webassembly, XCore and X86.

```python
from capstone import *
CODE = b"\x55\x48\x8b\x05\xb8\x13\x00\x00"
md = Cs(CS_ARCH_X86, CS_MODE_64)
for i in md.disasm(CODE, 0x1000):
    print("0x%x:\t%s\t%s" %(i.address, i.mnemonic, i.op_str)
```
```asm
0x1000: push    rbp
0x1001: mov rax, qword ptr [rip + 0x13b8]
```

- Rust: [capstone-rust/capstone-rs: High-level Capstone system bindings for Rust](https://github.com/capstone-rust/capstone-rs)
- .NET
  - [9ee1/Capstone.NET: .NET Core and .NET Framework binding for the Capstone Disassembly Framework](https://github.com/9ee1/Capstone.NET)
- [alexander-hanel/capstool](https://github.com/alexander-hanel/capstool)

[Capstone Disassembler Framework | Hacker News](https://news.ycombinator.com/item?id=41648711)
> Capstone supports an impressive breadth of architectures. However, if all you need is x86/AMD64 decoding and disassembly, there are much higher quality (in terms of accurate decoding) libraries out there.  
> I wrote a differential fuzzer for x86 decoders a few years ago, and XED and Zydis generally performed far better (in terms of accuracy) than Capstone[1]. And on the Rust side, yaxpeax and iced-x86 perform very admirably.


[^woodruffDifferentialAnalysisX86642021]: Woodruff, W., Carroll, N., & Peters, S. (2021). Differential analysis of x86-64 instruction decoders. 2021 IEEE Security and Privacy Workshops (SPW), 152–161. https://doi.org/10.1109/SPW53761.2021.00029
