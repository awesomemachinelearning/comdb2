if (${CMAKE_C_COMPILER_ID} STREQUAL GNU)
  set_source_files_properties(cson_amalgamation_core.c PROPERTIES COMPILE_FLAGS "-Wno-unused-variable -Wno-unused-but-set-variable -Wno-unused-label")
elseif(${CMAKE_C_COMPILER_ID} STREQUAL Clang)
  set_source_files_properties(cson_amalgamation_core.c PROPERTIES COMPILE_FLAGS "-Wno-unused-variable -Wno-unused-const-variable -Wno-unused-label")
endif()
add_library(cson cson_amalgamation_core.c)
