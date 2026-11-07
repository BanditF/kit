# Kit 👁️

**Kit** is an open, modular AI familiar: a small orb with an expressive domed eye, microphone, speaker, and an optional connection to a PC-hosted AI.

## Vision

Kit starts as a USB-powered desk companion. It can animate independently, show PC telemetry, and act as a voice interface to AI services running locally or remotely. Eventually the orb can move between interchangeable bodies and a charging dock.

## Roadmap

### V0: Optical proof of concept
- [ ] Select round display/controller (candidate: Waveshare ESP32-S3 1.46-inch)
- [ ] Test convex lens and display spacing
- [ ] Create basic blinking and eye-tracking animations
- [ ] Measure actual board/enclosure dimensions

### V1: Desktop familiar
- [ ] USB-powered orb enclosure and desk mount
- [ ] Audio input/output tests
- [ ] PC companion protocol over USB or Wi-Fi
- [ ] PC telemetry display
- [ ] Push-to-talk voice loop to external/local AI
- [ ] Privacy control and mute indicator
- [ ] Seasonal themes, including Halloween eyeball

### V2: Portable orb
- [ ] Battery, protection, charge management
- [ ] Docking interface; evaluate Qi vs magnetic contacts
- [ ] Modular shell/body attachment

### V3: Mobile body
- [ ] Motorized base, obstacle sensing, and docking

## Proposed architecture

```text
                    +---------------------------+
                    | PC / local server / cloud |
                    | AI, speech, PC telemetry  |
                    +-------------+-------------+
                                  | USB / Wi-Fi
                    +-------------v-------------+
                    | Kit orb / ESP32-S3         |
                    | Animated eye, mic, speaker|
                    | local behavior, controls  |
                    +-------------+-------------+
                                  |
                    Optional future body/dock
```

## Guiding principles

1. The **orb is the character**; bodies are interchangeable.
2. It works as an expressive display even without an AI connection.
3. AI inference is off-device by default.
4. Design for future mobility, but do not build it into V1.
5. Prefer assembled modules and avoid soldering where practical.
6. Verify optics, physical fit, battery safety, and audio performance empirically.
7. Clearly indicate when the microphone is active; prefer a hardware mute.

## Status

Planning and hardware evaluation. No production firmware or validated enclosure yet.

## Layout

- `docs/` design notes and decisions
- `hardware/` component shortlist and mechanical notes
- `firmware/` eventual microcontroller implementation
- `companion/` eventual PC-side bridge/AI integration
- `assets/` eventual eye skins and animations

## License

TBD before distributing firmware or artwork.
