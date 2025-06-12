# 🎯 **FFmpeg — Powerful Multimedia Toolkit**  

**FFmpeg** is a leading command-line tool for processing video, audio, and other multimedia files. It supports conversion, streaming, editing, and playback across countless formats.  

---

## ✅ Features  
- Convert between **any** video/audio format (MP4, MKV, MP3, AAC, etc.)  
- Extract audio, merge streams, or remux containers  
- Trim, crop, resize, adjust speed, and apply filters  
- Capture live streams (RTMP, HLS, etc.) and screen recordings  
- Hardware acceleration (NVENC, QuickSync, VA-API)  
- Cross-platform (Linux, macOS, Windows) and open-source  

---

## 📦 Installation  

### Debian/Ubuntu  
```bash  
sudo apt install ffmpeg  
```  

### Arch Linux  
```bash  
sudo pacman -S ffmpeg  
```  

### macOS (Homebrew)  
```bash  
brew install ffmpeg  
```  

### Windows (Scoop)  
```bash  
scoop install ffmpeg  
```  

---

## � Basic Usage  

### Convert video to MP4  
```bash  
ffmpeg -i input.avi output.mp4  
```  

### Extract audio from video (MP3)  
```bash  
ffmpeg -i video.mp4 -q:a 0 -map a audio.mp3  
```  

---

## ⚙️ Options & Examples  

| Command/Flag            | Description                                  |  
|-------------------------|----------------------------------------------|  
| `-i input.mp4`          | Specify input file                           |  
| `-c:v libx264`          | Encode video as H.264                        |  
| `-c:a aac`              | Encode audio as AAC                          |  
| `-ss 00:01:30 -t 10`    | Trim from 1m30s for 10 seconds               |  
| `-vf "scale=1280:720"`  | Resize to 720p                               |  
| `-filter:a "atempo=1.5"`| Speed up audio by 1.5x                       |  

### Combine video and audio  
```bash  
ffmpeg -i video.mp4 -i audio.mp3 -c copy output.mkv  
```  

### Convert to GIF  
```bash  
ffmpeg -i clip.mp4 -vf "fps=10,scale=640:-1" animation.gif  
```  

---

## 🧩 Tips  
- Use `-preset ultrafast` for faster encoding (tradeoff: larger files)  
- Add `-crf 23` (18–28) to control H.264/265 quality (lower = better)  
- Extract frames: `ffmpeg -i video.mp4 frame_%04d.png`  
- Stream copy (`-c copy`) avoids re-encoding for speed  

---

## 📚 More Info  
- Docs: Run `ffmpeg -h full` or visit [FFmpeg Official](https://ffmpeg.org/documentation.html)  
- GitHub: [https://github.com/FFmpeg/FFmpeg](https://github.com/FFmpeg/FFmpeg)  
