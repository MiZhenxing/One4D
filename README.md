# One4D: Unified 4D Generation and Reconstruction via Decoupled LoRA Control

**[Zhenxing Mi](https://mizhenxing.github.io), [Yuxin Wang](https://w-ted.github.io), [Dan Xu](https://www.danxurgb.net)**
<br>
**The Hong Kong University of Science and Technology (HKUST)**

[![Arxiv](https://img.shields.io/badge/ArXiv-2511.18922-b31b1b.svg)](https://arxiv.org/abs/2511.18922)
[![Paper](https://img.shields.io/badge/PDF-Read%20Paper-red)](https://arxiv.org/pdf/2511.18922)
[![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Paper-yellow)](https://huggingface.co/)
[![Website](https://img.shields.io/badge/Project-Website-blue)](https://mizhenxing.github.io/One4D/)

<div align="center">
  <video src="https://github.com/user-attachments/assets/4bcc7f4f-4368-4332-8423-6bd428922448" width="100%" autoplay loop muted></video>
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
<div align="center">
  <video src="https://github.com/user-attachments/assets/e0767b37-3069-4902-a28d-adfdcca0078e" autoplay loop muted playsinline width="100%"></video>
</div>
<div align="center">
  <video src="https://github.com/user-attachments/assets/3b97cafc-acb3-40df-b815-8b39fe84c323" autoplay loop muted playsinline width="100%"></video>
</div>
<div align="center">
  <video src="https://github.com/user-attachments/assets/081b66fa-7e15-42cf-bf73-5cc5353ce039" autoplay loop muted playsinline width="100%"></video>
</div>
<div align="center">
  <video src="https://github.com/user-attachments/assets/4875b35d-d58c-471e-ad66-81f43f2f3337" autoplay loop muted playsinline width="100%"></video>
</div>
<div align="center">
  <video src="https://github.com/user-attachments/assets/5d590675-1b99-4ee2-80a9-1825558b4044" autoplay loop muted playsinline width="100%"></video>
</div>

### 2. Sparse Frames to 4D
Reconstructing the 4D scene given only a few sparse frames.

<div align="center">
<video src="https://github.com/user-attachments/assets/2915058d-412f-49c0-91e7-06c8bdc98a51" autoplay loop muted playsinline width="100%"></video>
</div>
<div align="center">
<video src="https://github.com/user-attachments/assets/a3ab73c6-4028-4fba-bfef-0e2c2839aab7" autoplay loop muted playsinline width="100%"></video>
</div>
<div align="center">
<video src="https://github.com/user-attachments/assets/49112197-f989-4836-9a7e-165c86a1194b" autoplay loop muted playsinline width="100%"></video>
</div>
<div align="center">
<video src="https://github.com/user-attachments/assets/6ad05f92-5629-4d22-90c9-de17a84881b1" autoplay loop muted playsinline width="100%"></video>
</div>
<div align="center">
<video src="https://github.com/user-attachments/assets/d4799227-ea23-4263-987a-3b22d1603ea5" autoplay loop muted playsinline width="100%"></video>
</div>

### 3. Full Video to 4D
High-fidelity reconstruction from a full video input.

<div align="center">
<video src="https://github.com/user-attachments/assets/913a010b-72dc-4d22-b32d-824a9b154d63" autoplay loop muted playsinline width="100%"></video>
</div>
<div align="center">
<video src="https://github.com/user-attachments/assets/9f9bbf06-6ab2-4245-8092-bb0b3de4b716" autoplay loop muted playsinline width="100%"></video>
</div>
<div align="center">
<video src="https://github.com/user-attachments/assets/44047d58-7f83-4b99-b32f-2ffbb3ffddad" autoplay loop muted playsinline width="100%"></video>
</div>
<div align="center">
<video src="https://github.com/user-attachments/assets/79f5068b-0729-4861-bd58-9274586f4ca3" autoplay loop muted playsinline width="100%"></video>
</div>
<div align="center">
<video src="https://github.com/user-attachments/assets/7a1780fc-fe41-4a50-b197-fa9a6a22576c" autoplay loop muted playsinline width="100%"></video>
</div>

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
