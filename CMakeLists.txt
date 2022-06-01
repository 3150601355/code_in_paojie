cmake_minimum_required(VERSION 3.12)
project(code_in_paojie VERSION 0.1.0 LANGUAGES C
  DESCRIPTION "代码排版成炮姐（御坂美琴）的样子，能运行，能唱歌"
  HOMEPAGE_URL "https://github.com/3150601355/code_in_paojie.git"
  )
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
set(CMAKE_BUILD_TYPE MinSizeRel)
set(BUILD_SHARED_LIBS OFF)

add_executable(railgun railgun.c)
set_target_properties(railgun PROPERTIES VERSION ${PROJECT_VERSION})
set_target_properties(railgun PROPERTIES INTERPROCEDURAL_OPTIMIZATION ON)
target_compile_options(railgun PRIVATE
  $<$<C_COMPILER_ID:GNU>:-finput-charset=UTF-8 -fextended-identifiers -fexec-charset=GBK>
  )
target_compile_definitions(railgun PRIVATE
  _CRT_SECURE_NO_WARNINGS _UNICODE UNICODE
  )
target_link_libraries(railgun PRIVATE vfw32)
