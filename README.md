# Learing C++ UI with Dear ImGui

This repo is a base project using CMake and vcpkg to install imgui and generate a sln to work in.

See the [Dear ImGui git repository](https://github.com/ocornut/imgui) for information on imgui.

## Getting Started

1. Download and install [CMake](https://cmake.org/) 
2. Download and install [vcpkg](https://learn.microsoft.com/en-us/vcpkg/get_started/get-started?pivots=shell-cmd#1---set-up-vcpkg)
3. Download and install [Visual Studio 2022](https://visualstudio.microsoft.com/vs/)
  > Ensure to include the CMake additional module when installing VS2022
4. Create new repo using template and git clone to local machine
5. Run `cmake .` inside root of local git repo
6. Open the generated `LearningUICpp.sln` solution
7. Right click `LearningUICpp.sln` in Solution Explorer -> Select `Set as Startup Project`
8. Run with `F5` or `Ctrl+F5`

## Notes
1. This project is using the `docking` branch of imgui to provide multi-view and docking support
2. This project uses >= v1.91.0 of ImGui
3. This project is generated to use DX12 and Win32 APIs. If you'd like to use a different set of APIs update the vcpkg.json, update the `main.cpp` using the [examples from imgui](https://github.com/ocornut/imgui/tree/docking/examples), and re-generate the SLN using step 5 in `Getting Started`

