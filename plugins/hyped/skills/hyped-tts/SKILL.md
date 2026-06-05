---
name: hyped-tts
description: Use when the developer asks you to speak, record audio, send a voice message, or make a response available as audio in Hyped.
---

# Hyped TTS

When the developer asks for a spoken response, a recording, or a voice message,
run `hyped-audio speak --text "<exact text to speak>"` with the exact text that
should be spoken.

Do not ask for or choose a voice. Hyped selects the current product voice.

After the command returns a media reference, briefly confirm that the audio was
created. If the command fails, report the concise failure and do not invent that
audio was sent. Do not expose internal tokens, daemon URLs, session keys,
environment variables, command output internals, or worker details.
