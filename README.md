# Kokoro-Say Skill

An agent skill to speak text aloud, switch voices, and configure text-to-speech settings using the local [Kokoro TTS](https://github.com/hexgrad/kokoro) model (`kokoro-say`).

## Installation

Install using [`npx skills`](https://skills.sh):

```bash
npx skills add NoJuanNobody/kokoro-say-skill -g
```

## Prerequisites

Requires `kokoro-say` available locally (e.g. at `~/.local/bin/kokoro-say`).

## Usage

Trigger in your agent conversations via:
- `/say <text>`
- `/kokoro-say`
- Asking naturally: *"speak this aloud"*, *"read this to me"*, or *"change your TTS voice"*.
