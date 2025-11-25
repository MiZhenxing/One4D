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
Generating a consistent 4D scene from a single input image, ensuring high-quality RGB frames and consistent geometry for the entire 4D output.

<table width="100%">
  <tr>
    <td width="50%">
      <div align="center">
        <video src="https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_2.mp4" autoplay loop muted playsinline></video>
        <br>
        <strong>Example 1</strong>
      </div>
    </td>
    <td width="50%">
      <div align="center">
        <video src="https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_6.mp4" autoplay loop muted playsinline></video>
        <br>
        <strong>Example 2</strong>
      </div>
    </td>
  </tr>
  <tr>
    <td width="50%">
      <div align="center">
        <video src="https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_3.mp4" autoplay loop muted playsinline></video>
        <br>
        <strong>Example 3</strong>
      </div>
    </td>
    <td width="50%">
      <div align="center">
        <video src="https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_4.mp4" autoplay loop muted playsinline></video>
        <br>
        <strong>Example 4</strong>
      </div>
    </td>
  </tr>
  <tr>
    <td width="50%">
      <div align="center">
        <video src="https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_5.mp4" autoplay loop muted playsinline></video>
        <br>
        <strong>Example 5</strong>
      </div>
    </td>
    <td width="50%">
      </td>
  </tr>
</table>

### 2. Sparse Frames to 4D
Reconstructing the 4D scene given only a few sparse frames. One4D interpolates the missing information utilizing Unified Masked Conditioning.

<table width="100%">
  <tr>
    <td width="50%">
      <div align="center">
        <video src="https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_7.mp4" autoplay loop muted playsinline></video>
        <br>
        <strong>Example 1</strong>
      </div>
    </td>
    <td width="50%">
      <div align="center">
        <video src="https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_8.mp4" autoplay loop muted playsinline></video>
        <br>
        <strong>Example 2</strong>
      </div>
    </td>
  </tr>
  <tr>
    <td width="50%">
      <div align="center">
        <video src="https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_11.mp4" autoplay loop muted playsinline></video>
        <br>
        <strong>Example 3</strong>
      </div>
    </td>
    <td width="50%">
      <div align="center">
        <video src="https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_12.mp4" autoplay loop muted playsinline></video>
        <br>
        <strong>Example 4</strong>
      </div>
    </td>
  </tr>
  <tr>
    <td width="50%">
      <div align="center">
        <video src="https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_13.mp4" autoplay loop muted playsinline></video>
        <br>
        <strong>Example 5</strong>
      </div>
    </td>
    <td width="50%">
      </td>
  </tr>
</table>

### 3. Full Video to 4D
High-fidelity reconstruction from a full video input, ensuring temporal consistency and accurate geometry estimation.

<table width="100%">
  <tr>
    <td width="50%">
      <div align="center">
        <video src="https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_9.mp4" autoplay loop muted playsinline></video>
        <br>
        <strong>Example 1</strong>
      </div>
    </td>
    <td width="50%">
      <div align="center">
        <video src="https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_10.mp4" autoplay loop muted playsinline></video>
        <br>
        <strong>Example 2</strong>
      </div>
    </td>
  </tr>
  <tr>
    <td width="50%">
      <div align="center">
        <video src="https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_14.mp4" autoplay loop muted playsinline></video>
        <br>
        <strong>Example 3</strong>
      </div>
    </td>
    <td width="50%">
      <div align="center">
        <video src="https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_15.mp4" autoplay loop muted playsinline></video>
        <br>
        <strong>Example 4</strong>
      </div>
    </td>
  </tr>
  <tr>
    <td width="50%">
      <div align="center">
        <video src="https://raw.githubusercontent.com/MiZhenxing/MiZhenxing.github.io/main/One4D/assets/videos/cut_16.mp4" autoplay loop muted playsinline></video>
        <br>
        <strong>Example 5</strong>
      </div>
    </td>
    <td width="50%">
      </td>
  </tr>
</table>

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