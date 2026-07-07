# Nsketch AI — Cursor Plugin

Generate images, videos, voice, and more with [Nsketch AI](https://nsketch.ai) directly from Cursor, via the Nsketch MCP server.

## Install

Add the Nsketch MCP server to Cursor (`mcp.json`):

```json
{
  "mcpServers": {
    "nsketch": {
      "type": "http",
      "url": "https://mcp.nsketch.ai/mcp"
    }
  }
}
```

On first use, Cursor prompts you to sign in with your Nsketch account — that's it.

## Usage

Use the `/nsketch` command or just ask:

> "Generate an image of a neon-lit ramen shop, 16:9"
> "Turn this image into a 5-second cinematic clip"

Tools available: `generate_image`, `generate_video`, `generate_voice`, `clone_voice`, `lipsync`, `motion_transfer`, `reshoot`, `upscale_image`, `remove_background`, `upload_media`, `get_generation_status`, `list_models`, `get_credits`.

## Using Claude Code, Codex, or a terminal agent?

The [Nsketch CLI](https://github.com/Nsketch-AI/cli) + [skills](https://github.com/Nsketch-AI/skills) are a better fit:

```bash
npm install -g @nsketch/cli && nsketch auth login
npx skills add Nsketch-AI/skills
```
