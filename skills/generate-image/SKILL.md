---
name: nsketch-generate-image
description: >
  Generate or edit images with Nsketch AI. Use when the user wants to create an
  image, render, product shot, illustration, or edit an existing image.
---

Use the Nsketch MCP `generate_image` tool. For local file references, upload via `upload_media` first. Poll `get_generation_status` (type "image") until complete and present the result URL.

Examples:
- "generate an image of a mountain cabin at dusk" → `generate_image` with the prompt
- "make the sky in photo.png stormy" → `upload_media`, then `generate_image` with an edit model and `image_urls`
