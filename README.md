# 🎬 Bilibili Auto Downloader & Cropper

一个轻量级的 Python 工具，利用 `yt-dlp` 和 `FFmpeg` 实现 Bilibili 视频的自动化下载、合并与后期裁剪。

该工具专为高效处理视频归档、内容二次剪辑及界面去水印而设计，通过“硬核”裁剪法，快速去除 Bilibili 视频中恼人的 UI 覆盖层。



---

## ✨ 核心功能
* **📥 批量下载**：支持同时处理多个 Bilibili 链接。
* **📦 自动合并**：自动调用 FFmpeg 将分离的音视频流合并为高质量 MP4。
* **✂️ 自动裁剪**：内置裁剪引擎，自动去除视频边缘或 UI 水印。
* **🚫 暴力去水印**：针对 1920×1080 分辨率视频，直接通过裁剪移除顶部 UI 栏。
* **📂 一键归档**：处理完毕后的视频自动保存至桌面指定目录。

---

## 🛠 前置要求
* **Python 3.8+**
* **FFmpeg**：确保已安装并配置至系统环境变量（[点击下载 FFmpeg](https://ffmpeg.org/download.html)）。
* **安装依赖库**：
  ```bash
  pip install yt-dlp
