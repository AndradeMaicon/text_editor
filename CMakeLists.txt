# CMakeList.txt: projeto de CMake para text_editor, incluir origem e definir
# lógica específica a um projeto aqui.
#
cmake_minimum_required (VERSION 3.8)

# Enable Hot Reload for MSVC compilers if supported.
if (POLICY CMP0141)
  cmake_policy(SET CMP0141 NEW)
  set(CMAKE_MSVC_DEBUG_INFORMATION_FORMAT "$<IF:$<AND:$<C_COMPILER_ID:MSVC>,$<CXX_COMPILER_ID:MSVC>>,$<$<CONFIG:Debug,RelWithDebInfo>:EditAndContinue>,$<$<CONFIG:Debug,RelWithDebInfo>:ProgramDatabase>>")
endif()

project ("text_editor")

# Adicione a origem ao executável deste projeto.
add_executable (text_editor "text_editor.cpp" "text_editor.h")

if (CMAKE_VERSION VERSION_GREATER 3.12)
  set_property(TARGET text_editor PROPERTY CXX_STANDARD 20)
endif()

  find_package(FLTK CONFIG REQUIRED)
  target_link_libraries(text_editor PRIVATE fltk fltk_gl fltk_forms fltk_images)

# TODO: Adicione testes e instale destinos, se necessário.
