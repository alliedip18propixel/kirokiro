# Private AI motion video

A single-file animated explainer (about 76 seconds) of the setup: Ollama with `qwen3.5:9b` on a MacBook Air, Tailscale between devices, and the Enchanted app on iPhone. No dependencies, no network needed.

## Open it

On a Mac, from the project folder:

```
open video/index.html
```

Or serve it locally:

```
cd video
python3 -m http.server 8000
```

then visit http://localhost:8000 in Safari or Chrome.

Click the video or press **Space** to play and pause. Use the slider to scrub, **Restart** to start over, and the left and right arrow keys to jump 5 seconds. The stage scales to the window; use full screen (green button or Ctrl+Cmd+F) for best results.

## Record it as an mp4

1. Open the page and make the window large or full screen. Pause at the start.
2. Press **Cmd+Shift+5** and choose "Record Selected Portion" (or "Record Entire Screen").
3. Click Record, then press Space to start playback.
4. When it ends (about 1 minute 16 seconds), click the stop button in the menu bar.

The recording is saved as a `.mov` on your Desktop. QuickTime Player can export it: File, Export As. To get mp4 with ffmpeg: `ffmpeg -i recording.mov -c:v libx264 -pix_fmt yuv420p out.mp4`.
