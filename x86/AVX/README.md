# Advanced Vector Extensions (AVX)
[Wikipedia](https://en.wikipedia.org/wiki/Advanced_Vector_Extensions)

## AVX

## AVX2

[Vector Veil - CyberSci Regionals 2024 :: 1t1n1's blog](https://1t1n1.github.io/writeups/vector_veil/)
> 这回我出的题是 800 行手写的 AVX2，来自全国的 80 队里三队解出来了 (UW, UofT, PolyCyber)  
> UofT 的人赛后还在分析这个 AVX2 是怎么生成的，不同地方在 C 里怎么实现，听到我纯手写汇编之后笑疯了🤣

## AVX-512
[Wikipedia](https://en.wikipedia.org/wiki/AVX-512)

> AVX-512 expands AVX to 512-bit support using a new EVEX prefix encoding proposed by Intel in July 2013 and first supported by Intel with the Knights Landing co-processor, which shipped in 2016. In conventional processors, AVX-512 was introduced with Skylake server and HEDT processors in 2017.

- EVEX prefix ([Wikipedia](https://en.wikipedia.org/wiki/EVEX_prefix))

[Converting ASCII strings to lower case at crazy speeds with AVX-512 -- Daniel Lemire's blog](https://lemire.me/blog/2024/08/03/converting-ascii-strings-to-lower-case-at-crazy-speeds-with-avx-512/)

[AVX Bitwise ternary logic instruction busted!](https://arnaud-carre.github.io/2024-10-06-vpternlogd/) ([Hacker News](https://news.ycombinator.com/item?id=41759112))

[New FFmpeg AVX-512 Optimizations Hit Up To 36x The Performance Of Plain C Code - Phoronix](https://www.phoronix.com/news/FFmpeg-July-2025-AVX-512)
- [史上最显著提升：手写汇编代码，FFmpeg 实现部分功能速度提升 100 倍 - IT之家](https://www.ithome.com/0/868/959.htm)

  > 只是单个 filter 的特定 routine 的 AVX512 实现对比没开编译器优化的C实现有100倍  
  > 实际对比 clang -O3 -march=x86-64-v3 或老 SSE2 实现都只快了几倍而已  
  > 反映到整个pipe，可能两倍都没有

## AVX10
[Intel AVX10: Taking AVX-512 With More Features & Supporting It Across P/E Cores - Phoronix](https://www.phoronix.com/news/Intel-AVX10) ([Hacker News](https://news.ycombinator.com/item?id=36854030))

## Libraries
- [numpy/x86-simd-sort: C++ template library for high performance SIMD based sorting algorithms](https://github.com/numpy/x86-simd-sort)
  - [ENH: Vectorize quicksort for 16-bit and 64-bit dtype using AVX512 by r-devulap - Pull Request #22315 - numpy/numpy](https://github.com/numpy/numpy/pull/22315/)

  [Intel Publishes Blazing Fast AVX-512 Sorting Library, Numpy Switching To It For 10~17x Faster Sorts - Phoronix](https://www.phoronix.com/news/Intel-AVX-512-Quicksort-Numpy) ([r/Python](https://www.reddit.com/r/Python/comments/113cb77/intel_publishes_blazing_fast_avx512_sorting/))

## CPUs
[AMD Zen 5 架构将支持多种全新指令集，进一步强化 AI 性能 - IT之家](https://www.ithome.com/0/750/041.htm)
> 新版 GNU 编译器集合（GCC）已经为即将到来的 AMD Zen 5 架构提供了初步支持，并确认 Zen 5 处理器至少引入 5 个全新的指令集，包括 AVXVNNI、MOVDIRI、MOVDIR64B、AVX512VP2INTERSECT、PREFETCHI。这 5 个全新的指令集中有 4 个早已在 Intel CPU 上引入，还有一个指令后续也将很快出现在 Intel Granite Rapids 服务器 CPU 上。AMD 此前在指令集支持方面并不像 Intel 那样重视，尤其是 AVX 相关指令。

[Please do not require AVX support for your software](https://pavel.network/please-do-not-require-avx-for-your-software/)
> <- 尝试在没有 AVX 的机器上自部署 MongoDB 然后理所当然地失败了的人（tmd为什么
> 
> 有人做了个这个：https://github.com/GermanAizek/mongodb-without-avx
