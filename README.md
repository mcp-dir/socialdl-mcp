# Social → Context

### Transforme vídeos e posts de redes sociais em texto para Claude, Cursor e agentes de IA

Cole um link de rede social (TikTok, Instagram reel/post/carrossel, YouTube ou um .mp4) e receba o conteúdo como texto: metadados, transcrição do áudio/vídeo e descrição (OCR e resumo) das imagens. Dá ao Claude o contexto do que está dentro do vídeo ou post.

- 🎬 **Vídeo e post viram texto**: transcrição do áudio + OCR e resumo das imagens
- 🔗 **TikTok, Instagram (reel/post/carrossel), YouTube** ou qualquer .mp4
- 🧠 **Contexto pro seu agente**: o Claude passa a entender o que está dentro do link
- 🪶 **Metadados leves** (autor, legenda, duração) sem baixar o vídeo inteiro
- 🔒 **Somente leitura** · 🎁 **3 chamadas grátis**
- 💬 **Funciona com qualquer cliente MCP**: Claude Desktop, Cursor, VS Code, Cline, Continue

[English version](README.en.md) · [Documentação completa](docs/) · [Skill pra agentes](skills/)

---

## Instalar em 1 clique

### Claude (Web e Desktop)

A Anthropic unificou a instalação de MCPs em `claude.ai/customize/connectors`. **O mesmo link serve pra Claude Web e Claude Desktop** (basta estar logado):

[➕ Abrir no Claude e conectar](https://claude.ai/customize/connectors?modal=add-custom-connector&mcpName=Social%20%E2%86%92%20Context&mcpServerUrl=https%3A%2F%2Fapi.mcp.ai%2Fp_socialdl)

**Manual** (se o deeplink não abrir): [claude.ai/customize/connectors](https://claude.ai/customize/connectors) → **+** → **Adicionar conector personalizado** → cole **Nome** `Social → Context` e **URL** `https://api.mcp.ai/p_socialdl`.

### Cursor

[➕ Instalar Social → Context no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=socialdl&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9zb2NpYWxkbCJ9)

### VS Code (Copilot Chat)

[➕ Instalar Social → Context no VS Code](vscode:mcp/install?name=socialdl&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_socialdl%22%7D)

### ChatGPT, Manus, OpenClaw e mais 40+ clientes

Funciona em qualquer cliente MCP que suporte **MCP over HTTP**. A URL do servidor é sempre:

```
https://api.mcp.ai/p_socialdl
```

Detalhes por cliente: [INSTALL.md](INSTALL.md).

---

## Exemplos de uso

```
Transcreva este reel: https://www.instagram.com/reel/...
Resuma o que esse vídeo do TikTok fala: <link>
Pegue a legenda e a transcrição deste vídeo do YouTube: <link>
```

---

## 3 ferramentas disponíveis

| Tool | Descrição |
|---|---|
| `socialdl_extract` | Download a social-media link (TikTok, Instagram reel/post/carousel, YouTube, or any direct .mp4) and return it as usable text context: metadata (author, caption, duration), the audio/video transcript, and a vision description (OCR + summary) of each image in a carousel/post. YouTube uses its existing captions when available. Use this to give Claude the content of a video or post the user pasted. |
| `socialdl_metadata` | Lightweight lookup: resolve a social-media link to its metadata (author, caption, duration, counts) and media URLs WITHOUT transcribing or running vision. Cheaper than socialdl_extract — use when the caption/context alone is enough. |
| `socialdl_download` | Resolve a TikTok / Instagram / YouTube link (or direct .mp4/image URL) to its DIRECT download URLs from the source CDN — every video quality, audio track and image, with quality labels. Use when the user wants to DOWNLOAD/save the media instead of transcribing it. No transcription/vision. |

Detalhe de cada tool: [docs/ferramentas.md](docs/ferramentas.md)

---

## Preços

Planos a partir do tier grátis. Veja [docs/precos.md](docs/precos.md).

---

## Privacidade & LGPD

- **Somente leitura**, nenhuma ferramenta altera dados na origem.
- **Sub-processadores**: o LLM host que você escolher (Claude, ChatGPT, Cursor, agente próprio). Lista completa em [docs/privacidade-lgpd.md](docs/privacidade-lgpd.md).
- Os dados retornados pelas tools são enviados ao **LLM host que você escolher**, sub-processador fora do nosso controle. Recomendamos planos com opt-out de treinamento.

---

## Perguntas frequentes

**Pra que serve?**
Pra dar contexto ao seu agente de IA sobre vídeos e posts. Em vez de você assistir, o Claude lê a transcrição e o resumo das imagens e responde sobre o conteúdo.

**Quais plataformas?**
Links de TikTok, Instagram (reel, post, carrossel), YouTube, ou qualquer arquivo .mp4 direto.

**Quanto custa?**
As 3 primeiras chamadas são grátis. Depois, por uso (veja docs/precos.md).

**O servidor é open source?**
O servidor é proprietário (hosted). Este repositório é o wrapper público com manifestos, docs e skills, tudo MIT.


---

## Suporte

- 📧 [socialdl@mcp.ai](mailto:socialdl@mcp.ai)
- 🐛 [GitHub Issues](https://github.com/mcp-dir/socialdl-mcp/issues)
- 📄 [docs/](docs/)

---

## Licença

MIT — veja [LICENSE](LICENSE). O servidor MCP em `api.mcp.ai/p_socialdl` é proprietário (hosted); este repositório (manifestos, docs, skills) é MIT.
