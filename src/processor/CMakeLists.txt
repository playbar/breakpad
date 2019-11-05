find_library(FOUNDATION_LIB Foundation)

add_executable(minidump_stackwalk
        basic_code_modules.cc
        basic_source_line_resolver.cc
        call_stack.cc
        cfi_frame_info.cc
        convert_old_arm64_context.cc
        disassembler_x86.cc
        dump_context.cc
        dump_object.cc
        exploitability.cc
        exploitability_linux.cc
        exploitability_win.cc
        minidump.cc
        minidump_processor.cc
        minidump_stackwalk.cc
        logging.cc
        pathname_stripper.cc
        process_state.cc
        proc_maps_linux.cc
        simple_symbol_supplier.cc
        source_line_resolver_base.cc
        stack_frame_symbolizer.cc
        stackwalk_common.cc
        stackwalker.cc
        stackwalker_amd64.cc
        stackwalker_arm.cc
        stackwalker_arm64.cc
        stackwalker_mips.cc
        stackwalker_sparc.cc
        stackwalker_ppc.cc
        stackwalker_ppc64.cc
        stackwalker_x86.cc
        symbolic_constants_win.cc
        tokenize.cc
        $<TARGET_OBJECTS:common>
        $<TARGET_OBJECTS:disasm>)

target_link_libraries(minidump_stackwalk ${FOUNDATION_LIB})

install(TARGETS minidump_stackwalk DESTINATION bin)
