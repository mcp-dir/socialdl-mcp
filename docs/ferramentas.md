# Ferramentas

Social → Context expõe 3 ferramentas (todas somente leitura).

### 1. `socialdl_extract`
**Input**: `url`, `transcribe` (opcional), `describe_images` (opcional), `language` (opcional)

Download a social-media link (TikTok, Instagram reel/post/carousel, YouTube, or any direct .mp4) and return it as usable text context: metadata (author, caption, duration), the audio/video transcript, and a vision description (OCR + summary) of each image in a carousel/post. YouTube uses its existing captions when available. Use this to give Claude the content of a video or post the user pasted.

### 2. `socialdl_metadata`
**Input**: `url`

Lightweight lookup: resolve a social-media link to its metadata (author, caption, duration, counts) and media URLs WITHOUT transcribing or running vision. Cheaper than socialdl_extract — use when the caption/context alone is enough.

### 3. `socialdl_download`
**Input**: `url`

Resolve a TikTok / Instagram / YouTube link (or direct .mp4/image URL) to its DIRECT download URLs from the source CDN — every video quality, audio track and image, with quality labels. Use when the user wants to DOWNLOAD/save the media instead of transcribing it. No transcription/vision.

## Prompts de exemplo

```
Transcreva este reel: https://www.instagram.com/reel/...
Resuma o que esse vídeo do TikTok fala: <link>
Pegue a legenda e a transcrição deste vídeo do YouTube: <link>
```
