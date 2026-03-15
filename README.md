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

##⚙️ Configuration
Modify the parameters within the script to customize your workflow:
  
 Parameter,Description,Example
FFMPEG_BIN_PATH,Full path to your FFmpeg bin folder,C:\Users\PC\Downloads\ffmpeg\bin
OUTPUT_DIR,Directory where finished files are saved,Desktop/BilibiliDownloads
VIDEO_LIST,A list of Bilibili BV URL strings,"[""https://www.bilibili.com/video/BV1...""]"
CROP_FILTER,The FFmpeg crop filter string,'crop=1920:980:0:100'
