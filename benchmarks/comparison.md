# Voice Assistant Comparison

## Current published results

| Device | Quiet, 3.5 m | Fan noise | Own-music wake detected | Own-music command executed |
|---|---:|---:|---:|---:|
| MiciMike Home Mini | 5/5 | 5/5 | 5/5 | 5/5 |
| Third Reality Voice & Music Assistant | 5/5 | 5/5 | 10/10 | 5/10 |
| ReSpeaker XVF3800 | 5/5 | 3/10 | 8/10 | 2/10 |

Quiet, fan-noise, and command-execution values are end-to-end successful attempts
over all recorded attempts. A success requires the complete chain: wake-word
activation, speech recognition, pipeline processing, and execution of the
requested action or response. A failure at any stage is a failed attempt.

The own-music wake-detection column measures activation only, before command
processing and execution. Keeping it separate shows whether failures occurred at
the wake stage or later in the pipeline. The ratios are not normalized scores or
laboratory data.

## Interpretation

All three devices completed the quiet-distance test. Their behaviour separated
under device-generated audio and fan noise. That is useful practical evidence,
but it does not prove that microphone hardware alone caused the difference.
Firmware, wake-word processing, gain, placement, pipeline configuration, room
acoustics, and test execution can all affect the result.

Use this table to identify which full test to inspect, not as a substitute for
the conditions and limitations shown in the videos.

## Required metadata for future runs

Every new benchmark should record:

- test date and Home Assistant version;
- device model, hardware revision, and firmware version;
- wake word and wake-word engine;
- STT engine, conversation agent or intent handler, and TTS engine;
- Assist pipeline name and relevant non-default configuration;
- room, placement, distance, background-noise source, and attempt count.

Unknown values must remain explicitly undocumented rather than being inferred
after the recording.

## Evidence

- [Three-device comparison](https://youtu.be/kKDNd6tnFzE)
- [MiciMike Home Mini benchmark](https://youtu.be/pB5rBzix3V0)
- [Methodology](methodology.md)
