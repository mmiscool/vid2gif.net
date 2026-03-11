# vid2gif.net

Browser-based video-to-GIF conversion with no external runtime dependencies.

Repo: https://github.com/mmiscool/vid2gif.net

## What It Does

- Loads a local video file directly in the browser
- Lets you choose start and end time plus frame rate
- Preserves aspect ratio while resizing the GIF output
- Offers scale presets with visible output dimensions
- Generates an animated GIF locally in the page
- Exports a downloadable `.gif` without sending media to a server

## How To Use

1. Open `index.html` in a modern browser.
2. Choose a local video file.
3. Adjust the frame rate and time range.
4. Pick an output size:
   - Use the width and height fields directly
   - Keep `Lock aspect ratio` enabled to resize proportionally
   - Use the quick size presets to scale down faster
5. Click `Generate GIF`.
6. Preview the result and download it.

## Notes

- Everything runs client-side.
- Larger dimensions, longer clips, and higher frame rates will produce larger files and take longer to encode.
- GIF is limited to 256 colors, so some color loss is expected. This project uses an adaptive palette to improve quality compared with a fixed reduced palette.

## Local Development

This project is a single-page app. No build step is required.

To serve it locally:

```bash
python3 -m http.server 4173
```

Then open:

```text
http://127.0.0.1:4173/
```

## Files

- `index.html`: UI, GIF encoder, quantization, and page logic
- `README.md`: project overview and usage
