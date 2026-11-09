# MiciMike Home Mini DiP GEN1

**Status:** Published / tested

The MiciMike Home Mini DiP GEN1 replaces the PCB in an original Google Home
Mini while reusing its enclosure and speaker for Home Assistant voice use.

## Benchmark results

| Test | Result |
|---|---:|
| Quiet, 1 m | 5/5 |
| Quiet, 3–4 m | 5/5 |
| Fan interference | 5/5 |
| Competing YouTube speech | 3/5 |
| Wake word during own music playback | 5/5 |
| Command execution during own music playback | 5/5 |
| False wakes during 15 minutes | 0 |
| Sophia single intent | Success |
| Sophia dual intent | Success |
| Sophia triple intent | Partial |
| Barge-in | Inconsistent |
| Continued conversation | Not reliably working |

The own-music rows separate wake detection from completed command execution.
Other ratios are end-to-end results unless a row explicitly names one pipeline
stage. An end-to-end success requires activation, recognition, processing, and
execution to complete.

## Test observations

- The background-speech test used the creator's own voice.
- The Sophia triple-intent result was partial: the first request to turn on the
  light did not execute, while the temperature and main-door requests succeeded.
  A speech-recognition problem required that segment to be recorded again.
- Barge-in could interrupt TTS but often failed to execute the following command.
- Microphone performance was good under the tested conditions.
- The original Google Home Mini hardware provided strong speaker audio.

## Recorded test metadata

| Field | Value |
|---|---|
| Test date | Not documented in the current public record |
| Home Assistant version | Not documented in the current public record |
| Device firmware | Not documented in the current public record |
| Wake word and engine | `Okay Nabu` and `Hey Jarvis`; engine and version not confirmed |
| STT / agent / TTS | `faster-whisper`; standard Home Assistant agent and Sophia NLU; exact versions and TTS not confirmed |
| Assist pipeline configuration | Standard Home Assistant agent pipeline plus a second Sophia NLU pipeline; exact settings not confirmed |

## Links and resources

### Video

- [YouTube review](https://youtu.be/pB5rBzix3V0)

### Product

- [Official MiciMike Home Mini DiP GEN1 page](https://www.micimike.com/gen1.html)
- [MiciMike manufacturer website](https://micimike.com/)
- Affiliate link: none confirmed

### Testing

- [Comparison table](../../benchmarks/comparison.md)
- [Test methodology](../../benchmarks/methodology.md)

## Affiliate disclosure

No affiliate product link is currently listed for this device. Links marked as
affiliate elsewhere in this repository may earn Bearded Tinker a small
commission at no additional cost to you.
