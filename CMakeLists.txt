cmake_minimum_required(VERSION 3.15)
project(code_in_paojie VERSION 0.1.1 LANGUAGES C
  DESCRIPTION "代码排版成炮姐（御坂美琴）的样子，能运行，能唱歌"
  HOMEPAGE_URL "https://github.com/3150601355/code_in_paojie.git"
  )
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
set(CMAKE_C_STANDARD_REQUIRED ON)
set(CMAKE_BUILD_TYPE MinSizeRel)
set(CMAKE_C_EXTENSIONS OFF)
set(BUILD_SHARED_LIBS OFF)
set(CMAKE_C_STANDARD 99)

add_executable(railgun railgun.c)
set_target_properties(railgun PROPERTIES
  VERSION ${PROJECT_VERSION}
  INTERPROCEDURAL_OPTIMIZATION ON
  MSVC_RUNTIME_LIBRARY "MultiThreaded$<$<CONFIG:Debug>:Debug>"
  )
target_compile_options(railgun PRIVATE
  $<$<C_COMPILER_ID:GNU>:-finput-charset=UTF-8 -fexec-charset=GBK>
  $<$<C_COMPILER_ID:MSVC>:/source-charset:UTF-8 /execution-charset:GBK>
  )
target_compile_definitions(railgun PRIVATE
  _CRT_SECURE_NO_WARNINGS _UNICODE UNICODE
  )
target_link_libraries(railgun PRIVATE vfw32)
