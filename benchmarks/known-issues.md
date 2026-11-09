# Known Issues and Retest Tracking

This page records behaviour observed during published benchmarks. It separates
functional impact from suspected causes and provides a stable reference for
future firmware retests.

An observation is not proof of a firmware, hardware, pipeline, or acoustic root
cause. Causes remain **Unconfirmed** until supported by reproducible evidence.

## Current observations

| Device | Observed issue | Functional impact | Published result or evidence | Cause | Firmware in original test | Observation date | Reproduction record | Retest status |
|---|---|---|---|---|---|---|---|---|
| [MiciMike Home Mini DiP GEN1](../devices/micimike-home-mini/README.md) | Unreliable barge-in | The current response could stop, but the new command often did not execute | Inconsistent barge-in | Unconfirmed | Not confirmed | Not documented | Not yet documented separately | Pending |
| [Third Reality Voice & Music Assistant](../devices/thirdreality-voice-music/README.md) | Stuck `responding` state | Could block subsequent wake words and voice commands until intervention | Observed during the published test | Unconfirmed | Not confirmed | Not documented | Not yet documented separately | Pending |
| [Third Reality Voice & Music Assistant](../devices/thirdreality-voice-music/README.md) | Separation of user speech from the device's own music | Wake word was detected, but commands did not reliably complete | Wake 10/10; command execution 5/10 | Unconfirmed | Not confirmed | Not documented | 5 failures after successful wake detection | Pending |
| [ReSpeaker XVF3800 + XIAO ESP32-S3](../devices/respeaker-xvf3800/README.md) | Stale LED indicator | LED could remain on, but voice commands continued to work | Voice session remained functional | Unconfirmed | Not confirmed | 2026-10-31 | Observed intermittently | Pending |
| [ReSpeaker XVF3800 + XIAO ESP32-S3](../devices/respeaker-xvf3800/README.md) | Command processing during own-music playback | Most commands did not complete after or alongside wake detection | Wake 8/10; command execution 2/10 | Unconfirmed | Not confirmed | 2026-10-31 | Published 10-attempt series | Pending |
| [ReSpeaker XVF3800 + XIAO ESP32-S3](../devices/respeaker-xvf3800/README.md) | Low success with fan interference | Most requested commands did not execute | Command execution 3/10 | Unconfirmed | Not confirmed | 2026-10-31 | Published 10-attempt series | Pending |

## Retest and history policy

Published video results are historical records and must not be overwritten after
a firmware, Home Assistant, ESPHome, pipeline, or configuration update.

Every retest receives a separate dated record containing:

- device model and hardware revision;
- firmware version;
- Home Assistant version;
- wake word and wake-word engine;
- STT, conversation agent or intent handler, and TTS;
- relevant pipeline and non-default configuration;
- room, placement, distance, background source, and volume;
- attempt-level wake detection and command-execution results;
- whether the issue reproduced, improved, disappeared, or changed;
- links to the original benchmark and new evidence.

If the original firmware or configuration cannot be confirmed, keep it marked
as `Not confirmed`. Do not infer it from a later installation.

## Updating an issue

When a retest is available, retain the original row and add a dated retest record
below it or link to a dedicated retest document. A newer result may show an
improvement, but it does not invalidate the conditions or outcome of the
published historical test.
