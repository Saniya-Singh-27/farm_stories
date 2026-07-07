# Hero video

Drop your orchard drone clip here to get a **true autoplay cinematic hero**:

```
the-farm-stories/media/hero.mp4      (H.264 / MP4 — required)
the-farm-stories/media/hero.webm     (VP9 / WebM — optional, smaller)
```

The hero `<video>` in `index.html` already lists these as its first sources, so
as soon as `hero.mp4` exists it plays automatically (muted, looped, inline).

If neither file is present, the site falls back to a layered, animated
"Ken Burns" cinematic still (sunrise orchard with drifting mist, light rays and
floating particles) — so the hero always looks premium, with or without a video.

### Recommended clip
- 8–20 s, seamless loop, 1080p (or 1440p), **muted**
- Slow camera move through mature mango trees at sunrise; drifting mist / pollen
- Keep it under ~6–8 MB if possible (compress with HandBrake or `ffmpeg`)

```bash
# example compression
ffmpeg -i source.mov -vf "scale=1920:-2" -c:v libx264 -crf 24 -preset slow -an -movflags +faststart hero.mp4
```
