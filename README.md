# LMIF: A Large-scale Multi-focus Image Fusion Dataset Based on Smartphones
Official Repository for LMIF Dataset | 基于智能手机的大规模多焦点图像融合数据集

[![IEEE Paper](https://img.shields.io/badge/IEEE-ICCVIT2025-blue)]()
[![Dataset License](https://img.shields.io/badge/License-NonCommercial%20Academic-green)]()
[![Paper DOI](https://img.shields.io/badge/DOI-10.1109/ICCVIT67848.2025.11391393-orange)]()

## 📖 Project Introduction
Due to the limited depth of field of optical lenses, a single photo cannot make all objects in the scene clear at the same time. Multi-focus image fusion technology solves this problem by fusing multiple images with different focal planes into an all-in-focus clear image.

Most existing public multi-focus datasets are collected by professional cameras, which cannot simulate the real shooting characteristics of mobile phones in daily scenarios. To fill this gap, we construct the **LMIF dataset** captured by mainstream consumer smartphones, which can better evaluate the generalization ability of fusion algorithms on real mobile photography data.

### Paper Information
- Title: LMIF: A Large-scale Multi-Focus Image Fusion Dataset Based on Smartphones
- Conference: 2025 IEEE 3rd International Conference on Computer, Vision and Intelligent Technology (ICCVIT)
- Affiliation: College of Electronic and Information Engineering, Hebei University
- Corresponding Author: Shuaiqi Liu (shdkj-1918@163.com)

## 📦 Dataset Overview
### Basic Information
- Total image pairs: 229 pairs (A:66 / B:63 / C:100)
- Two versions provided: **Raw unprocessed data** + **Preprocessed standardized data (512×512 JPG)**
- Shooting devices: 12 mobile phone models from 7 mainstream brands (Huawei, iPhone, OPPO, Honor, Redmi, iQOO, Samsung, vivo, Realme, OnePlus, Xiaomi)
- Shooting scenes: Campus, indoor desk, balcony, library and other daily real environments
- License: Non-commercial, only for academic research, algorithm verification and teaching demonstration

### Preprocessing Pipeline
We processed raw mobile images to eliminate interference such as jitter, illumination difference and resolution mismatch:
1. Luminance equalization: SHINE color normalization toolbox to unify brightness and contrast
2. Image registration: SIFT feature matching to correct camera shake offset
3. Image cropping & resizing: Uniform 512×512 via nearest-neighbor interpolation

## 📥 Dataset Download
### GitHub Repository Storage
The complete dataset (raw + preprocessed) is stored in this repo, you can download it in two ways:
1. Git clone the whole repository
```bash
git clone https://github.com/cvmdsp/LMIF.git
cd LMIF
