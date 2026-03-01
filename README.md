# DevContainer C++ environment

Small example C++ project configured for development inside a devcontainer.

## Prerequisites
- Docker (for devcontainer) or a Linux environment with `cmake`, `ninja`, `gcc/clang`, `gdb`/`lldb`.
- VS Code: if you open this workspace in the devcontainer, VS Code will automatically install the recommended extensions listed in `.devcontainer/devcontainer.json`.
  If you open the folder without the devcontainer, please install the extensions listed below.

### Recommended VS Code Extensions
When opening this workspace in the devcontainer, these extensions are automatically installed:
- **C/C++** (`ms-vscode.cpptools`) — Microsoft's C/C++ extension for IntelliSense, debugging, and code exploration.
- **CMake Tools** (`ms-vscode.cmake-tools`) — Build, test, and debug support for CMake projects.
- **Clang Language Server** (`llvm-vs-code-extensions.vscode-clangd`) — Fast, accurate C/C++ language server (alternative to cpptools IntelliSense).

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
