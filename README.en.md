# Social → Context

### Turn social-media videos and posts into text for Claude, Cursor and AI agents

Paste a social-media link (TikTok, Instagram reel/post/carousel, YouTube or any .mp4) and get its content as text: metadata, an audio/video transcript and a vision description (OCR and summary) of the images. Gives your AI context about what is inside a video or post.

- 🎬 **Video and posts become text**: audio transcript + image OCR and summary
- 🔗 **TikTok, Instagram (reel/post/carousel), YouTube** or any .mp4
- 🧠 **Context for your agent**: your AI understands what is inside the link
- 🪶 **Lightweight metadata** (author, caption, duration) without pulling the whole video
- 🔒 **Read-only** · 🎁 **3 free calls**
- 💬 **Works with any MCP client**: Claude Desktop, Cursor, VS Code, Cline, Continue

[Portuguese version](README.md) · [Full docs (PT-BR)](docs/)

---

## One-click install

### Claude (Web and Desktop)

[➕ Open in Claude and connect](https://claude.ai/customize/connectors?modal=add-custom-connector&mcpName=Social%20%E2%86%92%20Context&mcpServerUrl=https%3A%2F%2Fapi.mcp.ai%2Fp_socialdl)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors) → **+** → **Add custom connector** → name `Social → Context`, URL `https://api.mcp.ai/p_socialdl`.

### Cursor

[➕ Install in Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=socialdl&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9zb2NpYWxkbCJ9)

### VS Code (Copilot Chat)

[➕ Install in VS Code](vscode:mcp/install?name=socialdl&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_socialdl%22%7D)

### Any other MCP-over-HTTP client

```
https://api.mcp.ai/p_socialdl
```

---

## 3 tools

| Tool | Description |
|---|---|
| `socialdl_extract` | Download a social-media link (TikTok, Instagram reel/post/carousel, YouTube, or any direct .mp4) and return it as usable text context: metadata (author, caption, duration), the audio/video transcript, and a vision description (OCR + summary) of each image in a carousel/post. YouTube uses its existing captions when available. Use this to give Claude the content of a video or post the user pasted. |
| `socialdl_metadata` | Lightweight lookup: resolve a social-media link to its metadata (author, caption, duration, counts) and media URLs WITHOUT transcribing or running vision. Cheaper than socialdl_extract — use when the caption/context alone is enough. |
| `socialdl_download` | Resolve a TikTok / Instagram / YouTube link (or direct .mp4/image URL) to its DIRECT download URLs from the source CDN — every video quality, audio track and image, with quality labels. Use when the user wants to DOWNLOAD/save the media instead of transcribing it. No transcription/vision. |

---

## Pricing

See [docs/precos.md](docs/precos.md) (PT-BR).

---

## License

MIT — see [LICENSE](LICENSE). The MCP server at `api.mcp.ai/p_socialdl` is proprietary (hosted); this repo (manifests, docs, skills) is MIT.
