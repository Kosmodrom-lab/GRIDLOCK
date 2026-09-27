---> [Gridlock.zip](https://github.com/user-attachments/files/32701239/Gridlock.zip)


# GRIDLOCK INTRO

A native Win32 demoscene intro featuring realtime 3D vector shape-morphing, a software post-processing pipeline, custom bitmap typography, and a 165 BPM Minimal Dark Drum & Bass hybrid audio engine.

Built entirely in **IWBasic 2.5**.

---

##  Visual & Graphics Features

* **3D Anamorphic Morph Engine:** Smooth vertex-interpolated transitions across 9 3D geometry target shapes (Board, Cube, Sphere, Hyperboloid, Möbius Strip, Saddle Shell, Octahedron, Starburst, Torus).
* **Software Rasterizer:** Renders to a 320×240 32-bit DIB section backbuffer (`CreateDIBSection`), stretched to viewport using `StretchBlt`.
* **Software Post-Processing Pass:**
  * **CRT Scanlines:** Interlaced line darkening filter.
  * **Audio-Driven Chromatic Aberration:** RGB channel split triggered on drum hits.
  * **Exposure Flashes:** Bloom bursts on 8-bar section turnarounds.
* **Custom Bitmap Font Blitter:** Gradient-filled 32×24 font rendering with dynamic audio-reactive spring physics.

---

## 🎵 Hybrid Audio Architecture

* **Engine:** Hybrid DirectSound PCM + WinMM General MIDI (`winmm.lib` / `dsound.lib`).
* **Timing:** High-precision multimedia timer thread (`timeSetEvent` set to 10ms resolution at 165 BPM).
* **Style:** Minimal Dark D&B / Noir Jungle (C minor root progression).
  * **Channel 0 (MIDI):** Synth Bass 1 Sub with smooth Eb1/F1 glides and dynamic low-pass filter sweeps (`CC 74`).
  * **Channel 2 (MIDI):** Dark Warm Pad low octave cluster (C2 + G2 + Bb2) with continuous filter modulation.
  * **DirectSound PCM (RAM WAVs):** 16-bit breaks featuring kicks, snares, rim rolls, hats, and dub FX drops.

---

## 🎹 Keyboard Controls

| Key | Function |
| :---: | :--- |
| **`K`** | Toggle Mute Kick Drum |
| **`S`** | Toggle Mute Snare & Rim Rolls |
| **`H`** | Toggle Mute Hi-Hats |
| **`B`** | Toggle Mute Sub-Bass Glides |
| **`D`** | Toggle Mute Low Ambient Drone |
| **`M`** | Toggle Manual / Auto Arranger Mode |
| **`ESC`** | Exit Intro |

---

