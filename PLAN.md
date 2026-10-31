# Project plan

## Phase 1: Hardware discovery
Inventory USB and ALSA ports; capture messages for each control across available modes.

## Phase 2: Protocol investigation
Research existing integrations and documentation; test DAW controls, host initialization, LEDs, and LCD. Mark findings by confidence.

## Phase 3: Architecture proposal
Compare native Bitwig JavaScript extension, Java extension, standalone MIDI translator, and hybrid approaches. Prefer native integration when feasible.

## Phase 4: Implementation (after review)
1. Device detection and transport
2. Eight selected-device remote parameters and banking
3. Mixer and track navigation
4. Pads and clip launching
5. LED feedback
6. LCD feedback if possible
7. Automation workflows and regression tests

## Discovery exit criteria
Reproducible port map and captures, accessible-controls matrix, identified unknowns, and a reviewed implementation proposal.
