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

## Result model

Record the following stages separately for every command attempt when the source
material makes them observable:

1. **Wake detected** — the device reacted to the wake word.
2. **Request end detected** — the device accepted the end of the spoken request
   and moved on to processing.
3. **Recognition and processing** — the transcript or pipeline behaviour showed
   that the request was understood and handled.
4. **Command executed** — the requested action or spoken response completed.

An **end-to-end success** requires all applicable stages to complete. Wake-word
detection alone is not command success. If a stage was not separately recorded,
mark it `N/R` rather than inferring it from another result.

Always publish the actual numerator and denominator. Historical tests used both
five and ten attempts, so do not normalize or silently convert them to a common
sample size. If a run was extended or stopped early, record why.

## Standard 13-group benchmark protocol

### 1. Setup and baseline record

Record the device and hardware revision, firmware, Home Assistant version, wake
word and engine, STT, conversation agent or intent handler, TTS, Assist pipeline,
network, room, placement, speaker settings, and every relevant non-default option.
Unknown values remain explicitly unconfirmed.

### 2. Quiet command at 1 metre

With no intentional background noise, stand approximately 1 m from the device
and use:

> Okay Nabu, turn on the lights.

Record wake detection, request-end detection, command execution, failures, and
response latency for every attempt.

### 3. Quiet command at 3.5 metres

Repeat the same command and scoring procedure at approximately 3.5 m. Keep the
room, device position, speaker direction, pipeline, and target action unchanged.

### 4. Fan interference

Place the fan approximately 1.5 m from the device, facing toward it. Repeat the
same light command. Record the fan model or setting when known, its distance and
orientation, the user-to-device distance, and the actual attempt denominator.

### 5. Competing speech

Play a spoken video on a laptop while issuing the same wake word and command.
Record the laptop position, distance, orientation, playback volume, and source.
Score at least these stages separately:

- whether the wake word activated the device;
- whether the device detected the end of the user's request;
- whether the requested command executed;
- any false activation caused by the competing speaker.

If the laptop position changes, publish each placement as a separate result. Do
not combine close-source and reference-placement attempts into one score.

### 6. Own-music playback

Play **Parni Valjak — Zastave** through the voice device's own speaker. While the
track continues, use the wake word and issue the standard command. Record the
device volume setting and score wake detection and command execution separately.

### 7. False-wake observation

Observe the device for 15 minutes without intentionally speaking its wake word.
Document the background source and conditions, then report the number of
unintended activations. Do not mix deliberate test attempts into this window.

### 8. Second-pipeline information request

Switch to the second test pipeline and use:

> Hey Jarvis, what is the time?

Record activation, request-end detection, whether the answer was correct, and
latency to the beginning of the spoken answer.

### 9. Single-intent command

Run the recorded Sophia NLU single-intent phrase. Store the exact spoken wording,
expected action, actual action, and latency. Do not reconstruct missing wording
after filming.

### 10. Dual-intent command

Issue the recorded two-command phrase as one utterance. Score each requested
action separately and report the overall attempt as successful only when both
actions complete.

### 11. Triple-intent command

Issue the recorded three-command phrase as one utterance. Score all three actions
separately. Use `Partial` when only some actions complete; do not count it as a
full end-to-end success.

### 12. Barge-in

Run two distinct interruption tests:

1. **During processing** — after the device accepts a command and is visibly or
   audibly thinking, say the wake word and issue a new command.
2. **During TTS** — while the device is speaking its response, say the wake word
   and issue a new command.

For each test, record whether the wake word was detected, whether the current
response stopped, whether the new request was accepted, and whether the new
command executed. Interrupting audio without executing the follow-up command is
not a successful barge-in.

### 13. Continued conversation

After a completed response, issue a follow-up request without repeating the wake
word. Record the configured continued-conversation window, whether the follow-up
was accepted, and whether it executed. Test each configured window separately;
for example, 0.5, 5, and 10 seconds must remain distinct results.

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
2. Confirm the same wake words, target action, and equivalent pipelines where possible.
3. Run the 13 protocol groups in order.
4. Keep wake detection, request-end detection, and execution as separate fields.
5. Mark START and STOP in the 30 fps timeline for each timed attempt.
6. Record failures without inventing a latency value.
7. Preserve the actual attempt denominator and every material condition change.
8. Publish the attempt table before writing conclusions.
