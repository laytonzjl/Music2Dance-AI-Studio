<div align="center">

# Music2Dance AI Studio

**基于生成式 AI 的音频驱动 3D 人体动作生成系统**

[![Windows](https://img.shields.io/badge/Platform-Windows-0078D4?logo=windows)](https://github.com)
[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC_BY--NC_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)
[![Python](https://img.shields.io/badge/Python-3.9+-3776AB?logo=python)](https://www.python.org/)

---

*“把汗水变成珍珠，把梦想变成实际。”*

</div>

## 💡 项目简介
**M2D AI Studio** 是一款面向游戏开发与动画制作的简易音乐到人体舞蹈动作生成的工具。输入音乐，该软件就能生成对应的3D人体舞蹈动作（BVH 格式）。

![软件主界面](menu.PNG)

## 🛠 功能亮点
- **依赖**：内置高效 ONNX 运行时环境，CPU 环境下即可完成推理。
- **采样**：集成高阶求解器，支持 1-3 阶自适应调节，平衡生成速度与平滑度。
- **对齐**：可以选定身体或者手部动作，选定输出帧数，直接输出可用的BVH动作资产。

## 🚀 快速开始
1. **下载安装**：前往 [Releases](https://github.com/laytonzjl/Music2Dance-AI-Studio/releases/tag/v1.0.0-alpha) 页面下载最新安装包 `M2D舞蹈生成_Setup.exe`。
2. **加载音频**：支持 `wav`, `mp3`, `flac` 等主流格式。
3. **参数配置**：根据目标引擎（UE5/Unity/Blender）选择帧率，推荐使用默认采样参数以获得最佳平衡。
4. **一键导出**：点击开始生成，自动导出 `.bvh` 文件。

## ⚠️ 版权与免责声明
- **协议说明**：本项目仅供**学术研究与个人学习使用**，严禁用于任何商业营利场景。
- **合规声明**：本软件生成的动作资产若用于公开展示，请在显著位置标注本项目出处。

## 🙏 致谢
本项目的核心算法与工程架构受以下先进工作的启发与支持：
- **数据集**：[FineDance](https://github.com/Finedance-dataset)
- **核心算法**：[EDGE](https://github.com/chahuja/EDGE), [DDPM](https://github.com/hojonathanho/diffusion), [IDDPM](https://github.com/openai/improved-diffusion), [DPM-Solver](https://github.com/LuChengTHU/dpm-solver)

---
<div align="center">
</div>
