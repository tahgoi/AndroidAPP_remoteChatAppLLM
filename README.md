# remoteChatAppLLM

**Version:** 1.18  
**Developer:** xAPPS-Lab.ca  
**Website:** [android.xapps-lab.com](https://android.xapps-lab.com)  
**LinkedIn:** [jstaguan](https://www.linkedin.com/in/jstaguan)  
**Privacy Policy:** [androidapps.xapps-lab.com/privacy](https://androidapps.xapps-lab.com/privacy)

## APP Status:Under Internal Testing

Drop us your gmail to download your pre-release app from playstore.

Pre-Release Download: https://play.google.com/apps/internaltest/4700612420796748501

email: android.xappslab@gmail.com
---

## Core Features

- **Dual-engine AI** — switch at runtime between a local LM Studio instance and Google Gemini cloud API
- **Streaming responses** — token-by-token output via Server-Sent Events (SSE) on both engines
- **Multimodal chat** — attach any file from the system file manager; images sent as Base64
- **Markdown & code rendering** — built-in renderer with syntax highlighting (no third-party library)
- **Chat history** — multiple named sessions; swipe left from chat to browse and restore past conversations
- **Model capability icons** — vision / reasoning / tools indicators derived from model name
- **Server management** — add multiple LM Studio servers; models auto-detected via 10-second background poll
- **Local-first privacy** — all chat history, settings, and credentials stored on-device via Room + DataStore; no analytics or telemetry
- **AMOLED black theme** — pure black (#000000) background for battery savings on OLED displays
- **Samsung S25 Ultra optimized** — bottom-anchored input and reachability-friendly layout

---

## How to Configure LM Studio

1. Run LM Studio on your PC and load a model. Enable the local server (default port **1234**).
2. Open the app and tap the **Settings** icon (gear).
3. Select the **LM Studio** tab.
4. Tap **Add Server**, enter a nickname and the server's IP address (e.g. `http://192.168.1.x`), then confirm.
5. The server card shows a green **Online** badge when the ping succeeds.
6. **Tap the server card** to expand its model list, then select a model. The list closes automatically after selection.

> **Emulator note:** When testing on the Android emulator, the host machine is reachable at `169.254.xx.xx` or `10.0.2.2`.

> **Real device note:** Android 15 (API 35+) requires the `ACCESS_LOCAL_NETWORK` runtime permission for LAN access. The app requests this automatically on first launch.

---

## How to Configure Gemini API

1. Get an API key from [Google AI Studio](https://aistudio.google.com/app/apikey).
2. Open the app and tap the **Settings** icon.
3. Select the **Gemini CLI** tab.
4. Paste your API key and tap **Validate Key** to confirm it works.
5. Select your preferred model (default: **gemini-2.5-flash**).
6. Optionally set a system prompt, temperature, and top-P.

---

## App Screenshots

<table>
  <tr>
    <td align="center" colspan="3">
      <img src="./screenshots/00_deployment.png" alt="Deployment Setup" width="700"/><br/>
      <sub><b>Deployment Setup</b></sub>
    </td>
  </tr>
  <tr>
    <td align="center" width="33%">
      <img src="./screenshots/01_UI-LMStudiowithMistralai.jpg" alt="LM Studio + Mistral AI" width="220"/><br/>
      <sub><b>LM Studio + Mistral AI</b></sub>
    </td>
    <td align="center" width="33%">
      <img src="./screenshots/02_UI-LMStudiowithQwen.jpg" alt="LM Studio + Qwen" width="220"/><br/>
      <sub><b>LM Studio + Qwen</b></sub>
    </td>
    <td align="center" width="33%">
      <img src="./screenshots/03_UIwithGeminiFlash.jpg" alt="Gemini Flash UI" width="220"/><br/>
      <sub><b>Gemini Flash UI</b></sub>
    </td>
  </tr>
  <tr>
    <td align="center" width="33%">
      <img src="./screenshots/04_GeminiCLI-APIKey.jpg" alt="Gemini API Key Setup" width="220"/><br/>
      <sub><b>Gemini API Key Setup</b></sub>
    </td>
    <td align="center" width="33%">
      <img src="./screenshots/05_LMStudioServer_LAN.jpg" alt="LM Studio Server (LAN)" width="220"/><br/>
      <sub><b>LM Studio Server (LAN)</b></sub>
    </td>
    <td align="center" width="33%">
      <img src="./screenshots/06_LMStudioServer_Tailscale.jpg" alt="LM Studio via Tailscale" width="220"/><br/>
      <sub><b>LM Studio via Tailscale</b></sub>
    </td>
  </tr>
  <tr>
    <td align="center" width="33%">
      <img src="./screenshots/07_TwoLMStudioServer_Tailscale.jpg" alt="Two Servers via Tailscale" width="220"/><br/>
      <sub><b>Two Servers via Tailscale</b></sub>
    </td>
    <td align="center" width="33%">
      <img src="./screenshots/08_TwoLMStudioServer_Models.jpg" alt="Two Servers — Model List" width="220"/><br/>
      <sub><b>Two Servers — Model List</b></sub>
    </td>
    <td align="center" width="33%">
      <img src="./screenshots/09_TwoLMStudioServer_ModelSelected.jpg" alt="Model Selected" width="220"/><br/>
      <sub><b>Model Selected</b></sub>
    </td>
  </tr>
  <tr>
    <td align="center" width="33%">
      <img src="./screenshots/10_LMStudioServer_ChatGemma4B.jpg" alt="Chat with Gemma 4B" width="220"/><br/>
      <sub><b>Chat with Gemma 4B</b></sub>
    </td>
    <td align="center" width="33%">
      <img src="./screenshots/10_LMStudioServer_ImageAnalysisMistralAI.jpg" alt="Image Analysis (Mistral AI)" width="220"/><br/>
      <sub><b>Image Analysis (Mistral AI)</b></sub>
    </td>
    <td align="center" width="33%">
      <img src="./screenshots/11_LMStudioServer_ImageAnalysisGemini-2.5-Flash.jpg" alt="Image Analysis (Gemini 2.5 Flash)" width="220"/><br/>
      <sub><b>Image Analysis (Gemini 2.5 Flash)</b></sub>
    </td>
  </tr>
  <tr>
    <td align="center" width="33%">
      <img src="./screenshots/12_LMStudioServer_ImageAnalysisGemini-2.5-Flash.jpg" alt="Image Analysis — Detail View" width="220"/><br/>
      <sub><b>Image Analysis — Detail View</b></sub>
    </td>
    <td align="center" width="33%">
      <img src="./screenshots/13_LocalAI%20or%20CloudAI.jpg" alt="Local AI vs Cloud AI Toggle" width="220"/><br/>
      <sub><b>Local AI vs Cloud AI Toggle</b></sub>
    </td>
    <td align="center" width="33%"></td>
  </tr>
</table>

---

## Release Notes

### v1.01
- Initial release: AMOLED black theme, dual-engine support (LM Studio + Gemini), Samsung S25 Ultra reachability optimizations
