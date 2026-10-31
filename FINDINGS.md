# Hardware discovery findings

## Environment
- Linux distribution / kernel:
- Bitwig version:
- FLkey firmware version (if known):
- USB vendor/product IDs:
- ALSA MIDI ports (input/output):
- Applications occupying ports:

## Verified observations
_None yet._

## Hypotheses
- The DAW port carries additional controls.
- Some controls require host initialization.
- LCD or LEDs may support host feedback.

## Research references
_Add URLs, dates, and exact claims._

## Next experiments
1. Enumerate USB and ALSA MIDI ports.
2. Monitor every relevant input port while testing a repeatable sequence of controls.
3. Record port, mode, timestamps, and raw MIDI messages.
4. Investigate initialization only after non-invasive capture.
