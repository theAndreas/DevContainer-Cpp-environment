# DevContainer C++ environment

Small example C++ project configured for development inside a devcontainer.

## Prerequisites
- Docker (for devcontainer) or a Linux environment with `cmake`, `ninja`, `gcc/clang`, `gdb`/`lldb`.
- VS Code with the CMake Tools and C/C++ extensions.

## Build (Debug)
From the workspace root:

```bash
cmake -S . -B build -DCMAKE_BUILD_TYPE=Debug
cmake --build build -j $(nproc)
```

This produces the executable at `build/main`.

## Debugging
Options:

- Use the CMake Tools extension: set the build variant to `Debug`, then `CMake: Configure`, `CMake: Build`, and `CMake: Debug Target` → choose `main`.
- Use the provided VS Code launch configurations (Run view) — `Debug main (gdb)`, `Debug main (lldb)`, or `Debug main (gdb, external console)`.

## Notes
- `.gitignore` excludes `build/` and clangd cache files.
- The repository has been pushed to: https://github.com/theAndreas/DevContainer-Cpp-environment
