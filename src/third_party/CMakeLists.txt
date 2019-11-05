set(disasm_SRC
        libdisasm/ia32_settings.c
        libdisasm/ia32_reg.c
        libdisasm/ia32_invariant.c
        libdisasm/ia32_insn.c
        libdisasm/ia32_operand.c
        libdisasm/ia32_implicit.c
        libdisasm/ia32_modrm.c
        libdisasm/ia32_opcode_tables.c
        libdisasm/x86_misc.c
        libdisasm/x86_operand_list.c
        libdisasm/x86_insn.c
        libdisasm/x86_disasm.c
        libdisasm/x86_imm.c
        )


add_library(disasm OBJECT ${disasm_SRC})


file(GLOB H lss/*h)
install(FILES ${H} DESTINATION include/breakpad/third_party/lss)
