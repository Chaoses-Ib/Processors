# Assembly Language
[Wikipedia](https://en.wikipedia.org/wiki/Assembly_language)

## Syntax
[^syntax-wiki]
- Intel syntax
- AT&T syntax

> intel语法更简洁，看起来顺眼，但是AT&T语法也有其优点，典型如宏参数[^att-csdn]

### Intel syntax
Configuration:
- GCC/Clang[^syntax-gcc-so-1][^syntax-gcc-so-2]
  - `.intel_syntax noprefix`
  - `-masm=intel -mnaked-reg`
- GDB: [set disassembly-flavor intel](https://visualgdb.com/gdbreference/commands/set_disassembly-flavor)  
  Permanent:
  ```sh
  echo "set disassembly-flavor intel" >> ~/.gdbinit
  ```
- objdump[^syntax-objdump]: `objdump -M intel`
  - llvm-objdump: `-x86-asm-syntax=intel`

### AT&T syntax
[AT&T汇编_移动开发_weixin_34245749的博客 - CSDN 博客](https://blog.csdn.net/weixin_34245749/article/details/93182186)

[^syntax-wiki]: [x86 assembly language - Wikipedia](https://en.wikipedia.org/wiki/X86_assembly_language#Syntax)
[^att-csdn]: [AT&T 和 Intel汇编学哪种比较好？？？-CSDN社区](https://bbs.csdn.net/topics/392505424)
[^syntax-gcc-so-1]: [c - Can I use Intel syntax of x86 assembly with GCC? - Stack Overflow](https://stackoverflow.com/questions/9347909/can-i-use-intel-syntax-of-x86-assembly-with-gcc)
[^syntax-gcc-so-2]: [assembly - How to set gcc or clang to use Intel syntax permanently for inline asm() statements? - Stack Overflow](https://stackoverflow.com/questions/38953951/how-to-set-gcc-or-clang-to-use-intel-syntax-permanently-for-inline-asm-stateme)
[^syntax-objdump]: [linux - How can objdump emit intel syntax - Stack Overflow](https://stackoverflow.com/questions/10362630/how-can-objdump-emit-intel-syntax)

## [→Assemblers](Assemblers.md)

## IDEs
- Visual Studio
  - [AsmDude2: Visual Studio extension for assembly syntax highlighting and code completion in assembly files and the disassembly window](https://github.com/HJLebbink/asm-dude)
- [ZathuraDbg: An emulation based tool for learning and debugging assembly.](https://github.com/ZathuraDbg/ZathuraDbg)

Web:
- [x86-64-playground: An online assembly editor, emulator and debugger for the x86-64 architecture](https://github.com/robalb/x86-64-playground)

  [x86-64 playground: an online assembly editor and GDB-like debugger : r/ReverseEngineering](https://www.reddit.com/r/ReverseEngineering/comments/1iwm389/x8664_playground_an_online_assembly_editor_and/)
