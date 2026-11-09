# Third Reality Voice & Music Assistant Dev Edition

**Status:** Published / tested

This is the Development Edition: a Linux-based, quad-core ARM Cortex-A53 device
with 256 MB RAM, 512 MB flash, dual digital microphones, a built-in 3 W speaker,
and 2.4 GHz Wi-Fi. The official listed price at filming was USD 69.99.

## Benchmark results

| Test | Result |
|---|---:|
| Quiet, 1 m | 5/5 |
| Quiet, 3.5 m | 5/5 |
| Fan interference | 5/5 |
| Competing YouTube speech | 3/5 |
| Wake word during own music playback | ~5/10 |
| False wakes during 15 minutes | 0 |
| Sophia single intent | Success |
| Sophia dual intent | Partial |
| Sophia triple intent | Error |
| Barge-in during thinking | Failed |
| Barge-in during TTS | Failed |
| Continued conversation | Failed |

`~` marks an approximate result from the published material rather than a raw
attempt table. The ratios are end-to-end results unless a row explicitly
measures only wake recognition. Continued conversation was tested at 0.5, 5,
and 10 seconds.

## Test observations

- Voice activation during music playback was unreliable.
- Occasional stuck responding states were observed and could prevent new commands.
- Recovery sometimes required intervention; the firmware root cause was not confirmed.
- The built-in speaker was adequate for voice and casual radio.
- The device has no standard 3.5 mm audio output.

## Recorded test metadata

| Field | Value |
|---|---|
| Test date | Not documented in the current public record |
| Home Assistant version | Not documented in the current public record |
| Device firmware used during filming | Not yet confirmed |
| Wake word and engine | Not documented in the current public record |
| STT / agent / TTS | Sophia tests recorded; exact versions not documented |
| Assist pipeline configuration | Not documented in the current public record |

## Firmware follow-up

Official release `v1.2.0` includes changes related to echo cancellation,
continued conversation, and process stability. This is a retest candidate, not
evidence of improvement. Before making any comparison claim, confirm both
firmware versions and repeat the same benchmark conditions.

## Links and resources

### Video

- [YouTube review](https://youtu.be/XkbWu0dwHzw)

### Product

- [Official Development Edition product page — affiliate link](https://www.thirdreality.com/products/voice-music-assistant-dev-edition?ref=BeardedTinker)

### Documentation and firmware

- [Official firmware repository](https://github.com/thirdreality/voice-music-assistant)
- [Firmware releases](https://github.com/thirdreality/voice-music-assistant/releases)

### Testing

- [Comparison table](../../benchmarks/comparison.md)
- [Test methodology](../../benchmarks/methodology.md)

## Affiliate disclosure

The product link above is an affiliate link. If you purchase through it,
Bearded Tinker may earn a small commission at no additional cost to you.
