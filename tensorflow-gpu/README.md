Creates a devcontainer for tensorflow development.
It container:

# BASE IMAGE:
  mcr.microsoft.com/devcontainers/python:1-3.10-bookworm

# tensorflow
- version : 2.18.0

# nvidia-smi
- NVIDIA-SMI 565.51.01
- Driver Version: 565.90
- CUDA Version: 12.7


# Swig
For GUI support from inside the container. Download Xlaunch for support.
