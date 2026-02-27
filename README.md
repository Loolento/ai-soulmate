# AI Soulmate (AI 心靈伴侶)

## 💎 Product Vision
A luxury, B2B smart home product designed for high-end bathrooms.
*   **Core Value:** A "Soulmate" in the ceiling that cares for your mental wellness through **Spoken Wisdom**.
*   **Target Audience:** High-net-worth individuals, luxury property developers.
*   **USP (Unique Selling Point):** 
    *   **Zero Friction:** One-button activation.
    *   **Privacy First:** No camera, no voice recognition, "Dumb Mode" switch.
    *   **Content First:** Curated "Chicken Soup" & Book Summaries (Primary), supported by high-quality music (Secondary).

## 🛁 User Experience (The "Morning Routine")
1.  **Trigger:** User enters bathroom or presses the **Smart Knob**.
2.  **Greeting:** "Good morning Joe! The weather is [Weather] today. How are you feeling?"
3.  **Interaction:** User replies (Good / Bad / So-so) or rotates knob.
4.  **Content Delivery (Prioritized):**
    *   **Primary (The "Soul"):** 
        *   **Motivational Stories:** (e.g., Tao Jie, Sammy Leung, Joe's Voice).
        *   **Book Summaries:** 5-minute essence of bestsellers.
    *   **Secondary (The "Vibe"):** 
        *   **Music:** Lo-fi, Classical, Jazz (Royalty-free).
        *   **Sound Effects:** Nature sounds (rain, forest).
        *   **Mindfulness:** Guided meditation.
5.  **Exit:** AI goes silent/standby.

## 🛠 Hardware Specs
*   **Core:** **ESP32-S3** ("XiaoZhi" / 小智 board).
*   **Interface:** **Smart Rotary Knob** with integrated LED screen (Ref: M5Stack Dial).
    *   *Click:* Wake/Confirm.
    *   *Rotate:* Volume/Selection.
    *   *Long Press:* Switch Mode (AI <-> Bluetooth).
*   **Audio:** High-quality I2S Amp connected to ceiling speakers (Bose/KEF).
*   **Connectivity:** WiFi (to Server) + Bluetooth (A2DP Sink).

## ☁️ Backend Architecture (Hetzner Server)
*   **STT:** OpenAI Whisper (Voice to Text).
*   **LLM:** Lightweight logic (or ChatGPT) with system prompt: *Warm, empathetic, no complex facts.*
*   **TTS:** Microsoft Edge TTS (Cantonese - Xiaoxiao/Yunxi).
*   **Content Engine:** `yt-dlp` to fetch YouTube audio (motivational/books) -> Convert to MP3.

## 📅 Roadmap
1.  **Phase 1 (Server):** Setup API for STT/TTS and Content Library (YouTube downloader).
2.  **Phase 2 (Hardware):** Flash ESP32 with initial firmware to test WiFi & Audio.
3.  **Phase 3 (Integration):** Connect Hardware Knob to Server logic.
