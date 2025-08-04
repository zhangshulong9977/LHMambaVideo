# LHMambaVideo

一个基于 Mamba 架构的视频分析深度学习项目。

## 项目概述

LHMambaVideo 是一个用于视频处理和分析的深度学习模型，采用了先进的 Mamba 状态空间模型架构。该项目包含了完整的模型定义、训练脚本和数据处理流程。

## 主要特性

- 🔥 基于 Mamba 状态空间模型的视频分析架构
- 🎯 支持多类别视频分类任务
- 📊 完整的训练和验证流程
- 🚀 高效的窗口分割和注意力机制
- 📈 可视化训练结果和模型性能

## 项目结构

```
LHMambaVideo/
├── model.py          # 主要模型定义文件
├── train.py          # 训练脚本
├── data/             # 数据目录
│   ├── 0/           # 类别0的视频文件
│   ├── 1/           # 类别1的视频文件  
│   ├── 2/           # 类别2的视频文件
│   └── 3/           # 类别3的视频文件
├── assert/          # 资源文件
│   └── fig1.png     # 项目相关图表
└── README.md        # 项目说明文档
```

## 模型架构

### 核心组件

1. **窗口分割机制**: 将输入视频帧分割为固定大小的窗口，提高计算效率
2. **Mamba 状态空间模型**: 采用选择性扫描机制处理序列数据
3. **多层感知机**: 用于特征变换和分类
4. **LayerNorm 和 DropPath**: 提供正则化和训练稳定性

### 模型可视化

![模型架构图](assert/fig1.png)

*图1: LHMambaVideo 模型架构示意图*

## 安装依赖

```bash
pip install torch torchvision
pip install timm
pip install mamba-ssm
pip install einops
pip install opencv-python
pip install pandas
pip install pillow
pip install numpy
```

## 使用方法

### 数据准备

1. 将视频文件按类别放入 `data/` 目录下的对应子文件夹
2. 确保视频格式为 `.mp4`
3. 创建相应的标签文件（CSV格式）

### 训练模型

```bash
python train.py
```

### 主要参数

- `data_dir`: 数据集路径
- `batch_size`: 批处理大小
- `learning_rate`: 学习率
- `epochs`: 训练轮数

## 模型特点

### 窗口分割
```python
def window_partition(x, window_size):
    # 将输入特征图分割为固定大小的窗口
    # 提高计算效率和局部特征提取能力
```

### Mamba 架构
- 采用选择性扫描机制
- 高效处理长序列数据
- 减少计算复杂度

## 性能表现

- **模型大小**: 相对轻量化的网络结构
- **计算效率**: 优化的窗口处理机制
- **准确性**: 在视频分类任务上表现优异

## 数据集信息

当前支持的数据集包含4个类别：
- 类别 0: 20个视频样本
- 类别 1: 20个视频样本  
- 类别 2: 20个视频样本
- 类别 3: 20个视频样本

## 贡献指南

欢迎提交 Issue 和 Pull Request 来改进这个项目！

## 许可证

本项目基于 MIT 许可证开源。

## 联系方式

如有问题或建议，请通过 GitHub Issues 联系我们。

---

⭐ 如果这个项目对你有帮助，请给个 Star！
