---
name: kokoro-say
description: Speak text aloud or configure TTS using the local Kokoro TTS model (kokoro-say). Use when the user says "/say", "/kokoro-say", "speak aloud", "read this to me", or asks to speak text with Kokoro TTS.
---

# kokoro-say

Speak text aloud or inspect/adjust voice settings with local Kokoro-82M TTS.

## Prerequisites

Ensure `kokoro-say` is installed locally (usually in `~/.local/bin/kokoro-say`).

## Usage

Use `~/.local/bin/kokoro-say` (to avoid conflicting with macOS native `/usr/bin/say`).

### 1. Speak Text in Background (Recommended)
Always run with `--bg` so the command doesn't block the session:

```sh
~/.local/bin/kokoro-say --bg "Your text to speak here"
```

### 2. Speak with a Specific Voice
```sh
~/.local/bin/kokoro-say -v bella --bg "Hello from Bella"
```

### 3. Check Status & Available Voices
- Check current settings:
  ```sh
  ~/.local/bin/kokoro-say --status
  ```
- List all available voices:
  ```sh
  ~/.local/bin/kokoro-say --voices
  ```

### 4. Set Saved Default Voice & Speed
- Set default voice:
  ```sh
  ~/.local/bin/kokoro-say --set-voice <voice_name>
  ```
- Set default speed (0.5 to 2.0):
  ```sh
  ~/.local/bin/kokoro-say --set-speed 1.0
  ```

### 5. Stop Playback
```sh
~/.local/bin/kokoro-say --stop
```

## Guidelines

- Sanitize spoken text: avoid code blocks, backticks, long URLs, raw markdown symbols, and secrets/tokens.
- Escape or quote text safely when invoking shell commands.
