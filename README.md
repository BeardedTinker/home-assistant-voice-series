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
| MiciMike Home Mini | 5/5 | 5/5 | 5/5 | [Results](devices/micimike-home-mini/README.md) |
| Third Reality Voice & Music Assistant | 5/5 | 5/5 | ~5/10 | [Results](devices/thirdreality-voice-music/README.md) |
| ReSpeaker XVF3800 | 5/5 | 3/10 | 2/10 | [Results](devices/respeaker-xvf3800/README.md) |

Values are successful activations or commands divided by recorded attempts, not
laboratory scores. `~` marks an approximate result reported from the published
material. Conditions and configurations were not necessarily identical; read
[the comparison notes](benchmarks/comparison.md) before drawing conclusions.

## Start here

- [Comparison and current results](benchmarks/comparison.md)
- [Benchmark methodology](benchmarks/methodology.md)
- [Published series videos](https://youtu.be/kKDNd6tnFzE)

## Scope

We publish only our own configurations, changes, measurements, and observations.
For firmware, hardware designs, STL files, and vendor documentation, use the
linked original project and respect its license.

GitHub Issues are for structured technical corrections and reproducible test
results, not general product support. Security reports must use the private
reporting channel described in [SECURITY.md](SECURITY.md).
