# genecode
```
python main.py --operations=conv,gemm --curr-build-dir=build --architectures=80 --cuda-version=11.0.0
```

# usage
```
usage: main.py [-h] [--operations OPERATIONS] [--build-dir BUILD_DIR]
               [--curr-build-dir CURR_BUILD_DIR]
               [--generator-target GENERATOR_TARGET]
               [--architectures ARCHITECTURES] [--kernels KERNELS]
               [--ignore-kernels IGNORE_KERNELS] [--filter-by-cc FILTER_BY_CC]
               [--cuda-version CUDA_VERSION]
               [--kernel-filter-file KERNEL_FILTER_FILE]
               [--selected-kernel-list SELECTED_KERNEL_LIST]
               [--interface-dir INTERFACE_DIR]

Generates device kernel registration code for CUTLASS Kernels

optional arguments:
  -h, --help            show this help message and exit
  --operations OPERATIONS
                        Specifies the operation to generate (gemm, all)
  --build-dir BUILD_DIR
                        CUTLASS top-level build directory
  --curr-build-dir CURR_BUILD_DIR
                        CUTLASS current build directory. cmake files will be
                        emitted in this directory
  --generator-target GENERATOR_TARGET
                        Target of CUTLASS Library Generator.
  --architectures ARCHITECTURES
                        Target compute architectures
  --kernels KERNELS     Comma delimited list to filter kernels by name.
  --ignore-kernels IGNORE_KERNELS
                        Comma delimited list of kernels to exclude from build.
  --filter-by-cc FILTER_BY_CC
                        If enabled, kernels whose comupte capability range is
                        not satisfied by the build target are excluded.
  --cuda-version CUDA_VERSION
                        Semantic version string of CUDA Toolkit
  --kernel-filter-file KERNEL_FILTER_FILE
                        Full path of filter file
  --selected-kernel-list SELECTED_KERNEL_LIST
                        Specify the output log file containing all enabled
                        kernels in this build
  --interface-dir INTERFACE_DIR
                        Interface header to kernels
```