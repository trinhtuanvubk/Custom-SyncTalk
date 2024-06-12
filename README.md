# Introduction
- This repository is my customization of SyncTalk. It builds upon their work and incorportates additional features and modifications specific to this project.

# Notes
- The most important is "pre-preprocess" to make sure your video: 
    - all frames contains face
    - 25 fps
    - 512x512 resolution
    - stable head movements (dont move to much)
# Instalation
- Follow the original Readme.

# Pipeline

### Pre-preprocess

- Run pre-preprocess:
```
python3 data_utils/pre_preprocess.py --inp data/path/to/video.mp4 --cpu
```

- Then, follow the return ffmpeg command showed on terminal, for example:
```
ffmpeg -i ../data/path/to/video/mp4 -ss 0.0 -t 35.32 -filter:v "crop=208:208:145:14, scale=512:512" crop.mp4
```

### Preprocess:
