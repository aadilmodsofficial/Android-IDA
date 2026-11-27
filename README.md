<div align="center">

<img src="assets/icon.png" alt="Android IDA icon" width="128" height="128">

# Android IDA

**ARM disassembler & decompiler for Android, right on your phone.**

Open any `.so` library or Unity IL2CPP dump, browse functions and classes, read ARM code, turn it into readable C-like pseudocode, and let AI help you.

[![Release](https://img.shields.io/github/v/release/aadilmodsofficial/Android-IDA?label=latest&color=3B82F6)](https://github.com/aadilmodsofficial/Android-IDA/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/aadilmodsofficial/Android-IDA/total?color=17B5D6)](https://github.com/aadilmodsofficial/Android-IDA/releases)
![Android](https://img.shields.io/badge/Android-7.0%2B-3DDC84?logo=android&logoColor=white)
![ABI](https://img.shields.io/badge/ABI-arm64--v8a%20%7C%20armeabi--v7a-555)

[**⬇ Download the latest APK**](https://github.com/aadilmodsofficial/Android-IDA/releases/latest) &nbsp;·&nbsp; [**🌐 Website**](https://app.aadilmods.com/aida/) &nbsp;·&nbsp; [**🤖 AI & MCP guide**](https://app.aadilmods.com/aida/ai)

</div>

---

## Features

### Analysis
- Opens ELF shared libraries (`.so`) and executables: **arm64-v8a**, **armeabi-v7a (ARM & Thumb-2)**
- Automatic function discovery, symbols (with C++ demangling), strings, relocations, PLT stubs, xrefs
- ELF info: header, sections, segments, dynamic table
- Projects (`.aida`) grouped by **game and version**: the analysis, names and your place are saved, so reopening is instant
- Open **several versions** of a game and switch between them in one tap

### Views
- **IDA View**: disassembly with line numbers, names, branch targets and data references
- **Pseudocode** *(VIP)*: C-like decompiler for arm64, ARM and Thumb
  - typed variables, parameters and return values (`bool`, `int`, `float`, `double`, `char *`, `std::string`, pointers, etc.)
  - `if` / `while` / `do-while` / `switch` (jump tables), floating point (VFP / AArch64 FP), NEON intrinsics
  - huge and obfuscated functions are decompiled completely (code behind computed jumps included)
  - line numbers, export as `.c`
- **Hex View**: file bytes with offsets and ASCII
- **Strings**, **Names**, **Relocations**, **ELF Info**
- Split view, focus mode, Back / Forward that return to the line you were reading
- **Sync views**: Functions, IDA View, Pseudocode and Hex View follow each other (each can be switched off)
- **Find in function** (focus mode): search text like `+ 0x58` or bytes, with next / previous
- Tap a word to highlight it everywhere (registers, variables, names); fast scrollbar on every list

### Unity
- **Unity dump viewer**: import an IL2CPP `dump.cs` or the game's DLLs
  - classes, structs, enums, interfaces, methods (RVA / offset / VA), fields (offsets), properties
  - fast search with regex and exact match, bookmarks, history, Back / Forward
  - compare versions: added / removed classes and methods, changed signatures and offsets
- **Unity method names for `libil2cpp.so`**: link a dump.cs or dummy DLLs and functions are named like `PlayerControl::FixedUpdate`

### AI
- **AI assistant** in the decompiler and the Unity viewer: ask in plain words, the AI searches the library or dump by itself
- **Cloud AI** with your own API key: Gemini, OpenRouter, GLM, Qwen, Claude, DeepSeek, Kimi, OpenAI or a custom server; several keys per service and auto-switch when one hits its limit
- **On-device AI**: `.task` / `.litertlm` models that run offline on your phone
- **MCP server** *(VIP)*: let any MCP-compatible AI client or agent use Android IDA's tools over Wi-Fi, USB, the same phone or from anywhere, with an access token and tool permissions
- AI tools include call trees, instruction search, vtables / pointer tables and update-proof signatures to port addresses between versions

See the [AI & MCP guide](https://app.aadilmods.com/aida/ai) for setup.

### Patching
- **Modify instruction** *(VIP)*: return a fixed `bool` / `int` / `int64` / `float` / `double`, NOP, always / never jump, invert a condition, skip a call, or any custom ARM code
- **ARM Converter**: ARM to hex and back for arm64, ARM and Thumb, with the instruction address for correct branch targets
- Copy bytes as hex or as a C++ array, save function offsets

---

## Download & install

1. Go to **[Releases](https://github.com/aadilmodsofficial/Android-IDA/releases/latest)** and download `Android_IDA_vX.Y_Official.apk`.
2. Open it on your phone and allow *Install unknown apps* for your browser / file manager if Android asks.
3. Sign in with Google.

**Requirements:** Android 7.0 (API 24) or newer, an ARM phone (arm64 or 32-bit ARM), internet connection.

---

## Free vs VIP

| | Free | VIP |
|---|:---:|:---:|
| IDA View, Hex View, Strings, Names, ELF Info, Relocations | ✅ | ✅ |
| ARM Converter | ✅ | ✅ |
| Unity dump viewer & Unity method names | ✅ | ✅ |
| AI assistant (your own key or on-device model) | ✅ | ✅ |
| Pseudocode (decompiler), also for the AI | ❌ | ✅ |
| MCP server for AI clients | ❌ | ✅ |
| Modify instruction | ❌ | ✅ |
| Device access | free, activate with a short link | ✅ always |
| Ads | yes | **no ads** |

VIP is linked to one device. You can get it from the **VIP** tab in the app.

---

## Screenshots

| IDA View | Pseudocode |
|---|---|
| ![IDA View](screenshots/ida-view.webp) | ![Pseudocode](screenshots/pseudocode.webp) |
| **Hex View** | **Projects** |
| ![Hex View](screenshots/hex-view.webp) | ![Projects](screenshots/projects.webp) |

---

## FAQ

**Why do I need to sign in and be online?**
Your account holds your VIP and device access, so the app checks them with the server. The libraries and dumps you open stay on your phone and are never uploaded to us.

**Is my code sent anywhere when I use AI?**
Only if you choose Cloud AI: then the code you ask about goes to the AI service you picked, with your own key. On-device models send nothing. MCP clients you connect can read only what you allow.

**Android or Play Protect warns me when installing.**
That is normal for apps installed outside Google Play. Download only from this page or the website, then choose *Install anyway*.

**Which files can I open?**
ARM ELF files: `.so` libraries (and executables) built for arm64-v8a or armeabi-v7a, for example from `lib/arm64-v8a/` inside an APK. x86 libraries are not supported. The Unity tab imports an IL2CPP `dump.cs` (from Il2CppDumper) or the game's DLLs.

**Does it work offline?**
Opening a library needs a connection for the access check. Saved projects keep their analysis, so they open quickly afterwards. On-device AI works offline.

---

## Support

- 🌐 **Website:** [app.aadilmods.com/aida](https://app.aadilmods.com/aida/)
- 🤖 **AI & MCP guide:** [app.aadilmods.com/aida/ai](https://app.aadilmods.com/aida/ai)
- 🐞 **Bugs / ideas:** use *Report an issue* / *Request a feature* inside the app, or open an [issue](https://github.com/aadilmodsofficial/Android-IDA/issues)
- 💬 **Discord:** [discord.gg/cnw8tYRRbN](https://discord.gg/cnw8tYRRbN)
- ✈️ **Telegram:** [t.me/aadilmodsofficial](https://t.me/aadilmodsofficial)
- 📸 **Instagram:** [@aadilmods](https://instagram.com/aadilmods)

---

## Notice

Android IDA is **closed source**; this repository only hosts releases and documentation.
It is an independent project and is **not affiliated with Hex-Rays or IDA Pro**.
Use it only on software you own or are allowed to analyse.

See [LICENSE](LICENSE) for the terms of use.
