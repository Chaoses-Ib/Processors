# Disassemblers
Disassemblers, 反汇编引擎

- [→iced](Assemblers.md#iced)
- [→Intel XED](Assemblers.md#intel-xed)
- [→LLVM](Assemblers.md#llvm)

Disassembling-only:
- [Zydis: Fast and lightweight x86/x86-64 disassembler and code generation library](https://github.com/zyantific/zydis)
  - Rust: [zyantific/zydis-rs](https://github.com/zyantific/zydis-rs/)
  - Used by x64dbg, Firefox, WebKit
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
- Binary Ninja
  - [yrp604/bad64: Binja Arm64 Disassembler](https://github.com/yrp604/bad64)
- OD
- VMProtect

[trailofbits/mishegos: A differential fuzzer for x86 decoders](https://github.com/trailofbits/mishegos/)

## Benchmarks
Can achieve 1~50M instructions per second.

[athre0z/disas-bench: X86 disassembler benchmark](https://github.com/athre0z/disas-bench)
- [icedland/disas-bench](https://github.com/icedland/disas-bench)
- iced > yaxpeax >> diStorm > udis86 > Zydis (min) > XED > bddisasm > Zydis (full) >> Capstone >> sleigh
- iced 比 Zydis (full) 快了六倍

## Length disassemblers
解析指令长度

- [CasualX/lde: Length disassembler for x86 and x86\_64 in Rust.](https://github.com/CasualX/lde)
- [lend: Tiny x86 Length Disassembler](https://github.com/greenbender/lend)
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
- [alexander-hanel/capstool](https://github.com/alexander-hanel/capstool)

[Capstone Disassembler Framework | Hacker News](https://news.ycombinator.com/item?id=41648711)
> Capstone supports an impressive breadth of architectures. However, if all you need is x86/AMD64 decoding and disassembly, there are much higher quality (in terms of accurate decoding) libraries out there.  
> I wrote a differential fuzzer for x86 decoders a few years ago, and XED and Zydis generally performed far better (in terms of accuracy) than Capstone[1]. And on the Rust side, yaxpeax and iced-x86 perform very admirably.
