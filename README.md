# MS-FDD
Multi-Scale Fatigue Driving Detection

# 🚗 MS-FDD: Multi-Scale Fatigue Driving Detection

> **MS-FDD** is an advanced fatigue driving detection framework that leverages multi-scale convolutional attention mechanisms and an improved neck structure with BiFPN and SE modules, enabling accurate and lightweight real-time fatigue monitoring.

## 🌟 Features
Feature-Enhanced Multi-Scale Convolution Module (FE-MSC)
Lightweight Adaptive Pyramid Fusion Module (LAPF)
Selective Compression Convolution Head (SCCH)

## 🧪 Experimental Environment

| Component | Version / Info                   |
| --------- | -------------------------------- |
| OS        | Ubuntu 20.04 / 22.04             |
| Python    | 3.8+                             |
| PyTorch   | 2.0+ (CUDA 11.7)                 |
| CUDA      | 11.3 or above                    |
| cuDNN     | 8.x                              |
| GPU       | NVIDIA RTX 3090 / 4090 (24 GB)   |
| Other     | OpenCV, tqdm, matplotlib, PyYAML |


## 🏗️ Architecture
```
Input Image ➜ Backbone (SPPF + MSCA) ➜ Neck (BiFPN-SE Fusion) ➜ Head (SCCH) ➜ Fatigue State Prediction
```

---

## 🚀 Quick Start

### Clone this repo

```bash
git clone https://github.com/SCNU-RISLAB/MS-FDD.git
cd MS-FDD
```


### Prepare your dataset
Organize your data following YOLO format or convert datasets (e.g., YawDD, NTHU-DDD) to YOLO-style annotations.
```
dataset/
  images/
    train/
    val/
  labels/
    train/
    val/
  class.yaml/
```
<class.yaml>
train:# 训练集图片路径
val: # 验证集图片路径
# 类别数量
nc: 2
# 类别名称
names: [ 'drowsy', 'undrowsy']

### Train the model
```bash
python train.py --data configs/fatigue.yaml --img-size 640 --batch-size 32 --epochs 150 --device 0
```

---

## 📄 Citation

If you use this repository or models in your work, please cite:

```
@article{your2024msfdd,
  title={MS-FDD: Multi-Scale Fatigue Driving Detection with Edge-Cloud Collaboration},
  author={Yating Li et al.},
  journal={ArXiv preprint arXiv:xxxx.xxxxx},
  year={2024}
}
```

## ✉️ Contact

If you have any questions or collaborations, please reach out to **[20238131037@m.scnu.edu.cn]** or open an issue.

---

### ⭐️ If you like this project, please give it a star! ⭐️

---
