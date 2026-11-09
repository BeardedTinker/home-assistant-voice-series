# Seeed Studio ReSpeaker XVF3800 + XIAO ESP32-S3

**Status:** Published / tested

The tested hardware was the ReSpeaker XVF3800 4-Mic Array with XIAO ESP32-S3,
XMOS XVF3800 audio processing, four microphones, an LED ring, external audio
connections, a 3.5 mm output, and a speaker connector.

> [!IMPORTANT]
> The tested product is the version **without case**. It included the speaker in
> the tested configuration. Do not substitute the With Case product variant.

## Benchmark results

| Test | Result |
|---|---:|
| Quiet, 1 m | 5/5 |
| Quiet, 3.5 m | 5/5 |
| Fan interference | 3/10 |
| Competing speech, laptop approximately 1 m from device | 0/5 commands |
| Competing speech, laptop approximately 3 m from device | 5/5 commands |
| Own music wake detected | 8/10 |
| Own music command executed | 2/10 |
| False wakes during 15 minutes | 0 |
| Sophia single intent | Success |
| Sophia dual intent | Success |
| Sophia triple intent | Partial |
| Barge-in during thinking | Failed |
| Barge-in during TTS | Failed |
| Continued conversation | 0/3 |

The own-music rows intentionally separate wake recognition from end-to-end
success. A complete success requires activation, recognition, processing, and
execution. The wake word was detected on 8 of 10 attempts, but only 2 of 10
commands executed; microphone count alone does not guarantee reliable separation
and processing of speech over the device's own music.

## Test observations

- The fan test was performed at approximately 3.5 m, with the fan approximately
  1.5 m from the device.
- The LED ring occasionally remained illuminated after a command, but voice
  functionality continued and the device accepted new commands. This was a stale
  indicator, not a confirmed stuck voice session.
- TTS at 25% was practically inaudible and 50% was very quiet.
- TTS at 75% and 100% was clean and sounded good.
- Microphone mute was not tested.
- Speaker performance should not be judged only from the initial 50% volume test.

## Recorded test metadata

| Field | Value |
|---|---|
| Test date | 2026-10-31 |
| Home Assistant version | Not documented in the current public record |
| Device firmware | Not documented in the current public record |
| Wake word and engine | Not documented in the current public record |
| STT / agent / TTS | Sophia tests recorded; exact versions not documented |
| Assist pipeline configuration | Not documented in the current public record |

## Links and resources

### Video

- [YouTube review](https://youtu.be/IY_zPQ-xLg4)

### Product

- [Official without-case product page — affiliate link](https://www.seeedstudio.com/ReSpeaker-XVF3800-4-Mic-Array-With-XIAO-ESP32S3-p-6489.html?sensecap_affiliate=lxIbXWq&referring_service=link)

### Documentation and firmware

- [Home Assistant setup guide](https://wiki.seeedstudio.com/respeaker_xvf3800_xiao_home_assistant/)

### Testing

- [Comparison table](../../benchmarks/comparison.md)
- [Test methodology](../../benchmarks/methodology.md)

## Affiliate disclosure

The product link above is an affiliate link. If you purchase through it,
Bearded Tinker may earn a small commission at no additional cost to you.
