# Awesome MiniMax Hailuo H3 API ⚡ — Prompts, Variants & One-Call Video Generation

> The most complete open guide to **MiniMax Hailuo H3 — the fast, high-motion AI video model (text / image / reference to video, open weights and official tiers)** — a community prompt library and a single API to run every variant.

<p align="center">
  <a href="https://wavespeed.ai/minimax-h3-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api"><img src="https://img.shields.io/badge/▶_Run_MiniMax_H3-Get_API_Key-00E5FF?style=for-the-badge&labelColor=0B0B0F" alt="Run MiniMax H3"></a>
</p>

<p align="center">
  <b>🌊 Powered by <a href="https://wavespeed.ai?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api">WaveSpeedAI</a> — serverless MiniMax Hailuo H3 API, pay-as-you-go, zero cold starts.</b><br>
  <a href="https://wavespeed.ai/minimax-h3-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api"><b>→ Get a MiniMax H3 API key</b></a>
</p>

<p align="center">
  🖥️ <b>No code?</b> Generate in your browser (no setup, free to start) → <a href="https://wavespeed.ai/video-generator?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api"><b>WaveSpeedAI Video Generator</b></a>
</p>

---

> **Generate right now**
> ```bash
> npm i -g @wavespeed/cli && wavespeed login
> wavespeed run wavespeed-ai/minimax-h3/text-to-video -p "your prompt"
> ```
> No GPU, no cold start — the same endpoint powers every prompt below.

---

