# MaizeLens · 玉米慧眼

Deep learning experiments for maize leaf disease classification. / 基于深度学习的玉米叶片病害识别与模型对比。

MaizeLens combines **maize** and **lens**: a lens for understanding maize leaf health.

## What is included

- Four classes: Healthy (0), Common Rust (1), Blight (2), Gray Leaf Spot (3).
- PyTorch image preprocessing, data augmentation and an 80/20 training/validation split.
- English notebook comparing ResNet18/50/101/152, TResNet, ViT and ResNeXt101.
- Chinese annotated notebook focused on ResNet18.
- Training curves, confusion matrices and prediction CSV generation in the notebooks.

## Project files

```text
English.ipynb                 Main experiments and model comparison
Chinese.ipynb                 Chinese annotated experiment
requirements.txt              Dependencies inferred from notebook imports
submission.csv                Original saved predictions (not a measured score)
data/train.csv                Training image IDs and labels
data/random_submission.csv    Example submission / placeholder labels
```

Notebook outputs have been cleared for a smaller, readable repository. The original ZIP is unchanged. Dataset images and generated copies are excluded from Git; the local prepared copy retains the original images in `data/train/` and `data/test/`.

## Getting started

Use a Python environment compatible with PyTorch and torchvision. From the project root:

```bash
python -m venv .venv
# Windows PowerShell:
.venv\Scripts\Activate.ps1
# macOS / Linux:
# source .venv/bin/activate
python -m pip install -r requirements.txt
jupyter lab
```

If cloning from GitHub, obtain the original dataset separately and restore the layout below. Dataset source and redistribution terms were not provided in the archive.

```text
data/
  train.csv
  random_submission.csv
  train/<Image ID>.jpg
  test/<Image ID>.jpg
```

Open `English.ipynb` from the project root and run the desired model sections in order after shared preprocessing and function definitions. The notebooks create `train/`, `test/` and `splitted_data/` automatically. Pretrained weights require internet access; training is substantially faster with a compatible GPU. No trained checkpoint is included.


## 中文说明

“玉米慧眼”通过叶片图片识别健康、普通锈病、叶枯病和灰斑病，并比较多种迁移学习模型。本仓库保留原始实验代码，补充依赖和运行说明；图片数据、训练权重及自动生成的重复目录不纳入版本管理。它是研究实验项目，尚未包含在线预测界面或网站部署。
