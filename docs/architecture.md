# Architecture notes

## Device responsibilities
- Local animation loop, eye states and idle behavior
- Microphone capture and speaker playback
- Physical controls, clear mute/listening indication
- Simple command/event protocol

## Host responsibilities
- System telemetry gathering
- Speech transcription and synthesis (or streaming voice service)
- LLM or assistant orchestration
- Configuration and downloadable theme assets

## Suggested initial event vocabulary
- `set_expression`: idle, happy, sleepy, curious, spooky, listening, thinking, speaking
- `set_gaze`: normalized x/y coordinates
- `show_metric`: key, value, duration
- `voice_start`, `voice_stop`
- `ping` / `device_status`

Protocol and transport intentionally TBD until hardware tests.
