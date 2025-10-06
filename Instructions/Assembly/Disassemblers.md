# Disassemblers
Disassemblers, 反汇编引擎

- [iced: Blazing fast and correct x86/x64 disassembler, assembler, decoder, encoder for Rust, .NET, Java, Python, Lua](https://github.com/icedland/iced)
- [Zydis: Fast and lightweight x86/x86-64 disassembler and code generation library](https://github.com/zyantific/zydis)

- BeaEngine

  [BeaEngine/beaengine: BeaEngine disasm project](https://github.com/BeaEngine/beaengine)

- udis86

  [vmt/udis86: Disassembler Library for x86 and x86-64](https://github.com/vmt/udis86)

  停止更新

- OD
- CE
- Capstone

  [aquynh/capstone: Capstone disassembly/disassembler framework](https://github.com/aquynh/capstone)

## Length disassemblers
解析指令长度

- [lend: Tiny x86 Length Disassembler](https://github.com/greenbender/lend)
- [Blackbone/LDasm.c at master - DarthTon/Blackbone - GitHub](https://github.com/DarthTon/Blackbone/blob/master/src/BlackBone/Asm/LDasm.c)

## Capstone
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
