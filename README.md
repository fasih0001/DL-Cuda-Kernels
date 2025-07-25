# DL-Cuda-Kernels
A collection of cuda kernels for deep learning inference optimization

# CUDA Kernels Project Structure

```
dl_cuda_kernels/
├── CMakeLists.txt                    # 🟩 Root CMake file (build entry point)
│
├── kernels/                          # Core kernel module
│   ├── CMakeLists.txt               # 🟦 Builds `cuda_kernels` static library
│   ├── include/                     # Public headers (.cuh) for CUDA kernels
│   ├── src/                         # Kernel implementation files (.cu)
│   ├── tests/                       # Unit and functional test programs for kernels
│   │   └── CMakeLists.txt          # 🟨 Builds test binaries (linked to cuda_kernels)
│   └── utils/                       # Common CUDA helpers (e.g., error checking, timers)
│
├── benchmarks/                       # Performance testing and profiling utilities
│   └── CMakeLists.txt               # 🟧 Builds benchmarks (linked to cuda_kernels)
│
└── out/                             # Build output directory for compiled binaries
```

## Directory Overview

- **Root (`CMakeLists.txt`)** 🟩: Main build configuration and project entry point
- **`kernels/`**: Core CUDA kernel implementation module
  - Contains the main static library build configuration
  - Includes public headers, source files, tests, and utilities
- **`benchmarks/`**: Performance testing and profiling tools
- **`out/`**: Generated build artifacts and compiled binaries