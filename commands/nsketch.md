# /nsketch — route a request to Nsketch MCP tools

Interpret the user's request after `/nsketch` and call the matching Nsketch MCP tool:

- **Images** → `generate_image` (prompt, optional model / aspect_ratio / image_urls for edits)
- **Videos** → `generate_video` (prompt, optional image_url for image-to-video)
- **Speech / narration** → `generate_voice`; voice cloning → `clone_voice`
- **Lipsync / talking photo** → `lipsync`
- **Motion transfer** → `motion_transfer`; place character into a scene → `reshoot`
- **Upscale / enhance** → `upscale_image`; background removal → `remove_background`
- **Local files** → upload with `upload_media` first, then pass the returned URL
- **Account** → `get_credits`; catalog → `list_models`

Async jobs return a `request_id` — poll `get_generation_status` until it's no longer processing, then present the result URL(s).

Examples:
- `/nsketch a neon-lit ramen shop, 16:9` → `generate_image`
- `/nsketch turn hero.png into a 5s cinematic clip` → `upload_media` + `generate_video`
- `/nsketch how many credits do I have?` → `get_credits`
