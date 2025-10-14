# Advanced Performance Extensions (APX)
[x86 - Wikipedia](https://en.wikipedia.org/wiki/X86#APX)

> These extensions have been called "generational" and "the biggest x86 addition since 64 bits".

> According to the architecture specification, the main features of APX are:
- 16 additional general-purpose registers R16-R31, called the Extended GPRs (EGPRs)
- Three-operand instruction formats for many integer instructions
- New conditional instructions for loads, stores, and comparisons with common instructions that do not modify flags
- Optimized register save/restore operations
- A 64-bit absolute direct jump instruction

> Extended GPRs for general purpose instructions are encoded using 2-byte REX2 prefix, while new instructions and extended operands for existing AVX/AVX2/AVX-512 instructions are encoded with extended EVEX prefix which has four variants used for different groups of instructions.

> They do not change the size and layout of the XSAVE area as they take up the space left behind by the deprecated Intel® MPX registers.
> Apparently MPX was Memory Protection Extensions and the design was so flawed, it was removed entirely soon after introduction.

[Introducing Intel® Advanced Performance Extensions (Intel® APX)](https://www.intel.com/content/www/us/en/developer/articles/technical/advanced-performance-extensions-apx.html) ([Hacker News](https://news.ycombinator.com/item?id=36853166))
