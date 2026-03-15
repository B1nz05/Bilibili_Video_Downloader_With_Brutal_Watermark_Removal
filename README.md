🎬 Bilibili Auto Downloader & Cropper一个轻量级的 Python 工具，利用 yt-dlp 和 FFmpeg 实现 Bilibili 视频的自动化下载、合并与后期裁剪。该工具专为高效处理视频归档、内容二次剪辑及界面去水印而设计，通过“硬核”裁剪法，快速去除 Bilibili 视频中恼人的 UI 覆盖层。✨ 核心功能📥 批量下载：支持同时处理多个 Bilibili 链接。📦 自动合并：自动调用 FFmpeg 将分离的音视频流合并为高质量 MP4。✂️ 自动裁剪：内置裁剪引擎，自动去除视频边缘或 UI 水印。🚫 暴力去水印：针对 1920×1080 分辨率视频，直接通过裁剪移除顶部 UI 栏。📂 一键归档：处理完毕后的视频自动保存至桌面指定目录。🛠 前置要求Python 3.8+FFmpeg：确保已安装并配置至系统环境变量（点击下载 FFmpeg）。安装依赖库：Bashpip install yt-dlp
⚙️ 配置指南在脚本中修改以下参数以符合你的需求：参数描述示例FFMPEG_BIN_PATHFFmpeg 可执行文件路径C:\ffmpeg\binOUTPUT_DIR最终视频保存路径Desktop/BilibiliDownloadsVIDEO_LIST需要下载的 BV 链接列表["https://www.bilibili.com/video/BV1..."]CROP_FILTER裁剪参数'crop=1920:980:0:100'裁剪原理解析默认配置采用 crop=1920:980:0:100，即：Width (1920): 保持原始宽度。Height (980): 裁剪掉顶部 100px 后的剩余高度。X (0): 水平起始坐标。Y (100): 从顶部 100px 处开始裁剪。🚀 使用方法配置好 VIDEO_LIST。运行脚本：Bashpython bilibili_downloader.py
查看输出：Plaintext==================================================
Bilibili Auto Downloader & Cropper
==================================================
[1/3] Processing: https://www.bilibili.com/video/BVxxxx
Downloading video...
Merging video and audio...
Executing video cropping...
Cropping completed successfully!
⚠️ 注意事项分辨率限制：目前的裁剪方案是针对 1920×1080 视频优化的。如果你的视频源是其他分辨率（如 4K 或 720P），请务必调整 CROP_FILTER 参数，否则可能导致画面比例失调。合规提示：请确保下载和使用视频内容符合相关版权规定及 Bilibili 的使用协议，仅限个人学习和研究使用。🧠 技术栈Pythonyt-dlp (下载核心)FFmpeg (音视频处理)Vibe Coding / AI-Assisted
