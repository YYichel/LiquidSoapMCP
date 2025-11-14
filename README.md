# ⭐ Liquidsoap MCP Server  
### *AI-powered, version-accurate Liquidsoap scripting using the official 2.4.0 docs.*

![Stars](https://img.shields.io/github/stars/splinesreticulating/liquidsoap-mcp?style=social)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

LLMs get Liquidsoap wrong *all the time*—mixing 1.x docs, outdated blog posts, and half-remembered API examples.

**This MCP server fixes that.**

It gives your AI assistant (Claude, ChatGPT, Cursor, Windsurf, etc.) **real Liquidsoap 2.4.0 documentation, examples, and API references**, making it finally possible to:

- Understand `.liq` scripts  
- Generate correct 2.4.0 code  
- Fix errors and deprecated usage  
- Explore operators, functions, transitions, and patterns  
- Build web radio pipelines with confidence  

No hallucinations. No version drift. No mystery errors.

---

# 🚀 Why this exists

Liquidsoap is incredibly powerful—but:

- Documentation varies heavily between versions  
- 1.x and 2.x syntax differs in subtle ways  
- LLMs blend outdated examples into their answers  
- Even the official docs are spread across sections, pages, and changelogs  

**This MCP server gives your AI one job:**  
📌 *Stick to Liquidsoap 2.4.0 exactly.*

It exposes a clean, structured API around the official docs so your assistant becomes a reliable Liquidsoap expert.

---

# ✨ Features

## 📚 Version-Pinned Documentation (2.4.0)
- Full language reference  
- Core API functions & operators  
- Protocols (Icecast, HLS, HTTP, SRT, etc.)  
- Encoder/decoder options  
- Runtime settings  

## 🔍 Smart Search
- Search functions/operators by name or keyword  
- Search through examples, patterns, and cookbook items  
- Search 2.4.0 changelog & migration notes

## 🧪 Script Assistance
- Detect deprecated functions (e.g. `null()`, `insert_metadata`)  
- Warn about 1.x syntax  
- Highlight common design pitfalls  

## 🧩 Example Library
Includes ready-to-use code snippets for:

- Crossfading  
- Fallback chains  
- Harbor live input  
- HLS output  
- Cron scheduling (`cron.add`, `cron.parse`)  
- Metadata rewriting  
- LUFS normalization  
- Blank detection  
- Multi-output pipelines  

## ⚡ Fast & Local  
- Docs cached and indexed for instant responses  
- No web requests needed once running  

---

# 📸 Demo (example)

*(Add GIF or screenshots here)*

Ask natural questions like:

- “Explain what this Liquidsoap script does.”  
- “Add a safe fallback chain before the HLS output.”  
- “Show the API docs for `crossfade`.”  
- “Rewrite this script using the new 2.4.0 `null` semantics.”  

Your AI responds using *only* the real 2.4.0 documentation.

---

# 🛠 Installation

## Prerequisites
- Node.js ≥ 18  
- Any MCP-compatible client (Claude Desktop, ChatGPT Desktop, Cursor, Windsurf, etc.)

## Install via npm (recommended)

```bash
npm install -g liquidsoap-mcp-server
```

## Or run from source

```bash
git clone https://github.com/yourname/liquidsoap-mcp.git
cd liquidsoap-mcp
npm install
npm run build
```

---

# 💬 Usage

## Claude Desktop Example

**macOS:**  
`~/Library/Application Support/Claude/claude_desktop_config.json`

**Windows:**  
`%APPDATA%/Claude/claude_desktop_config.json`

```json
{
  "mcpServers": {
    "liquidsoap": {
      "command": "npx",
      "args": ["-y", "liquidsoap-mcp-server"]
    }
  }
}
```

## From source:

```json
{
  "mcpServers": {
    "liquidsoap": {
      "command": "node",
      "args": ["/absolute/path/to/liquidsoap-mcp/build/index.js"]
    }
  }
}
```

---

# 🧠 Supported Tools

## 🔧 Core Tools
- `get_version`
- `list_sections`
- `get_documentation(section)`
- `search_functions(query)`
- `get_changelog`
- `get_examples(topic)`
- `validate_script_syntax(script)`

## 📁 Documentation Sections
- `language`
- `reference`
- `protocols`
- `settings`
- `encoding_formats`
- `ffmpeg`
- `quickstart`
- `cookbook`

---

# 🎯 Roadmap

- [ ] Add Liquidsoap script graph visualization  
- [ ] Integrate `liquidsoap --check` for real syntax/type validation  
- [ ] Multi-version switching (2.2.x, 2.3.x)  
- [ ] Fuzzy search & semantic examples  
- [ ] “Explain this error log” tool  
- [ ] Snippet library for common pipeline patterns  

---

# 🤝 Contributing

PRs welcome—especially:

- New examples  
- Improved search  
- Doc parsing improvements  
- More validation rules  
- Better MCP client integrations  

---

# 📚 Resources

- https://www.liquidsoap.info/doc-2.4.0/  
- https://modelcontextprotocol.io/  
- https://github.com/modelcontextprotocol/typescript-sdk  

---

# ❤️ Acknowledgments

Built for the Liquidsoap community—and for all the radio nerds, DJs, and hobby streamers who want to make Liquidsoap easier, safer, and way more fun with AI assistance.

---

## ⭐ Want to support the project?

**Please star the repo!**  
It helps others discover it and tells me this niche was worth carving out.
