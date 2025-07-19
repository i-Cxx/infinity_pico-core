external/FreeRTOS/
├── CMakeLists.txt
├── croutine.c
├── cspell.config.yaml
├── event_groups.c
├── examples
│   ├── cmake_example
│   │   ├── CMakeLists.txt
│   │   └── main.c
│   ├── coverity
│   │   ├── CMakeLists.txt
│   │   ├── coverity_misra.config
│   │   ├── FreeRTOSConfig.h
│   │   └── README.md
│   ├── README.md
│   └── template_configuration
│       ├── FreeRTOSConfig.h
│       └── readme.md
├── GitHub-FreeRTOS-Kernel-Home.url
├── History.txt
├── include
│   ├── atomic.h
│   ├── CMakeLists.txt
│   ├── croutine.h
│   ├── deprecated_definitions.h
│   ├── event_groups.h
│   ├── FreeRTOS.h
│   ├── list.h
│   ├── message_buffer.h
│   ├── mpu_prototypes.h
│   ├── mpu_syscall_numbers.h
│   ├── mpu_wrappers.h
│   ├── newlib-freertos.h
│   ├── picolibc-freertos.h
│   ├── portable.h
│   ├── projdefs.h
│   ├── queue.h
│   ├── semphr.h
│   ├── stack_macros.h
│   ├── StackMacros.h
│   ├── stdint.readme
│   ├── stream_buffer.h
│   ├── task.h
│   └── timers.h
├── LICENSE.md
├── list.c
├── manifest.yml
├── MISRA.md
├── portable
│   ├── ARMClang
│   │   └── Use-the-GCC-ports.txt
│   ├── ARMv8M
│   │   ├── copy_files.py
│   │   ├── non_secure
│   │   │   ├── portable
│   │   │   │   ├── GCC
│   │   │   │   │   ├── ARM_CM23
│   │   │   │   │   │   ├── mpu_wrappers_v2_asm.c
│   │   │   │   │   │   ├── portasm.c
│   │   │   │   │   │   └── portmacro.h
│   │   │   │   │   ├── ARM_CM23_NTZ
│   │   │   │   │   │   ├── mpu_wrappers_v2_asm.c
│   │   │   │   │   │   ├── portasm.c
│   │   │   │   │   │   └── portmacro.h
│   │   │   │   │   ├── ARM_CM33
│   │   │   │   │   │   ├── mpu_wrappers_v2_asm.c
│   │   │   │   │   │   ├── portasm.c
│   │   │   │   │   │   └── portmacro.h
│   │   │   │   │   ├── ARM_CM33_NTZ
│   │   │   │   │   │   ├── mpu_wrappers_v2_asm.c
│   │   │   │   │   │   ├── portasm.c
│   │   │   │   │   │   └── portmacro.h
│   │   │   │   │   ├── ARM_CM35P
│   │   │   │   │   │   └── portmacro.h
│   │   │   │   │   ├── ARM_CM55
│   │   │   │   │   │   └── portmacro.h
│   │   │   │   │   └── ARM_CM85
│   │   │   │   │       └── portmacro.h
│   │   │   │   └── IAR
│   │   │   │       ├── ARM_CM23
│   │   │   │       │   ├── mpu_wrappers_v2_asm.S
│   │   │   │       │   ├── portasm.s
│   │   │   │       │   └── portmacro.h
│   │   │   │       ├── ARM_CM23_NTZ
│   │   │   │       │   ├── mpu_wrappers_v2_asm.S
│   │   │   │       │   ├── portasm.s
│   │   │   │       │   └── portmacro.h
│   │   │   │       ├── ARM_CM33
│   │   │   │       │   ├── mpu_wrappers_v2_asm.S
│   │   │   │       │   ├── portasm.s
│   │   │   │       │   └── portmacro.h
│   │   │   │       ├── ARM_CM33_NTZ
│   │   │   │       │   ├── mpu_wrappers_v2_asm.S
│   │   │   │       │   ├── portasm.s
│   │   │   │       │   └── portmacro.h
│   │   │   │       ├── ARM_CM35P
│   │   │   │       │   └── portmacro.h
│   │   │   │       ├── ARM_CM55
│   │   │   │       │   └── portmacro.h
│   │   │   │       └── ARM_CM85
│   │   │   │           └── portmacro.h
│   │   │   ├── portasm.h
│   │   │   ├── port.c
│   │   │   ├── portmacrocommon.h
│   │   │   └── ReadMe.txt
│   │   ├── ReadMe.txt
│   │   └── secure
│   │       ├── context
│   │       │   ├── portable
│   │       │   │   ├── GCC
│   │       │   │   │   ├── ARM_CM23
│   │       │   │   │   │   └── secure_context_port.c
│   │       │   │   │   └── ARM_CM33
│   │       │   │   │       └── secure_context_port.c
│   │       │   │   └── IAR
│   │       │   │       ├── ARM_CM23
│   │       │   │       │   └── secure_context_port_asm.s
│   │       │   │       └── ARM_CM33
│   │       │   │           └── secure_context_port_asm.s
│   │       │   ├── secure_context.c
│   │       │   └── secure_context.h
│   │       ├── heap
│   │       │   ├── secure_heap.c
│   │       │   └── secure_heap.h
│   │       ├── init
│   │       │   ├── secure_init.c
│   │       │   └── secure_init.h
│   │       ├── macros
│   │       │   └── secure_port_macros.h
│   │       └── ReadMe.txt
│   ├── CMakeLists.txt
│   ├── Common
│   │   ├── mpu_wrappers.c
│   │   └── mpu_wrappers_v2.c
│   ├── GCC
│   │   ├── ARM7_AT91FR40008
│   │   │   ├── port.c
│   │   │   ├── portISR.c
│   │   │   └── portmacro.h
│   │   ├── ARM7_AT91SAM7S
│   │   │   ├── AT91SAM7X256.h
│   │   │   ├── ioat91sam7x256.h
│   │   │   ├── lib_AT91SAM7X256.c
│   │   │   ├── lib_AT91SAM7X256.h
│   │   │   ├── port.c
│   │   │   ├── portISR.c
│   │   │   └── portmacro.h
│   │   ├── ARM7_LPC2000
│   │   │   ├── port.c
│   │   │   ├── portISR.c
│   │   │   └── portmacro.h
│   │   ├── ARM7_LPC23xx
│   │   │   ├── port.c
│   │   │   ├── portISR.c
│   │   │   └── portmacro.h
│   │   ├── ARM_AARCH64
│   │   │   ├── portASM.S
│   │   │   ├── port.c
│   │   │   ├── portmacro.h
│   │   │   └── README.md
│   │   ├── ARM_AARCH64_SRE
│   │   │   ├── portASM.S
│   │   │   ├── port.c
│   │   │   ├── portmacro.h
│   │   │   └── README.md
│   │   ├── ARM_CA53_64_BIT
│   │   │   └── README.md
│   │   ├── ARM_CA53_64_BIT_SRE
│   │   │   └── README.md
│   │   ├── ARM_CA9
│   │   │   ├── portASM.S
│   │   │   ├── port.c
│   │   │   └── portmacro.h
│   │   ├── ARM_CM0
│   │   │   ├── mpu_wrappers_v2_asm.c
│   │   │   ├── portasm.c
│   │   │   ├── portasm.h
│   │   │   ├── port.c
│   │   │   └── portmacro.h
│   │   ├── ARM_CM23
│   │   │   ├── non_secure
│   │   │   │   ├── mpu_wrappers_v2_asm.c
│   │   │   │   ├── portasm.c
│   │   │   │   ├── portasm.h
│   │   │   │   ├── port.c
│   │   │   │   ├── portmacrocommon.h
│   │   │   │   └── portmacro.h
│   │   │   └── secure
│   │   │       ├── secure_context.c
│   │   │       ├── secure_context.h
│   │   │       ├── secure_context_port.c
│   │   │       ├── secure_heap.c
│   │   │       ├── secure_heap.h
│   │   │       ├── secure_init.c
│   │   │       ├── secure_init.h
│   │   │       └── secure_port_macros.h
│   │   ├── ARM_CM23_NTZ
│   │   │   └── non_secure
│   │   │       ├── mpu_wrappers_v2_asm.c
│   │   │       ├── portasm.c
│   │   │       ├── portasm.h
│   │   │       ├── port.c
│   │   │       ├── portmacrocommon.h
│   │   │       └── portmacro.h
│   │   ├── ARM_CM3
│   │   │   ├── port.c
│   │   │   └── portmacro.h
│   │   ├── ARM_CM33
│   │   │   ├── non_secure
│   │   │   │   ├── mpu_wrappers_v2_asm.c
│   │   │   │   ├── portasm.c
│   │   │   │   ├── portasm.h
│   │   │   │   ├── port.c
│   │   │   │   ├── portmacrocommon.h
│   │   │   │   └── portmacro.h
│   │   │   └── secure
│   │   │       ├── secure_context.c
│   │   │       ├── secure_context.h
│   │   │       ├── secure_context_port.c
│   │   │       ├── secure_heap.c
│   │   │       ├── secure_heap.h
│   │   │       ├── secure_init.c
│   │   │       ├── secure_init.h
│   │   │       └── secure_port_macros.h
│   │   ├── ARM_CM33_NTZ
│   │   │   └── non_secure
│   │   │       ├── mpu_wrappers_v2_asm.c
│   │   │       ├── portasm.c
│   │   │       ├── portasm.h
│   │   │       ├── port.c
│   │   │       ├── portmacrocommon.h
│   │   │       └── portmacro.h
│   │   ├── ARM_CM35P
│   │   │   ├── non_secure
│   │   │   │   ├── mpu_wrappers_v2_asm.c
│   │   │   │   ├── portasm.c
│   │   │   │   ├── portasm.h
│   │   │   │   ├── port.c
│   │   │   │   ├── portmacrocommon.h
│   │   │   │   └── portmacro.h
│   │   │   └── secure
│   │   │       ├── secure_context.c
│   │   │       ├── secure_context.h
│   │   │       ├── secure_context_port.c
│   │   │       ├── secure_heap.c
│   │   │       ├── secure_heap.h
│   │   │       ├── secure_init.c
│   │   │       ├── secure_init.h
│   │   │       └── secure_port_macros.h
│   │   ├── ARM_CM35P_NTZ
│   │   │   └── non_secure
│   │   │       ├── mpu_wrappers_v2_asm.c
│   │   │       ├── portasm.c
│   │   │       ├── portasm.h
│   │   │       ├── port.c
│   │   │       ├── portmacrocommon.h
│   │   │       └── portmacro.h
│   │   ├── ARM_CM3_MPU
│   │   │   ├── mpu_wrappers_v2_asm.c
│   │   │   ├── port.c
│   │   │   └── portmacro.h
│   │   ├── ARM_CM4F
│   │   │   ├── port.c
│   │   │   └── portmacro.h
│   │   ├── ARM_CM4_MPU
│   │   │   ├── mpu_wrappers_v2_asm.c
│   │   │   ├── port.c
│   │   │   └── portmacro.h
│   │   ├── ARM_CM55
│   │   │   ├── non_secure
│   │   │   │   ├── mpu_wrappers_v2_asm.c
│   │   │   │   ├── portasm.c
│   │   │   │   ├── portasm.h
│   │   │   │   ├── port.c
│   │   │   │   ├── portmacrocommon.h
│   │   │   │   └── portmacro.h
│   │   │   └── secure
│   │   │       ├── secure_context.c
│   │   │       ├── secure_context.h
│   │   │       ├── secure_context_port.c
│   │   │       ├── secure_heap.c
│   │   │       ├── secure_heap.h
│   │   │       ├── secure_init.c
│   │   │       ├── secure_init.h
│   │   │       └── secure_port_macros.h
│   │   ├── ARM_CM55_NTZ
│   │   │   └── non_secure
│   │   │       ├── mpu_wrappers_v2_asm.c
│   │   │       ├── portasm.c
│   │   │       ├── portasm.h
│   │   │       ├── port.c
│   │   │       ├── portmacrocommon.h
│   │   │       └── portmacro.h
│   │   ├── ARM_CM7
│   │   │   ├── r0p1
│   │   │   │   ├── port.c
│   │   │   │   └── portmacro.h
│   │   │   └── ReadMe.txt
│   │   ├── ARM_CM85
│   │   │   ├── non_secure
│   │   │   │   ├── mpu_wrappers_v2_asm.c
│   │   │   │   ├── portasm.c
│   │   │   │   ├── portasm.h
│   │   │   │   ├── port.c
│   │   │   │   ├── portmacrocommon.h
│   │   │   │   └── portmacro.h
│   │   │   └── secure
│   │   │       ├── secure_context.c
│   │   │       ├── secure_context.h
│   │   │       ├── secure_context_port.c
│   │   │       ├── secure_heap.c
│   │   │       ├── secure_heap.h
│   │   │       ├── secure_init.c
│   │   │       ├── secure_init.h
│   │   │       └── secure_port_macros.h
│   │   ├── ARM_CM85_NTZ
│   │   │   └── non_secure
│   │   │       ├── mpu_wrappers_v2_asm.c
│   │   │       ├── portasm.c
│   │   │       ├── portasm.h
│   │   │       ├── port.c
│   │   │       ├── portmacrocommon.h
│   │   │       └── portmacro.h
│   │   ├── ARM_CR5
│   │   │   ├── portASM.S
│   │   │   ├── port.c
│   │   │   └── portmacro.h
│   │   ├── ARM_CRx_MPU
│   │   │   ├── mpu_wrappers_v2_asm.S
│   │   │   ├── portASM.S
│   │   │   ├── port.c
│   │   │   ├── portmacro_asm.h
│   │   │   └── portmacro.h
│   │   ├── ARM_CRx_No_GIC
│   │   │   ├── portASM.S
│   │   │   ├── port.c
│   │   │   └── portmacro.h
│   │   ├── ATMega323
│   │   │   ├── port.c
│   │   │   └── portmacro.h
│   │   ├── AVR32_UC3
│   │   │   ├── exception.S
│   │   │   ├── port.c
│   │   │   └── portmacro.h
│   │   ├── AVR_AVRDx
│   │   │   └── README.md
│   │   ├── AVR_Mega0
│   │   │   └── README.md
│   │   ├── ColdFire_V2
│   │   │   ├── portasm.S
│   │   │   ├── port.c
│   │   │   └── portmacro.h
│   │   ├── CORTUS_APS3
│   │   │   ├── port.c
│   │   │   └── portmacro.h
│   │   ├── H8S2329
│   │   │   ├── port.c
│   │   │   └── portmacro.h
│   │   ├── HCS12
│   │   │   ├── port.c
│   │   │   └── portmacro.h
│   │   ├── IA32_flat
│   │   │   ├── ISR_Support.h
│   │   │   ├── portASM.S
│   │   │   ├── port.c
│   │   │   └── portmacro.h
│   │   ├── MCF5235
│   │   │   └── readme.md
│   │   ├── MicroBlaze
│   │   │   ├── portasm.s
│   │   │   ├── port.c
│   │   │   └── portmacro.h
│   │   ├── MicroBlazeV8
│   │   │   ├── portasm.S
│   │   │   ├── port.c
│   │   │   ├── port_exceptions.c
│   │   │   └── portmacro.h
│   │   ├── MicroBlazeV9
│   │   │   ├── portasm.S
│   │   │   ├── port.c
│   │   │   ├── port_exceptions.c
│   │   │   └── portmacro.h
│   │   ├── MSP430F449
│   │   │   ├── port.c
│   │   │   └── portmacro.h
│   │   ├── NiosII
│   │   │   ├── port_asm.S
│   │   │   ├── port.c
│   │   │   └── portmacro.h
│   │   ├── PPC405_Xilinx
│   │   │   ├── FPU_Macros.h
│   │   │   ├── portasm.S
│   │   │   ├── port.c
│   │   │   └── portmacro.h
│   │   ├── PPC440_Xilinx
│   │   │   ├── FPU_Macros.h
│   │   │   ├── portasm.S
│   │   │   ├── port.c
│   │   │   └── portmacro.h
│   │   ├── RISC-V
│   │   │   ├── chip_extensions.cmake
│   │   │   ├── chip_specific_extensions
│   │   │   │   ├── Pulpino_Vega_RV32M1RM
│   │   │   │   │   └── freertos_risc_v_chip_specific_extensions.h
│   │   │   │   ├── readme.txt
│   │   │   │   ├── RISCV_MTIME_CLINT_no_extensions
│   │   │   │   │   └── freertos_risc_v_chip_specific_extensions.h
│   │   │   │   ├── RISCV_no_extensions
│   │   │   │   │   └── freertos_risc_v_chip_specific_extensions.h
│   │   │   │   └── RV32I_CLINT_no_extensions
│   │   │   │       └── freertos_risc_v_chip_specific_extensions.h
│   │   │   ├── Documentation.url
│   │   │   ├── portASM.S
│   │   │   ├── port.c
│   │   │   ├── portContext.h
│   │   │   ├── portmacro.h
│   │   │   └── readme.txt
│   │   ├── RL78
│   │   │   ├── isr_support.h
│   │   │   ├── portasm.S
│   │   │   ├── port.c
│   │   │   └── portmacro.h
│   │   ├── RX100
│   │   │   ├── port.c
│   │   │   ├── portmacro.h
│   │   │   └── readme.txt
│   │   ├── RX200
│   │   │   ├── port.c
│   │   │   └── portmacro.h
│   │   ├── RX600
│   │   │   ├── port.c
│   │   │   ├── portmacro.h
│   │   │   └── readme.txt
│   │   ├── RX600v2
│   │   │   ├── port.c
│   │   │   ├── portmacro.h
│   │   │   └── readme.txt
│   │   ├── RX700v3_DPFPU
│   │   │   ├── port.c
│   │   │   ├── portmacro.h
│   │   │   └── readme.txt
│   │   ├── STR75x
│   │   │   ├── port.c
│   │   │   ├── portISR.c
│   │   │   └── portmacro.h
│   │   └── TriCore_1782
│   │       ├── port.c
│   │       ├── portmacro.h
│   │       └── porttrap.c
│   ├── MemMang
│   │   ├── heap_1.c
│   │   ├── heap_2.c
│   │   ├── heap_3.c
│   │   ├── heap_4.c
│   │   ├── heap_5.c
│   │   └── ReadMe.url
│   ├── MikroC
│   │   └── ARM_CM4F
│   │       ├── port.c
│   │       └── portmacro.h
│   ├── readme.txt
│   ├── Tasking
│   │   └── ARM_CM4F
│   │       ├── port_asm.asm
│   │       ├── port.c
│   │       └── portmacro.h
│   ├── template
│   │   ├── port.c
│   │   └── portmacro.h
│   ├── ThirdParty
│   │   ├── CDK
│   │   │   └── T-HEAD_CK802
│   │   │       ├── portasm.S
│   │   │       ├── port.c
│   │   │       └── portmacro.h
│   │   ├── Community-Supported-Ports
│   │   │   ├── CCRH
│   │   │   │   └── RH850_F1KM_S4
│   │   │   │       ├── portasm.s
│   │   │   │       ├── port.c
│   │   │   │       ├── portmacro.h
│   │   │   │       └── README.md
│   │   │   ├── CCS
│   │   │   │   └── C2000_C28x
│   │   │   │       ├── portasm.asm
│   │   │   │       ├── port.c
│   │   │   │       ├── portmacro.h
│   │   │   │       └── README.md
│   │   │   ├── GCC
│   │   │   │   ├── CORTEX_A53_64-bit_UltraScale_MPSoC
│   │   │   │   │   ├── bsp_patches
│   │   │   │   │   │   ├── boot.S
│   │   │   │   │   │   ├── cpu.c
│   │   │   │   │   │   ├── cpu.h
│   │   │   │   │   │   ├── ReadMe.txt
│   │   │   │   │   │   ├── scugic_v4_2_diff.png
│   │   │   │   │   │   ├── standalone_v7_2_diff.png
│   │   │   │   │   │   ├── xil-crt0.S
│   │   │   │   │   │   └── xscugic.c
│   │   │   │   │   ├── portASM.S
│   │   │   │   │   ├── port_asm_vectors.S
│   │   │   │   │   ├── port.c
│   │   │   │   │   ├── portmacro.h
│   │   │   │   │   ├── portZynqUltrascale.c
│   │   │   │   │   └── ReadMe.txt
│   │   │   │   ├── MSP430FR5969
│   │   │   │   │   ├── port.c
│   │   │   │   │   └── portmacro.h
│   │   │   │   ├── RISC-V
│   │   │   │   │   └── chip_specific_extensions
│   │   │   │   │       └── THEAD_RV32
│   │   │   │   │           └── freertos_risc_v_chip_specific_extensions.h
│   │   │   │   ├── RP2350_ARM_NTZ
│   │   │   │   │   ├── CMakeLists.txt
│   │   │   │   │   ├── FreeRTOS_Kernel_import.cmake
│   │   │   │   │   ├── library.cmake
│   │   │   │   │   ├── LICENSE.md
│   │   │   │   │   ├── non_secure
│   │   │   │   │   │   ├── freertos_sdk_config.h
│   │   │   │   │   │   ├── mpu_wrappers_v2_asm.c
│   │   │   │   │   │   ├── portasm.c
│   │   │   │   │   │   ├── portasm.h
│   │   │   │   │   │   ├── port.c
│   │   │   │   │   │   ├── portmacrocommon.h
│   │   │   │   │   │   ├── portmacro.h
│   │   │   │   │   │   └── rp2040_config.h
│   │   │   │   │   ├── pico_sdk_import.cmake
│   │   │   │   │   └── README.md
│   │   │   │   ├── RP2350_RISC-V
│   │   │   │   │   ├── CMakeLists.txt
│   │   │   │   │   ├── Documentation.url
│   │   │   │   │   ├── FreeRTOS_Kernel_import.cmake
│   │   │   │   │   ├── include
│   │   │   │   │   │   ├── freertos_risc_v_chip_specific_extensions.h
│   │   │   │   │   │   ├── freertos_sdk_config.h
│   │   │   │   │   │   ├── portContext.h
│   │   │   │   │   │   ├── portmacro.h
│   │   │   │   │   │   └── rp2040_config.h
│   │   │   │   │   ├── library.cmake
│   │   │   │   │   ├── LICENSE.md
│   │   │   │   │   ├── notes.txt
│   │   │   │   │   ├── pico_sdk_import.cmake
│   │   │   │   │   ├── portASM.S
│   │   │   │   │   ├── port.c
│   │   │   │   │   ├── README.md
│   │   │   │   │   └── readme.txt
│   │   │   │   └── TriCore_38xa
│   │   │   │       ├── port.c
│   │   │   │       ├── port.h
│   │   │   │       ├── portmacro.h
│   │   │   │       ├── porttrap.c
│   │   │   │       └── readme.txt
│   │   │   ├── LICENSE
│   │   │   ├── README.md
│   │   │   └── Z88DK
│   │   │       └── Z180
│   │   │           ├── port.c
│   │   │           ├── portmacro.h
│   │   │           └── readme.md
│   │   ├── GCC
│   │   │   ├── ARC_EM_HS
│   │   │   │   ├── arc_freertos_exceptions.c
│   │   │   │   ├── arc_freertos_exceptions.h
│   │   │   │   ├── arc_support.s
│   │   │   │   ├── freertos_tls.c
│   │   │   │   ├── port.c
│   │   │   │   └── portmacro.h
│   │   │   ├── ARC_v1
│   │   │   │   ├── arc_freertos_exceptions.c
│   │   │   │   ├── arc_freertos_exceptions.h
│   │   │   │   ├── arc_support.s
│   │   │   │   ├── port.c
│   │   │   │   └── portmacro.h
│   │   │   ├── ARM_TFM
│   │   │   │   ├── os_wrapper_freertos.c
│   │   │   │   └── README.md
│   │   │   ├── ATmega
│   │   │   │   ├── port.c
│   │   │   │   ├── portmacro.h
│   │   │   │   └── readme.md
│   │   │   ├── Posix
│   │   │   │   ├── FreeRTOS-simulator-for-Linux.url
│   │   │   │   ├── port.c
│   │   │   │   ├── portmacro.h
│   │   │   │   └── utils
│   │   │   │       ├── wait_for_event.c
│   │   │   │       └── wait_for_event.h
│   │   │   ├── RISC-V
│   │   │   │   └── README-for-info-on-official-MIT-license-port.txt
│   │   │   ├── RP2040
│   │   │   │   ├── CMakeLists.txt
│   │   │   │   ├── FreeRTOS_Kernel_import.cmake
│   │   │   │   ├── include
│   │   │   │   │   ├── freertos_sdk_config.h
│   │   │   │   │   ├── portmacro.h
│   │   │   │   │   └── rp2040_config.h
│   │   │   │   ├── library.cmake
│   │   │   │   ├── LICENSE.md
│   │   │   │   ├── pico_sdk_import.cmake
│   │   │   │   ├── port.c
│   │   │   │   └── README.md
│   │   │   └── Xtensa_ESP32
│   │   │       ├── FreeRTOS-openocd.c
│   │   │       ├── include
│   │   │       │   ├── FreeRTOSConfig_arch.h
│   │   │       │   ├── portbenchmark.h
│   │   │       │   ├── portmacro.h
│   │   │       │   ├── port_systick.h
│   │   │       │   ├── xt_asm_utils.h
│   │   │       │   ├── xtensa_api.h
│   │   │       │   ├── xtensa_config.h
│   │   │       │   ├── xtensa_context.h
│   │   │       │   ├── xtensa_rtos.h
│   │   │       │   └── xtensa_timer.h
│   │   │       ├── portasm.S
│   │   │       ├── port.c
│   │   │       ├── port_common.c
│   │   │       ├── portmux_impl.h
│   │   │       ├── portmux_impl.inc.h
│   │   │       ├── port_systick.c
│   │   │       ├── xtensa_context.S
│   │   │       ├── xtensa_init.c
│   │   │       ├── xtensa_loadstore_handler.S
│   │   │       ├── xtensa_overlay_os_hook.c
│   │   │       ├── xtensa_vector_defaults.S
│   │   │       └── xtensa_vectors.S
│   │   ├── KnownIssues.md
│   │   ├── Partner-Supported-Ports
│   │   │   ├── Cadence
│   │   │   │   └── Xtensa
│   │   │   │       ├── asm-offsets.c
│   │   │   │       ├── Makefile
│   │   │   │       ├── mpu.S
│   │   │   │       ├── portasm.S
│   │   │   │       ├── portbenchmark.h
│   │   │   │       ├── port.c
│   │   │   │       ├── portclib.c
│   │   │   │       ├── portmacro.h
│   │   │   │       ├── portmpu.c
│   │   │   │       ├── porttrace.h
│   │   │   │       ├── readme_xtensa.txt
│   │   │   │       ├── relnotes.txt
│   │   │   │       ├── xtensa_api.h
│   │   │   │       ├── xtensa_config.h
│   │   │   │       ├── xtensa_context.h
│   │   │   │       ├── xtensa_context.S
│   │   │   │       ├── xtensa_coproc_handler.S
│   │   │   │       ├── xtensa_intr_asm.S
│   │   │   │       ├── xtensa_intr.c
│   │   │   │       ├── xtensa_intr_wrapper.c
│   │   │   │       ├── xtensa_overlay_os_hook.c
│   │   │   │       ├── xtensa_rtos.h
│   │   │   │       ├── xtensa_timer.h
│   │   │   │       ├── xtensa_vectors.S
│   │   │   │       └── xtensa_vectors_xea3.S
│   │   │   ├── GCC
│   │   │   │   ├── AVR_AVRDx
│   │   │   │   │   ├── port.c
│   │   │   │   │   ├── porthardware.h
│   │   │   │   │   └── portmacro.h
│   │   │   │   └── AVR_Mega0
│   │   │   │       ├── port.c
│   │   │   │       ├── porthardware.h
│   │   │   │       └── portmacro.h
│   │   │   ├── LICENSE
│   │   │   ├── README.md
│   │   │   ├── Tasking
│   │   │   │   └── AURIX_TC3xx
│   │   │   │       ├── port.c
│   │   │   │       └── portmacro.h
│   │   │   └── TI
│   │   │       └── CORTEX_A53_64-BIT_TI_AM64_SMP
│   │   │           ├── portASM.S
│   │   │           ├── port.c
│   │   │           └── portmacro.h
│   │   ├── README.md
│   │   ├── XCC
│   │   │   └── Xtensa
│   │   │       └── readme_xtensa.txt
│   │   └── xClang
│   │       └── XCOREAI
│   │           ├── portasm.S
│   │           ├── port.c
│   │           ├── portmacro.h
│   │           ├── port.xc
│   │           └── rtos_support_rtos_config.h
│   └── WizC
│       └── PIC18
│           ├── addFreeRTOS.h
│           ├── Drivers
│           │   └── Tick
│           │       ├── isrTick.c
│           │       └── Tick.c
│           ├── Install.bat
│           ├── port.c
│           └── portmacro.h
├── queue.c
├── Quick_Start_Guide.url
├── README.md
├── stream_buffer.c
├── tasks.c
└── timers.c

174 directories, 528 files
