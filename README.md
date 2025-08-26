# flash-attention pre-build wheels

This repository provides wheels for the pre-built [flash-attention](https://github.com/Dao-AILab/flash-attention).

Since building flash-attention takes a **very long time** and is resource-intensive,
I also build and provide combinations of CUDA and PyTorch that are not officially distributed.

The building Github Actions Workflow can be found [here](./.github/workflows/build.yml).  
The built packages are available on the [release page](https://github.com/Seedmanc/flash-attention-prebuild-wheels/releases).

## Table of Contents

- [Install](#install) 
- [Packages](#packages) 
  - [Windows x86_64](#windows-x86_64)
- [History](#history)
- [Original Repository](#original-repository)

## Install

1. Select the versions for Python, CUDA, PyTorch, and flash_attn.

```bash
flash_attn-[flash_attn Version]+cu[CUDA Version]torch[PyTorch Version]-cp[Python Version]-cp[Python Version]-win_amd64.whl

# Example: Python 3.11, CUDA 12.4, PyTorch 2.5, and flash_attn 2.6.3
flash_attn-1.0.9+cu124torch2.6-cp311-cp311-win_amd64.whl
```

2. Find the corresponding version of a wheel from the below [Package section](#packages) and [releases](https://github.com/Seedmanc/flash-attention-prebuild-wheels/releases)

3. Download and Local Install

```bash
# Download and Local Install
wget https://github.com/Seedmanc/flash-attention-prebuild-wheels/releases/download/v109.0.2/flash_attn-1.0.9+cu124torch2.5-cp310-cp310-win_amd64.whl
pip install flash_attn-1.0.9+cu124torch2.5-cp310-cp310-win_amd64.whl
```

## Self build

If you cannot find the version you are looking for, you can fork this repository and create a wheel on GitHub Actions.

1. Fork this repository
2. Edit workflow file [`.github/workflows/build.yml`](https://github.com/Seedmanc/flash-attention-prebuild-wheels/blob/main/.github/workflows/build.yml) to set the version you want to build.
3. Add tag `v*.*.*` to trigger the build workflow.

Please note that depending on the combination of versions, it may not be possible to build.

## Packages

### Windows x86_64

#### Flash-Attention 1.0.9

<details>
<summary>Packages for Flash-Attention 1.0.9</summary>

| Python | PyTorch | CUDA | package |
| ------ | ------- | ---- | ------- |
| 3.11 | 2.6 | 12.4 | [Release1](https://github.com/mjun0812/flash-attention-prebuild-wheels/releases/tag/v10.9.1) |
| 3.10 | 2.5 | 12.4 | [Release1](https://github.com/Seedmanc/flash-attention-prebuild-wheels/releases/tag/v109.0.2) |

</details>

## Original Repository

[repo]([https://github.com/Dao-AILab/flash-attention](https://github.com/mjun0812/flash-attention-prebuild-wheels/))

```bibtex
@inproceedings{dao2022flashattention,
  title={Flash{A}ttention: Fast and Memory-Efficient Exact Attention with {IO}-Awareness},
  author={Dao, Tri and Fu, Daniel Y. and Ermon, Stefano and Rudra, Atri and R{\'e}, Christopher},
  booktitle={Advances in Neural Information Processing Systems (NeurIPS)},
  year={2022}
}
```
