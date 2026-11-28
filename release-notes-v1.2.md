<img src="https://raw.githubusercontent.com/aadilmodsofficial/Android-IDA/main/assets/icon.png" alt="Android IDA" width="96" height="96">

## Android IDA v1.2

ARM disassembler & decompiler for Android, now with a Unity dump viewer, an AI assistant and an MCP server.

### Download
**`Android_IDA_v1.2_Official.apk`** (27.96 MB) below, then install it on an ARM phone running Android 7.0 or newer.

### New in v1.2

**Unity dump viewer**
- Import an IL2CPP `dump.cs` or the game's DLLs; indexing runs in the background and resumes where it stopped
- Classes, structs, enums, interfaces, methods (RVA / offset / VA), fields (offsets) and properties
- Fast search with regex and exact match, bookmarks, history, Back / Forward
- Compare two versions: added / removed classes and methods, changed signatures and offsets

**AI assistant**
- Ask about any function or Unity class; the AI searches the library or dump by itself
- Cloud AI with your own key: Gemini, OpenRouter, GLM, Qwen, Claude, DeepSeek, Kimi, OpenAI or a custom server
- Several API keys per service, searchable model list, auto-switch keys when one hits its limit
- On-device models (`.task` / `.litertlm`) that work offline

**MCP server (VIP)**
- Let any MCP-compatible AI client or agent use Android IDA's tools
- Connect over Wi-Fi, USB, the same phone, or from anywhere through `mcp.aadilmods.com`
- Access token, tool permissions, connected clients and request log

**Decompiler & workspace**
- Much stronger pseudocode: huge and obfuscated functions are decompiled completely, NEON intrinsics, line numbers, export as `.c`
- Unity method names for `libil2cpp.so`: link a dump.cs or dummy DLLs and functions are named like `PlayerControl::FixedUpdate`
- Sync views: Functions, IDA View, Pseudocode and Hex View follow each other (each can be switched off)
- Focus mode search: find text such as `+ 0x58` inside a function, with next / previous
- Open several versions of a game and switch between them in one tap
- Back returns to the line you were reading
- New AI tools: call trees, instruction search, vtables / pointer tables, update-proof signatures to port addresses between versions

**App**
- Portrait layout (the decompiler stays landscape), new home, bottom bar and dialogs
- Projects grouped by game and version

### Already in v1.0
- arm64-v8a and armeabi-v7a (ARM + Thumb-2) libraries
- IDA View, Hex View, Strings, Names, Relocations, ELF Info
- Pseudocode decompiler with types, floating point and switch statements (VIP)
- Modify instruction and ARM Converter
- Saved projects (`.aida`)

See the [README](https://github.com/aadilmodsofficial/Android-IDA#readme) for all features, the [AI & MCP guide](https://app.aadilmods.com/aida/ai), or visit [app.aadilmods.com/aida](https://app.aadilmods.com/aida/).
