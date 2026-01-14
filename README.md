# FD-DIT: Frequency Domain-Directed Diffusion Transformer for Low-Dose CT Reconstruction
[![arXiv](https://img.shields.io/badge/arXiv-2506.23466-b31b1b.svg)](https://arxiv.org/abs/2506.23466)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
This repository contains the PyTorch implementation of the paper **"FD-DIT: Frequency Domain-Directed Diffusion Transformer for Low-Dose CT Reconstruction"**.
> **Code Availability:** The source code is available at [https://github.com/yqx7150/FD-DIT](https://github.com/yqx7150/FD-DIT).

## Abstract
Low-dose computed tomography (LDCT) re-duces radiation exposure but suffers from image artifacts and loss of detail due to quantum and electronic noise, po-tentially impacting diagnostic accuracy.Transformer com-bined with diffusion models has been a promising approach for image generation. Nevertheless, existing methods ex-hibitlimitations in preserving fine-grained image details. To address this issue, frequency domain-directed diffusion transformer(FD-DiT)is proposed for LDCTreconstruc-tion. FD-DiTcenters on a diffusion strategy that progres-sively introduces noise until the distribution statistically aligns with that of LDCT data, followed by denoising pro-cessing. Furthermore, we employ a frequency decoupling technique to concentrate noise primarily in high-frequency domain, thereby facilitating effective capture of essential anatomical structures and fine details. A hybrid denoising network is then utilized to optimize the overall datarecon-struction process. To enhance the capability in recognizing high-frequency noise, we incorporate sliding sparse localat-tention to leverage the sparsity and locality of shallow-layer information, propagating them via skip connections for im-proving feature representation. Finally, we propose a learn-able dynamic fusion strategy for optimal component inte-gration. Experimental results demonstrate that at identical dose levels, LDCT images reconstructed byFD-DiT exhibit superior noise and artifact suppression compared to state-of-the-art methods.

Index Terms—Low-dose CT, diffusion transformer, frequencydomain, sinogram domain,multi-network learning.

## 🚀 Key Features

* **Generalized Diffusion Strategy:** Perturbs data towards the specific LDCT distribution rather than a random Gaussian distribution, improving feature retention during the reverse process.
* **Frequency-Aware Architecture:** Decomposes sinogram data into frequency subbands (High, Low, Full) via Gaussian filtering to target specific noise characteristics.
* **Sliding Sparse Local Attention (SSLA):** A novel attention mechanism in the FHD module that captures local high-frequency features with reduced computational cost, tailored for sparse and localized noise patterns.
* **Multi-Network Learning:** Synergistically combines the global context capability of Transformers (for high frequencies) with the local inductive bias of CNNs (for low frequencies).
* **Robust Reconstruction:** Integrates Penalized Weighted Least-Squares (PWLS) and Total Variation (TV) regularization during iterative reconstruction to ensure data fidelity.
