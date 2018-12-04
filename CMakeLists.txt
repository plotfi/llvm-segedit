set(LLVM_LINK_COMPONENTS
  AllTargetsAsmPrinters
  AllTargetsDescs
  AllTargetsDisassemblers
  AllTargetsInfos
  BinaryFormat
  CodeGen
  DebugInfoDWARF
  DebugInfoPDB
  Demangle
  MC
  MCDisassembler
  Object
  Support
  Symbolize
  )

add_llvm_tool(llvm-segedit
  llvm-segedit.cpp
  )

if(HAVE_LIBXAR)
  target_link_libraries(llvm-segedit PRIVATE ${XAR_LIB})
endif()

