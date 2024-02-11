- pip install pydub

# Lỗi RuntimeWarning: Couldn't find ffmpeg or avconv - defaulting to ffmpeg, but may not work
- fix :
1. Download ffmpeg file into your computer and install it.
2. Pass the system path of the ffmpeg file location : C:\ffmpeg\bin

```
AudioSegment.converter = "C:\\ffmpeg\\bin\\ffmpeg.exe"
AudioSegment.ffmpeg = "C:\\ffmpeg\\bin\\ffmpeg.exe"
AudioSegment.ffprobe ="C:\\ffmpeg\\bin\\ffprobe.exe"

```
- then restart computer.
