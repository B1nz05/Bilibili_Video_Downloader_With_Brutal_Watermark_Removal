。

🎬 Bilibili Auto Downloader & Cropper

A lightweight AI-assisted (Vibe Coding) Python script that automatically:

📥 Downloads videos from Bilibili

📦 Supports batch downloading

🎞 Merges video + audio using FFmpeg

✂️ Crops unwanted areas of the video automatically

🚫 Brutally removes Bilibili watermark (for 1920×1080 videos)

📂 Saves the final video directly to your Desktop

This tool is designed to automate repetitive workflows such as:

Video archiving

Content repurposing

Removing UI overlays or watermarks

Preparing clips for further editing

✨ Features
📥 Batch Download Support

You can download multiple Bilibili videos at once.

Simply add URLs into the list:

VIDEO_LIST = [
    "https://www.bilibili.com/video/BV1xxxxx",
    "https://www.bilibili.com/video/BV2xxxxx",
    "https://www.bilibili.com/video/BV3xxxxx"
]

The script will automatically:

Download each video

Merge video and audio

Crop the video

Save the final result

🚫 Brutal Watermark Removal (1920×1080)

Bilibili videos often contain UI overlays or watermarks near the top of the frame.

Instead of complex detection, this script uses a simple brute-force crop approach.

Example crop filter:

crop=1920:980:0:100

Meaning:

Parameter	Value	Description
Width	1920	Keep full width
Height	980	Remove top portion
X	0	Start from left
Y	100	Cut top 100px

Result:

✔ Removes Bilibili watermark / UI bar
✔ Keeps main video content

⚠️ This method assumes the video resolution is 1920×1080.

🛠 Requirements

Python 3.8+

Install dependency:

pip install yt-dlp

Install FFmpeg:

https://ffmpeg.org/download.html

⚙️ Configuration

Inside the script you can configure:

FFmpeg Path
FFMPEG_BIN_PATH

Example:

C:\Users\PC\Downloads\ffmpeg\bin
Output Directory
OUTPUT_DIR

Default:

Desktop/BilibiliDownloads
Video List

Add Bilibili URLs:

VIDEO_LIST = [
    "https://www.bilibili.com/video/BV1DxPPzdE9o"
]
Crop Filter
CROP_FILTER = 'crop=1920:980:0:100'

Format:

crop=width:height:x:y
🚀 Usage

Run the script:

python bilibili_downloader.py

Example output:

==================================================
Bilibili Auto Downloader & Cropper
==================================================

[1/3] Processing: https://www.bilibili.com/video/BVxxxx
Downloading video...
Merging video and audio...
Executing video cropping...

Cropping completed successfully!
📂 Output Structure
Desktop
 └── BilibiliDownloads
        ├── VideoTitle1.mp4
        ├── VideoTitle2.mp4
        ├── VideoTitle3.mp4

Each file is already:

✔ Downloaded
✔ Merged
✔ Cropped

⚠️ Limitations

Crop settings are optimized for 1920×1080 videos

Other resolutions may require adjusting CROP_FILTER

🧠 Built With

Python

yt-dlp

FFmpeg

Vibe Coding / AI-assisted development
