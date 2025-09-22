# Processor Virtualization
## x86
[Wikipedia](https://en.wikipedia.org/wiki/X86_virtualization)

> In the late 1990s x86 virtualization was achieved by complex software techniques, necessary to compensate for the processor's lack of hardware-assisted virtualization capabilities while attaining reasonable performance. In 2005 and 2006, both Intel (VT-x) and AMD (AMD-V) introduced limited hardware virtualization support that allowed simpler virtualization software but offered very few speed benefits.[^adamsComparisonSoftwareHardware2006] Greater hardware support, which allowed substantial speed improvements, came with later processor models.

- Intel VT-x
- AMD-V

> We find that the hardware support fails to provide an unambiguous performance advantage for two primary reasons: first, it offers no support for MMU virtualization; second, it fails to co-exist with existing software techniques for MMU virtualization. We look ahead to emerging techniques for addressing this MMU virtualization problem in the context of hardware-assisted virtualization.[^adamsComparisonSoftwareHardware2006]

## ARM
[Introduction to the ARMv8 Virtualization System | openEuler](https://www.openeuler.org/en/blog/yorifang/2020-10-24-arm-virtualization-overview.html)

## [→MMU virtualization](https://github.com/Chaoses-Ib/InformationSystems/blob/main/Memory/Virtual/MMU/IO/README.md#virtualization)


[^adamsComparisonSoftwareHardware2006]: Adams, K., & Agesen, O. (2006). A comparison of software and hardware techniques for x86 virtualization. SIGOPS Oper. Syst. Rev., 40(5), 2–13. https://doi.org/10.1145/1168917.1168860
