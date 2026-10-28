# Parallax Studio

Turn any photo into a moving 3D **parallax video** (MP4, 1080p or 4K), right in your web browser.

**Try it:** https://parallaxstudio1.netlify.app/

Nothing to install. Your photos never leave your computer: everything, including the AI, runs in the browser.

## What it does

- **Select the subject** that should stand out from the background:
  - ✨ **Auto-detect** finds the main subject with AI.
  - 🎯 **Object tool**: hover over anything to see the object the AI recognises, click to add it, Alt/⌥-click to remove it, or drag a box to take everything inside it.
  - Brush, lasso, magic wand and a hair/edge brush for fine detail, with Add/Subtract, undo and edge refinement.
  - Optional **Middle** depth layer for a deeper 3D look.
- **Preview live** while you adjust: camera movement (push in, side to side, orbit…, one way or back and forth), length, parallax amount, background blur.
- **Light & lens**: focus pull (depth of field), vignette, light leak.
- **Any picture shape**: the video takes the photo's own shape, or 16:9, 9:16 (Reels/TikTok), square, 4:5.
- **Batch**: load many photos, the AI selects each one, you check and approve them, then render one long video (with fades) or a separate video per photo (save all as a .zip).

## Running it

Open `index.html` in Chrome, Edge or Safari (17 or newer), or use the link above. An internet connection is needed the first time, to download the AI models (they are then kept by the browser).

The whole app is this one file. To host your own copy, put `index.html` on any static web host (Netlify, GitHub Pages…).

## Built with

- [Transformers.js](https://github.com/huggingface/transformers.js) (Apache 2.0) to run the AI models in the browser
- [RMBG-1.4](https://huggingface.co/briaai/RMBG-1.4) by BRIA AI for auto-detect: free for **non-commercial** use under the [BRIA model license](https://bria.ai/bria-huggingface-model-license-agreement/); commercial use needs a licence from BRIA
- [Segment Anything (SAM)](https://huggingface.co/Xenova/sam-vit-base) by Meta AI (Apache 2.0) for the object tool
- [mp4-muxer](https://github.com/Vanilagy/mp4-muxer) (MIT) and the browser's WebCodecs video encoder to write the MP4
