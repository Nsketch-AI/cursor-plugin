---
name: nsketch-generate-video
description: >
  Generate videos with Nsketch AI. Use when the user wants a video clip from a
  prompt or wants to animate an existing image (image-to-video).
---

Use the Nsketch MCP `generate_video` tool. For local file references, upload via `upload_media` first. Videos take minutes — poll `get_generation_status` (type "video", pass the returned model and endpoint) until complete and present the result URL.

Examples:
- "a 5 second clip of waves crashing at sunset" → `generate_video` with the prompt
- "animate hero.png with a slow zoom" → `upload_media`, then `generate_video` with `image_url`
