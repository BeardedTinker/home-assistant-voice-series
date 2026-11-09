# Home Assistant Voice Series

Real-world testing of Home Assistant-compatible voice hardware, Assist pipelines,
and the practical trade-offs that appear in an actual home.

This repository is the long-term technical reference for the Bearded Tinker
Voice Assistant video series. It contains our test methodology, recorded results,
configuration notes, and links to the original projects. It does **not** mirror
third-party firmware, models, or documentation.

## Published benchmarks

| Device | Quiet, 3.5 m | Fan noise | Own music | Device notes |
|---|---:|---:|---:|---|
| MiciMike Home Mini DiP GEN1 | 5/5 | 5/5 | 5/5 | [Results](devices/micimike-home-mini/README.md) |
| Third Reality Voice & Music Assistant | 5/5 | 5/5 | ~5/10 | [Results](devices/thirdreality-voice-music/README.md) |
| ReSpeaker XVF3800 + XIAO ESP32-S3 | 5/5 | 3/10 | 2/10 | [Results](devices/respeaker-xvf3800/README.md) |

Each ratio is an **end-to-end success rate**. An attempt counts as successful
only when activation, recognition, processing, and execution all complete.
These are not laboratory scores. `~` marks an approximate result reported from
the published material. Conditions and configurations were not necessarily
identical; read [the comparison notes](benchmarks/comparison.md) before drawing
conclusions.

## Upcoming devices

| Order | Device or comparison | Status |
|---:|---|---|
| 1 | Home Assistant Voice Preview Edition | Owned / not yet benchmarked |
| 2 | M5Stack Atom VoiceS3R vs original Atom Echo | Owned / not yet benchmarked |
| 3 | ESP32-S3-BOX-3 | Owned / not yet benchmarked |
| 4 | Lumi / Waveshare | Ordered / DIY build in progress |
| 5 | FutureProofHomes Satellite1.1 | Ordered / in transit |

Device directories are added only when testing starts and there is verified
material to publish. See [upcoming device resources](resources/upcoming-devices.md)
for verified project links and current preparation notes.

## Start here

- [Comparison and current results](benchmarks/comparison.md)
- [Benchmark methodology](benchmarks/methodology.md)
- [Published series videos](https://youtu.be/kKDNd6tnFzE)

## Affiliate disclosure

Some links in the device and resource pages are marked as affiliate links. If
you purchase through them, Bearded Tinker may earn a small commission at no
additional cost to you. Affiliate URLs are kept separate from official project,
documentation, and firmware links.

## Scope

We publish only our own configurations, changes, measurements, and observations.
For firmware, hardware designs, STL files, and vendor documentation, use the
linked original project and respect its license.

GitHub Issues are for structured technical corrections and reproducible test
results, not general product support. Security reports must use the private
reporting channel described in [SECURITY.md](SECURITY.md).
