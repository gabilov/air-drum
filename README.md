# Air Drum 🥁

**Turn your phone into a drumstick.** Swing it through the air, and the drum sound comes from the screen.

Air Drum is a single-page web app that runs in your phone's browser and is played with your body. It uses the phone's motion sensors to turn a physical swing into a drum hit, so you play it as a gesture instead of by tapping the screen.

## How it works
- **Motion input:** reads `DeviceMotionEvent` / `DeviceOrientationEvent` to detect a swing, with an adjustable hit threshold
- **Sound:** drum sounds are generated live with the Web Audio API (no audio files)
- **Feedback:** each hit shows a visual flash, and phones that support it also vibrate
- **Re-center:** one button resets the phone's resting position

## Modes
| Mode | What it does |
|---|---|
| Free play | Swing and play |
| Demo | The app plays a pattern by itself while you watch |
| Play along | Play together with a pattern |
| Looper | Record a loop, play it back, add a metronome, quantize, set the BPM |

## Try it
1. Open `index.html` on a phone. It has to be served over HTTPS so the browser allows sensor access.
2. On iPhone, turn off silent mode and tap **Allow** when it asks for motion access.
3. Tap **Başla** (Start) and swing.

The interface is in Azerbaijani.

## Design notes
- **Embodied interaction:** the gesture *is* the input, which mirrors how a real drumstick works.
- **Sensor permission:** iOS asks for motion access only after a user gesture, so the app waits for the Start tap.
- **Light and dark themes:** follow the system setting (`prefers-color-scheme`).
- **Mobile layout:** respects iPhone safe areas.

## Built with
HTML · CSS · JavaScript · Web Audio API · Device Motion API

Designed by Kanan Gabilov. The code was written with help from an AI assistant (Claude).
