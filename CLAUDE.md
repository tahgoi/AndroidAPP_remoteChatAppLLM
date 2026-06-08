# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository State

This is a **distribution-only repository** — it contains the compiled `app-release.apk` and documentation. No Android source code (Kotlin/Java, Gradle files, XML resources) is present. The `.gitignore` pattern confirms this is an Android Studio project layout, but source has not been committed.

Target deployment: `https://github.com/tahgoi/AndroidAPP_remoteChatAppLLM.git`

## App Overview

**remoteLLMChatApp** (v1.18) is an Android AI chat app with two switchable backends:

- **Local engine:** LM Studio via HTTP/SSE to a LAN or Tailscale server (default port 1234)
- **Cloud engine:** Google Gemini REST API (default model: `gemini-2.5-flash`)

Switching between engines happens at runtime without restarting the app.

## Key Architecture Points

- **Streaming:** Both engines deliver responses token-by-token via Server-Sent Events (SSE)
- **Multimodal:** File attachments are Base64-encoded; vision capability is inferred from model name patterns
- **Storage:** Room ORM for chat history, DataStore for settings/credentials — all local, no cloud sync
- **Server polling:** LM Studio model availability is checked every 10 seconds in the background
- **Android 15+ (API 35+):** Requires `ACCESS_LOCAL_NETWORK` runtime permission for LAN access; requested automatically on first launch
- **AMOLED theme:** Pure `#000000` background; layout anchored to bottom for Samsung S25 Ultra one-hand reachability

## Open Tasks (from myPlan.md)

- Deploy source to GitHub: `https://github.com/tahgoi/AndroidAPP_remoteChatAppLLM.git`
- Verify README screenshots render correctly
- Ensure no API keys or passwords appear in any committed files (mask with `***`)
- Do not mention Claude or Gemini in the Contributors section
