<div align="center">

# Music2Dance AI Studio

**基于生成式 AI 的音频驱动 3D 人体动作生成系统**

[![Windows](https://img.shields.io/badge/Platform-Windows-0078D4?logo=windows)](https://github.com)
[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC_BY--NC_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)
[![Python](https://img.shields.io/badge/Python-3.9+-3776AB?logo=python)](https://www.python.org/)

*“把汗水变成珍珠，把梦想变成实际。”*

---

![软件主界面](menu.PNG)

</div>

## 📖 项目概述
**M2D AI Studio** 是一个专为游戏开发人员、动画师及 3D 内容创作者打造的端侧多模态舞蹈动作生成系统。该系统通过深度分析输入的音频流，提取音频特征，并利用扩散模型（Diffusion Model）进行高效的动作序列生成，实现从音乐到 BVH 动作资产的一键式转换。

## ⚙️ 技术特性
* **CPU推理**：基于 `ONNX Runtime` 部署的推理引擎，无需 GPU 加速即可在普通桌面 CPU 上实现高效实时推理。
* **帧数选择**：支持 30FPS/60FPS 动作输出，兼容主流 3D 引擎。

## 🛠 功能参数详解
| 参数名称 | 建议设置 | 说明 |
| :--- | :--- | :--- |
| **推理步数** | 15 - 30 | 值越高动作细节越丰富，但生成时间随之增加。 |
| **求解器阶数** | 3 | 阶数越高，扩散迭代过程越平滑，平衡计算效率的首选。 |
| **手部动作** | 开启 | 包含手部关节数据，适用于精细的艺术动画需求。 |
| **输出帧率** | 60 | 推荐 60FPS 以保证在 UE5 或 Unity 中的动画线性平滑。 |

## 🚀 快速上手说明
1. **获取应用**：访问 [Releases 页面](https://github.com/laytonzjl/Music2Dance-AI-Studio/releases/tag/v1.0.0-alpha) 下载最新的安装程序。
2. **环境准备**：软件已完成自动化封装，无需预先安装 Python 或 CUDA，直接运行即可。
3. **音频预处理**：尽量选择音质清晰、节拍明显的音频片段。若音频过长，请使用窗口裁剪功能限定 20 秒内的生成范围。
4. **导出规范**：生成的 BVH 文件支持直接拖拽至 Blender 动作库，执行重定向（Retargeting）操作即可应用到角色模型。

## ❓ 常见问题排查 (FAQ)
* **Q: 为什么生成的动作在某些角色上看起来有“漂移”？**
  * A: 动作漂移通常源于根骨骼（Root/Pelvis）的偏移。请在动作重定向时，检查并固定根骨骼的高度偏移量。
* **Q: 程序运行时占用内存较高？**
  * A: 动作解算过程中会加载完整的模型权重与 3D 几何拓扑矩阵，建议预留 4GB 以上的系统空闲内存。
* **Q: 是否支持批量处理？**
  * A: 本版本为单次推理模式，批量自动化功能将在后续迭代中更新。

## 🙏 鸣谢与资源声明
本项目引用并受益于以下优秀开源工作：
* **核心数据集**：[FineDance](https://github.com/Finedance-dataset) 提供的舞蹈动作基准。
* **算法参考**：[EDGE](https://github.com/chahuja/EDGE), [DDPM](https://github.com/hojonathanho/diffusion), [IDDPM](https://github.com/openai/improved-diffusion), [DPM-Solver](https://github.com/LuChengTHU/dpm-solver)

## ⚠️ 版权警示
本项目仅限用于**非营利性的科研测试与学习交流**，严禁未经许可将本工具用于任何商业产品的开发或营利性行为。
---
<div align="center">
</div>
