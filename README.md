# 🎬 Bilibili Auto Downloader & Cropper

A lightweight Python script that uses `yt-dlp` and `FFmpeg` to automate the downloading, merging, and cropping of Bilibili videos. 

Designed for efficient video archiving, content repurposing, and removing UI overlays or watermarks, this tool uses a "brute-force" cropping approach to clean up your footage quickly.



---

## ✨ Features
* **📥 Batch Download Support**: Process multiple Bilibili URLs in one go.
* **📦 Automatic Merging**: Automatically merges audio and video streams using FFmpeg.
* **✂️ Intelligent Cropping**: Built-in engine to remove unwanted frames or watermarks.
* **🚫 Brutal Watermark Removal**: Specialized cropping for 1920×1080 videos to strip out top-frame UI elements.
* **📂 Seamless Archiving**: Automatically saves finalized videos to your local directory.

---

## 🛠 Requirements
* **Python 3.8+**
* **FFmpeg**: Must be installed and added to your system PATH ([Download FFmpeg](https://ffmpeg.org/download.html)).
* **Dependencies**:
  ```bash
  pip install yt-dlp

  ⚙️ ConfigurationModify the parameters in the script to match your environment:ParameterDescriptionExampleFFMPEG_BIN_PATHPath to FFmpeg executableC:\ffmpeg\binOUTPUT_DIRFinal save destinationDesktop/BilibiliDownloadsVIDEO_LISTList of BV URLs to process["https://www.bilibili.com/video/BV1..."]CROP_FILTERCropping filter string'crop=1920:980:0:100'Understanding the Crop FilterDefault config crop=1920:980:0:100 explained:Width (1920): Keeps original width.Height (980): The resulting height after removing 100px.X (0): Horizontal starting coordinate.Y (100): Vertical starting point (cuts the top 100px).🚀 UsageConfigure your VIDEO_LIST inside the script.Run the script:Bashpython bilibili_downloader.py
Example output:Plaintext==================================================
Bilibili Auto Downloader & Cropper
==================================================
[1/3] Processing: [https://www.bilibili.com/video/BVxxxx](https://www.bilibili.com/video/BVxxxx)
Downloading video...
Merging video and audio...
Executing video cropping...
Cropping completed successfully!
⚠️ Limitations & NotesResolution Dependency: The default crop settings are optimized for 1920×1080. If your source video has a different resolution (e.g., 4K or 720P), you must adjust the CROP_FILTER accordingly to avoid aspect ratio distortion.Compliance: Please ensure your use of downloaded content adheres to Bilibili's Terms of Service and applicable copyright laws. This tool is intended for personal archival and research purposes only.🧠 Built WithPythonyt-dlp (Download engine)FFmpeg (Video/Audio processing)Vibe Coding / AI-Assisted Development
