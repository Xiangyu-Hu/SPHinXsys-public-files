# Bundled dependency

`oneapi-for-nvidia-gpus-2025.2.0-linux.sh` is the unmodified Codeplay NVIDIA
adapter installer for Intel oneAPI 2025.2.0. It is bundled so CUDA 12.3 builds
do not depend on locating a retired download link.

- Size: 318,643 bytes.
- SHA-256: `84c0225131da6d066144a56ab3bd6213314a894ef4346d400140185b2f97bdc7`.
- The original copyright notices and embedded license remain in the installer.
- `LICENSE_oneAPI_for_nvidia_GPUs.md` is an unchanged copy of its included license
  (Apache 2.0 with LLVM Exceptions).
- Vendor documentation: https://developer.codeplay.com/products/oneapi/nvidia/2025.2.0/guides/get-started-guide-nvidia.html

`dependencies.py` checks this directory before additional `--cache` directories
and verifies both file size and hash before use. It does not execute installers;
they run only inside the Docker build stages. Other, larger archives are fetched
using `dependencies.lock.json` or supplied by the user as a local cache.
