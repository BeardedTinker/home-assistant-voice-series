# Real-World Voice Assistant Comparison Methodology

This method is designed for repeatable Home Assistant demonstrations in a real
home. It supports useful comparisons without claiming laboratory precision.

## Test categories

1. **Setup and integration** — installation, discovery, firmware, controls, and initial configuration.
2. **Wake-word recognition** — reliable and unintended activations.
3. **Voice commands** — Home Assistant actions such as lights and switches.
4. **Information requests** — time, weather, and pipeline-supported questions.
5. **Response latency** — end of the spoken command to the first observable result.
6. **Microphone performance** — documented distances and noise conditions.
7. **Usability** — controls, LEDs, sounds, speaker clarity, and device-specific features.
8. **Reliability** — failures, retries, unexpected behaviour, and limitations.

Only report a category when it was actually tested. Keep optional future tests
separate from completed observations.

## Response timer

- **START:** the end of the spoken user command.
- **STOP:** the first reliably observable result of the requested action.
- For spoken answers, stop at the beginning of the answer.
- A chirp counts only when it reliably coincides with the requested action.
- Failed commands remain failures and receive no estimated latency.

The reusable DaVinci Resolve/Fusion overlay is named **BT Voice Response Timer**.
At 30 fps, frame placement has a resolution of approximately 33 ms.

This measures time to first observable result. It does not isolate wake-word,
STT, intent, conversation-agent, network, action-execution, or TTS latency.

## Fair-comparison rules

- Use equivalent commands and the same Assist pipeline when possible.
- Record Home Assistant, firmware, pipeline, network, room, placement, distance,
  and background-noise differences.
- Keep action-response and speech-response results separate.
- Publish the attempt count; do not select only the fastest success.
- Keep failures and retries in the record.
- Do not claim identical conditions when they cannot be established.
- Do not imply more precision than the source recording provides.

## Suggested sequence

1. Record the environment and software versions.
2. Confirm the same wake word and equivalent pipeline where possible.
3. Run a fixed command list in a fixed order.
4. Mark START and STOP in the 30 fps timeline.
5. Record failures without inventing a latency value.
6. Repeat under each documented distance or noise condition.
7. Publish the attempt table before writing conclusions.
