# Codex instructions — Bitwig FLkey 37

## Mission
Investigate and build a native-feeling Bitwig Studio integration for the original Novation FLkey 37 (MK1) on Linux. Prefer using the factory firmware and Bitwig's controller API. First investigate hardware and protocol behavior; do not implement a full controller until findings are reviewed.

## Goals
- Transport: play, stop, record, quantize, metronome
- Eight knobs: selected-device remote parameters and banking
- Mixer navigation, volume, pan, sends, mute, solo, arm
- Pads, clip launching, bidirectional LED feedback
- LCD labels and parameter values if supported
- Parameter automation recording in Bitwig

## Discovery workflow
1. Inspect the local Linux distribution, USB devices, MIDI tools and permissions; start with `lsusb` and `aconnect -l`.
2. Enumerate every ALSA MIDI input/output port, distinguishing regular MIDI from any DAW integration port.
3. Research official FLkey documentation and open-source implementations; include URLs and dates in findings.
4. Make repeatable, timestamped MIDI captures. Ask the user for precise physical button-press sequences.
5. Test all relevant ports; absence of output on one port is not evidence a control is inaccessible. Consider host initialization as a hypothesis.
6. Distinguish verified observations, external documentation, and hypotheses.
7. Compare native Bitwig JavaScript and Java controller extensions with an external MIDI translator or hybrid. Prefer the simplest maintainable solution.
8. Propose architecture and obtain review before full implementation.

## Safety
Do not flash firmware, enter bootloader modes, reset the keyboard, or send undocumented SysEx without explicit approval. Do not install packages or change system MIDI configuration without approval. Do not commit secrets or unrelated machine-specific data.

## Deliverables
Maintain `FINDINGS.md` (environment, observations, confidence, experiments), `PROTOCOL.md` (verified messages, ports, prerequisites and evidence), `PLAN.md` (architecture and stages), and `captures/` (diagnostic logs).

## First session
Inspect the attached FLkey and local MIDI environment, record findings, and stop with a precise test sequence when physical button presses are required. Do not start full implementation yet.
