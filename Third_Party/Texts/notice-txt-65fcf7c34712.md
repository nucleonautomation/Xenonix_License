# NOTICE.txt

[Browse libraries](../README.md) · [Repository home](../../README.md)

Original-file SHA-256: `65fcf7c3471202b80c97289418f6c842bbb49f25216dc9af03699acb508545ad`

## License and notices

````text
This upstream cuda-toolkit release is a metadata-only dependency selector, containing no executable library code. No separate license file is supplied in its wheel. The selected CUDA components carry their own license texts in this reference.

# cuda-toolkit 13.0.2

### [NVIDIA CUDA Toolkit](https://developer.nvidia.com/cuda-toolkit)

> The NVIDIA CUDA Toolkit provides a development environment for creating high-performance, GPU-accelerated applications. With it, you can develop, optimize, and deploy your applications on GPU-accelerated embedded systems, desktop workstations, enterprise data centers, cloud-based platforms, and supercomputers. The toolkit includes GPU-accelerated libraries, debugging and optimization tools, a C/C++ compiler, and a runtime library.

### `cuda-toolkit` package

The `cuda-toolkit` package is a meta-package (a package that contains no software and only installs other packages) to install all or part of the NVIDIA CUDA Toolkit.

For instructions on how to use the `cuda-toolkit` package, please refer to the [NVIDIA CUDA Toolkit documentation](https://docs.nvidia.com/cuda/) and follow the installation guide for your platform. A summary of usage is also available below.

### Using the `cuda-toolkit` package

The `cuda-toolkit` package uses package extras to install all or part of the CUDA Toolkit.
Some examples of using the `cuda-toolkit` meta-package with extras:

Install all of the CUDA Toolkit
```
pip install cuda-toolkit[all]
```

Install just the CUDA Runtime
```
pip install cuda-toolkit[cudart]
```

Install cuBLAS, cuSOLVER, and cuSPARSE
```
pip install cuda-toolkit[cublas,cusolver,cusparse]
```

### Available extras

| Extra | Package | Version |
|-------|---------|---------|
| `all` | All packages below |  |
| cccl | nvidia-cuda-cccl | 13.0.85  |
| crt | nvidia-cuda-crt | 13.0.88  |
| cublas | nvidia-cublas | 13.1.0.3  |
| cudart | nvidia-cuda-runtime | 13.0.96  |
| cufft | nvidia-cufft | 12.0.0.61  |
| cufile | nvidia-cufile | 1.15.1.6  |
| culibos | nvidia-cuda-culibos | 13.0.85  |
| cupti | nvidia-cuda-cupti | 13.0.85  |
| curand | nvidia-curand | 10.4.0.35  |
| cusolver | nvidia-cusolver | 12.0.4.66  |
| cusparse | nvidia-cusparse | 12.6.3.3  |
| cuxxfilt | nvidia-cuda-cuxxfilt | 13.0.85  |
| npp | nvidia-npp | 13.0.1.2  |
| nvcc | nvidia-cuda-nvcc | 13.0.88  |
| nvfatbin | nvidia-nvfatbin | 13.0.85  |
| nvjitlink | nvidia-nvjitlink | 13.0.88  |
| nvjpeg | nvidia-nvjpeg | 13.0.1.86  |
| nvml | nvidia-nvml-dev | 13.0.87  |
| nvptxcompiler | nvidia-nvptxcompiler | 13.0.88  |
| nvrtc | nvidia-cuda-nvrtc | 13.0.88  |
| nvtx | nvidia-nvtx | 13.0.85  |
| nvvm | nvidia-nvvm | 13.0.88  |
| opencl | nvidia-cuda-opencl | 13.0.85  |
| profiler | nvidia-cuda-profiler-api | 13.0.85  |
| sanitizer | nvidia-cuda-sanitizer-api | 13.0.85  |
````

## Where this notice appears

- [cuda-toolkit 13.0.2](../Libraries/cuda-toolkit/13.0.2/README.md) — `cuda-toolkit-13.0.2/upstream/NOTICE.txt`
