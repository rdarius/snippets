# FFMPEG

## Convert gif to image sequence

```bash
ffmpeg -i target.gif ./target_frames/frame_%d.png
```

## Convert video

```bash
ffmpeg -i input.mp4 output.mp4
```

## Extract Audio from Video

```bash
ffmpeg -i input.mp4 output.mp3
```

## Convert Video using CUDA

```bash
ffmpeg -y -vsync 0 -hwaccel cuda -hwaccel_output_format cuda -i input.mp4 -c copy output.mp4
```
