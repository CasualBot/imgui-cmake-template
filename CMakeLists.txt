# CMakeList.txt : CMake project for LearningUICpp, include source and define
# project specific logic here.
#
cmake_minimum_required(VERSION 3.10)


if(DEFINED ENV{VCPKG_ROOT})
    set(CMAKE_TOOLCHAIN_FILE $ENV{VCPKG_ROOT}/scripts/buildsystems/vcpkg.cmake CACHE STRING "")
endif()

project ("LearningUICpp")

find_package(imgui CONFIG REQUIRED)
# Add source to this project's executable.
add_executable (LearningUICpp "main.cpp")

target_link_libraries(LearningUICpp PRIVATE imgui::imgui)

# Enable Hot Reload for MSVC compilers if supported.
if (POLICY CMP0141)
  cmake_policy(SET CMP0141 NEW)
  set(CMAKE_MSVC_DEBUG_INFORMATION_FORMAT "$<IF:$<AND:$<C_COMPILER_ID:MSVC>,$<CXX_COMPILER_ID:MSVC>>,$<$<CONFIG:Debug,RelWithDebInfo>:EditAndContinue>,$<$<CONFIG:Debug,RelWithDebInfo>:ProgramDatabase>>")
endif()

if (CMAKE_VERSION VERSION_GREATER 3.12)
  set_property(TARGET LearningUICpp PROPERTY CXX_STANDARD 20)

endif()
# TODO: Add tests and install targets if needed.
