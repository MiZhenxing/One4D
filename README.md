# One4D: Unified 4D Generation and Reconstruction via Decoupled LoRA Control

**[Zhenxing Mi](https://mizhenxing.github.io), [Yuxin Wang](https://w-ted.github.io), [Dan Xu](https://www.danxurgb.net)**
<br>
**The Hong Kong University of Science and Technology (HKUST)**

[![Arxiv](https://img.shields.io/badge/ArXiv-2511.18922-b31b1b.svg)](https://arxiv.org/abs/2511.18922)
[![Paper](https://img.shields.io/badge/PDF-Read%20Paper-red)](https://arxiv.org/pdf/2511.18922)
[![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Paper-yellow)](https://huggingface.co/)
[![Website](https://img.shields.io/badge/Project-Website-blue)](https://mizhenxing.github.io/One4D/)

<div align="center">
  <video src="https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_1.mp4" width="100%" autoplay loop muted></video>
</div>

## 📝 Abstract

**One4D** is a unified framework for **4D generation and reconstruction** that can seamlessly transition between 4D generation from a **single image**, 4D reconstruction from a **full video**, and mixed generation and reconstruction from **sparse frames** via **Unified Masked Conditioning (UMC)**. With **Decoupled LoRA Control (DLC)**, which employs two modality-specific LoRA adapters to form decoupled computation branches for RGB frames and pointmaps, connected by lightweight, zero-initialized control links that gradually learn mutual pixel-level consistency, One4D produces high-quality RGB frames and accurate pointmaps across both generation and reconstruction tasks.

## 🧠 Methodology

### Unified Framework

<div align="center">
  <img src="https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/pics/framework.png" width="100%" alt="One4D Framework">
</div>

*Figure 1: The One4D Unified Framework architecture.*

  * **🎛️ Unified Masked Conditioning (UMC):** Enables seamlessly transition between 4D generation from a **single image**, 4D reconstruction from a **full video**, and mixed generation and reconstruction from **sparse frames** using a single unified model.
  * **🧩 Decoupled LoRA Control (DLC):** Decouples RGB and XYZ computation to minimize interference while maintaining pixel-wise cross-modal control.

### Architecture Comparison

<div align="center">
  <img src="https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/pics/arch_compare.png" width="100%" alt="Architecture Comparison">
</div>

*Figure 2: Comparison of Decoupled LoRA Control against other architectures.*
## 🎨 Results Showcase

### 1. Single Image to 4D
Generating a consistent 4D scene from a single input image.

* [![Scene 1](https://img.shields.io/badge/▶-Watch_Scene_1-red)](https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_2.mp4)
* [![Scene 2](https://img.shields.io/badge/▶-Watch_Scene_2-red)](https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_6.mp4)
* [![Scene 3](https://img.shields.io/badge/▶-Watch_Scene_3-red)](https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_3.mp4)
* [![Scene 4](https://img.shields.io/badge/▶-Watch_Scene_4-red)](https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_4.mp4)
* [![Scene 5](https://img.shields.io/badge/▶-Watch_Scene_5-red)](https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_5.mp4)

### 2. Sparse Frames to 4D
Reconstructing the 4D scene given only a few sparse frames.

* [![Example 1](https://img.shields.io/badge/▶-Watch_Example_1-blue)](https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_7.mp4)
* [![Example 2](https://img.shields.io/badge/▶-Watch_Example_2-blue)](https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_8.mp4)
* [![Example 3](https://img.shields.io/badge/▶-Watch_Example_3-blue)](https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_11.mp4)
* [![Example 4](https://img.shields.io/badge/▶-Watch_Example_4-blue)](https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_12.mp4)
* [![Example 5](https://img.shields.io/badge/▶-Watch_Example_5-blue)](https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_13.mp4)

### 3. Full Video to 4D
High-fidelity reconstruction from a full video input.

* [![Reconstruction 1](https://img.shields.io/badge/▶-Watch_Reconstruction_1-darkgreen)](https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_9.mp4)
* [![Reconstruction 2](https://img.shields.io/badge/▶-Watch_Reconstruction_2-darkgreen)](https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_10.mp4)
* [![Reconstruction 3](https://img.shields.io/badge/▶-Watch_Reconstruction_3-darkgreen)](https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_14.mp4)
* [![Reconstruction 4](https://img.shields.io/badge/▶-Watch_Reconstruction_4-darkgreen)](https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_15.mp4)
* [![Reconstruction 5](https://img.shields.io/badge/▶-Watch_Reconstruction_5-darkgreen)](https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_16.mp4)

## 📖 BibTeX

If you find our work useful for your research, please consider citing us:

```bibtex
@article{mione4d2025,
  title={One4D: Unified 4D Generation and Reconstruction via Decoupled LoRA Control},
  author={Mi, Zhenxing and Wang, Yuxin and Xu, Dan},
  journal={arXiv preprint arXiv:2511.18922},
  year={2025}
}
```