## 📖 Contents
1. [What is MiniMax Hailuo H3?](#what-is-minimax-hailuo-h3)
2. [Run it via API](#run-it-via-api)
3. [Model Variants](#model-variants)
4. [Prompt Library](#prompt-library) — 10 community prompts
5. [Related Model Guides](#related-model-guides)
6. [Contributing](#contributing)

---

## What is MiniMax Hailuo H3?

**MiniMax Hailuo H3** is MiniMax's fast, high-motion AI video model, strong on dynamic action and character consistency. WaveSpeedAI serves the open-weights **MiniMax H3** (text, image and reference to video with native stereo audio, video edit, video extend, ControlNet, custom LoRA, plus image generation and editing) and the official MiniMax H3, H3 Lite, H3 Highspeed and H3 Image endpoints.

---

## Run it via API

One endpoint, submit + poll. Swap the model path for any variant below.

```bash
curl -s -X POST "https://api.wavespeed.ai/api/v3/wavespeed-ai/minimax-h3/text-to-video" \
  -H "Authorization: Bearer $WAVESPEED_API_KEY" -H "Content-Type: application/json" \
  -d '{"prompt": "A parkour runner leaping between rooftops at sunset, dynamic camera, 8k", "aspect_ratio": "16:9"}'
# → {"data": {"id": "<prediction_id>"}}

curl -s "https://api.wavespeed.ai/api/v3/predictions/<prediction_id>/result" \
  -H "Authorization: Bearer $WAVESPEED_API_KEY"
# → status: completed → outputs: ["<url>"]
```

**[→ Get your MiniMax H3 API key](https://wavespeed.ai/minimax-h3-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api)** · pay-as-you-go, live pricing on each model page.

**Python wrapper:** [minimax-h3-api](https://github.com/WaveSpeedAI/minimax-h3-api) — one typed function per MiniMax H3 endpoint, built on the official SDK.

---

## Model Variants

All variants open in-browser with a copy-paste API snippet.

### MiniMax H3 (open weights) — recommended &nbsp;[▶ API](https://wavespeed.ai/minimax-h3-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api)
[text-to-video](https://wavespeed.ai/models/wavespeed-ai/minimax-h3/text-to-video?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api) · [image-to-video](https://wavespeed.ai/models/wavespeed-ai/minimax-h3/image-to-video?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api) · [reference-to-video](https://wavespeed.ai/models/wavespeed-ai/minimax-h3/reference-to-video?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api) · [video-edit](https://wavespeed.ai/models/wavespeed-ai/minimax-h3/video-edit?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api) · [video-extend](https://wavespeed.ai/models/wavespeed-ai/minimax-h3/video-extend?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api) · [controlnet](https://wavespeed.ai/models/wavespeed-ai/minimax-h3/controlnet-union?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api) · [text-to-image](https://wavespeed.ai/models/wavespeed-ai/minimax-h3/text-to-image?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api) · [image-edit](https://wavespeed.ai/models/wavespeed-ai/minimax-h3/image-edit?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api)

### Official MiniMax H3 &nbsp;[▶ API](https://wavespeed.ai/minimax-h3-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api)
[text-to-video](https://wavespeed.ai/models/minimax/h3/text-to-video?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api) · [image-to-video](https://wavespeed.ai/models/minimax/h3/image-to-video?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api) · [reference-to-video](https://wavespeed.ai/models/minimax/h3/reference-to-video?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api)

### H3 Lite / Highspeed / Image
[lite t2v](https://wavespeed.ai/models/minimax/h3-lite/text-to-video?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api) · [lite i2v](https://wavespeed.ai/models/minimax/h3-lite/image-to-video?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api) · [highspeed t2v](https://wavespeed.ai/models/minimax/h3-highspeed/text-to-video?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api) · [highspeed i2v](https://wavespeed.ai/models/minimax/h3-highspeed/image-to-video?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api) · [image t2i](https://wavespeed.ai/models/minimax/h3-image/text-to-image?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api) · [image edit](https://wavespeed.ai/models/minimax/h3-image/edit?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api)

> Full catalog: **[wavespeed.ai/minimax-h3-api](https://wavespeed.ai/minimax-h3-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api)**

---

## Prompt Library

10 prompts curated from the MiniMax Hailuo H3 creator community. Credit stays with the original author. Fill in `{...}` placeholders.

### 1. Medium shot, vertical format, handheld camera…
*by [@IamEmily2050](https://x.com/IamEmily2050)*

```
{
  "shot": {
    "composition": "Medium shot, vertical format, handheld camera",
    "camera_motion": "slight natural shake",
    "frame_rate": "30fps",
    "film_grain": "none"
  },
  "subject": {
    "description": "A towering, snow-white Yeti with shaggy fur and expressive blue eyes",
    "wardrobe": "slightly oversized white T-shirt with the name 'Emily' in bold, blood-red letters across the chest"
  },
  "scene": {
    "location": "lush forest clearing",
    "time_of_day": "daytime",
    "environment": "sunlight filtering through the canopy, creating dappled light patterns on the forest floor"
  },
  "visual_details": {
    "action": "Yeti holds a smartphone on a selfie stick, speaking excitedly to the camera before letting out a dramatic scream",
    "props": "smartphone mounted on a selfie stick"
  },
  "cinematography": {
    "lighting": "natural sunlight with soft shadows",
    "tone": "lighthearted and humorous"
  },
  "audio": {
    "ambient": "rustling leaves, distant bird calls",
    "dialogue": {
      "character": "Yeti",
      "line": "Veo3 Fast is now available in the Gemini app—three videos per day! People are going to prompt me like crazy!",
      "subtitles": false
    },
    "effects": "sudden loud scream, flapping wings of startled birds"
  },
  "color_palette": "naturalistic with earthy greens and browns; bold red lettering on shirt provides contrast"
}
```

### 2. A dynamic camera glides through a miniature LEGO world, …
*by [@ZHO_ZHO_ZHO](https://x.com/ZHO_ZHO_ZHO)*

```
A dynamic camera glides through a miniature LEGO world, where an epic adventure unfolds. All sound effects—footsteps, explosions, cars, dragons—are created using mouth sounds by a single AI-generated voice artist. As each sound is made, the visuals instantly respond: LEGO characters jump into action, cars race, spaceships take off, volcanoes erupt. The journey moves through LEGO-built environments—city streets, underwater ruins, space stations, and lava lairs. The video is fast-paced, playful, and visually rich, like a blend between The LEGO Movie and next-gen AI storytelling. The sound-to-visual sync creates a magical, toy-driven universe where imagination controls reality.
```

### 3. Front-facing static shot, A woman enthusiastically bites…
*by [@azed_ai](https://x.com/azed_ai)*

```
Front-facing static shot, A woman enthusiastically bites into a hyper-realistic glass fried chicken leg. As it cracks delicately in her mouth, she smiles and says,  "Zero calories, zero cruelty, 100% crunch.... vegan life, baby!" Subtle ASMR crunching sounds. soft lighting, mukbang video style, playful and bizarre tone.
```

### 4. Static shot, A man delicately slices a hyper-realistic g…
*by [@azed_ai](https://x.com/azed_ai)*

```
Static shot, A man delicately slices a hyper-realistic glass dragon fruit on a pristine cutting board. The whisper-thin blade glides through the transparent fruit, scattering soft-glimmering shards. Surgical, serene lighting. Hyper-clean, ASMR video
```

### 5. Top-down static shot, A thick slice of marbled steak siz…
*by [@azed_ai](https://x.com/azed_ai)*

```
Top-down static shot, A thick slice of marbled steak sizzles on a hot black pan, juices bubbling as the surface caramelizes. Steam rises in soft curls, catching warm, directional kitchen light. Rich textures and ASMR sounds evoke savory satisfaction. Hyper-real, food-commercial style.
```

### 6. Close-up static shot: a hand slowly squeezing a glossy pink jelly donut
*by [@azed_ai](https://x.com/azed_ai)*

```
Close-up static shot: a hand slowly squeezes a shiny, pink jelly donut on a clean surface. The soft, gelatinous texture deforms and oozes between the fingers, glistening under soft ambient light. Vivid colors ripple through the translucent jelly. Playful, ASMR, deeply satisfying.
```

### 7. Front static shot, A man casually eats molten lava from …
*by [@azed_ai](https://x.com/azed_ai)*

```
Front static shot, A man casually eats molten lava from a bowl with a metal spoon. Each scoop sizzles and pops, the bowl glowing with heat. He slurps it like soup, unfazed, as lava crackles beneath. Dramatic lighting, surreal textures, playful and absurd tone, ASMR
```

### 8. A dynamic tracking shot, a rooster launches off a gymnas…
*by [@azed_ai](https://x.com/azed_ai)*

```
A dynamic tracking shot, a rooster launches off a gymnastics vault, flipping mid-air with feathers flying in slow motion. It sticks the landing perfectly, wings spread in a proud pose. Judges flash “10.0” scorecards. Bright stadium lights, roaring crowd. Playful, surreal Olympic parody.
```

### 9. Front static shot, a woman hosts a podcast at a desk, sp…
*by [@azed_ai](https://x.com/azed_ai)*

```
Front static shot, a woman hosts a podcast at a desk, speaking softly into a mic with low tones, whispering. Wearing headphones, she grins and says: “Confidence? Oh, honey, I don’t walk into a room—I glide in like I own the Wi-Fi.” Soft studio lighting, cozy, playful, and empowering podcast energy. podcast vibe. no subtitle
```

### 10. Static shot: A chef delicately slices a hyper-realistic …
*by [@azed_ai](https://x.com/azed_ai)*

```
Static shot: A chef delicately slices a hyper-realistic kiwi on a spotless cutting board. The green flesh and glistening black seeds fracture cleanly under a whisper-thin blade. Each slice emits a soft, crystalline shimmer, ASMR. The atmosphere is surgical, serene, and visually pristine.
```

*Add yours via a PR — keep the original author's credit. See [Contributing](#contributing).*

---

## Related Model Guides
Part of the WaveSpeedAI **Awesome Model** series — one guide per frontier model, all runnable through one API:

- 🎬 [awesome-seedance-api](https://github.com/WaveSpeedAI/awesome-seedance-api) — ByteDance Seedance video
- 🌊 [awesome-wan-api](https://github.com/WaveSpeedAI/awesome-wan-api) — Alibaba Wan video
- ⚡ [awesome-minimax-h3-api](https://github.com/WaveSpeedAI/awesome-minimax-h3-api) — MiniMax Hailuo H3 video *(this repo)*
- 🎞️ [awesome-kling-api](https://github.com/WaveSpeedAI/awesome-kling-api) — Kling video
- 🖼️ [awesome-seedream-api](https://github.com/WaveSpeedAI/awesome-seedream-api) — ByteDance Seedream image
- 🎨 [awesome-gpt-image-api](https://github.com/WaveSpeedAI/awesome-gpt-image-api) — OpenAI GPT Image
- 🍌 [awesome-nano-banana-api](https://github.com/WaveSpeedAI/awesome-nano-banana-api) — Google Nano Banana image

---

## Contributing
PRs welcome:
1. Reusable prompts (`{placeholders}` for swappable parts).
2. **Credit the original author** with a link.
3. No output images unless you own and can license them.

## License
[CC0-1.0](LICENSE) — text & prompts are free to use. Model outputs follow the model provider's and [WaveSpeed](https://wavespeed.ai)'s terms.

---
<p align="center"><sub>Maintained by <a href="https://wavespeed.ai?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api">WaveSpeedAI</a> — the fastest way to run frontier image & video models via one API. <a href="https://wavespeed.ai/minimax-h3-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-minimax-h3-api"><b>Run MiniMax Hailuo H3 →</b></a></sub></p>
