**sdb**

A native x64 Linux debugger implemented in C++, following Building a Debugger by Sy Brand.

**About**

This repository tracks my progress as I work through the book, learning about debugger internals, Linux system programming, and C++ development.

The goal is to build a debugger incrementally, understanding the underlying concepts and implementation details rather than simply reproducing the code.

**Development Environment**
Language: C++
Platform: Linux (Ubuntu on WSL)
Build system: CMake
Version control: Git

Additional dependencies and tools will be documented as they are introduced.

**Building**

Build instructions will be updated as the project evolves.

The project is developed and built inside WSL using Linux development tools.

**Progress**
Initialize the project repository
Chapter 1 — Project setup and dependencies
Subsequent chapters — To be updated as I progress through the book
Repository Structure

The directory structure follows the project's implementation and evolves as new components are introduced.

src/ — Source code
include/ — Header files
test/ — Tests
tools/ — Development tools
CMakeLists.txt — CMake build configuration

**Learning Notes**

This repository is primarily a hands-on learning project. Implementation decisions, debugging notes, and lessons learned will be recorded alongside the code as needed.

**Reference**

Sy Brand, Building a Debugger: Write a Native x64 Debugger From Scratch, No Starch Press.

**System Dependencies (Ubuntu / WSL)**

  Install the following system packages before configuring the project:
  
    sudo apt update
    sudo apt install build-essential cmake git pkg-config libedit-dev catch2
  
  
  The project also uses vcpkg for dependencies declared in vcpkg.json.
  
  Configure and build from the repository root:
  
    cmake -S . -B build \
      -DCMAKE_TOOLCHAIN_FILE="$HOME/lrn/packages/vcpkg/vcpkg/scripts/buildsystems/vcpkg.cmake"
    
    cmake --build build
  
  
  Run tests with:
  
    ctest --test-dir build --output-on-failure
