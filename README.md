# 🎛️ Master Pro Audio Analyzer Suite

[![Live Application](https://img.shields.io/badge/Live%20App-Click%20Here-00f3ff?style=for-the-badge&logo=googlechrome&logoColor=black)](https://varunmaurya-git.github.io/Master-Pro-Audio-Analyzer/)
[![License: MIT](https://img.shields.io/badge/License-MIT-22c55e?style=for-the-badge)](LICENSE)
[![Vanilla JS](https://img.shields.io/badge/Language-Vanilla%20JS-f7df1e?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Privacy](https://img.shields.io/badge/Privacy-100%25%20Client--Side-9d72ff?style=for-the-badge)](#-100-client-side-privacy)

A full-fledged, zero-dependency, professional-grade real-time audio analysis application that operates 100% inside your web browser. Built with low-level **Vanilla JavaScript**, **Web Audio API**, **Canvas 2D**, and multi-threaded **Web Workers**.

---

### 👤 Created By
**VARUN MAURYA**  
[![LinkedIn Profile](https://img.shields.io/badge/LinkedIn-Connect%20with%20Varun-0A66C2?style=flat&logo=linkedin)](https://www.linkedin.com/in/maurya-varun)

---

## 🚀 Key Features

* **📊 Interactive HD Spectrogram (4096-Point FFT):**
  * Dual-channel (Left / Right) spectral visualization.
  * Powered by a **2D Catmull-Rom Bicubic Surface Interpolation Engine** (16-point spatial matrix filtering).
  * Toggle between **Mel Scale** (perceptual pitch tuning) and **Linear Scale**.
  * Up to **64x Horizontal Time Zoom** with interactive crosshair frequency and timestamp inspection.
  * Variable gain boost controls (0.5x to 3.5x).

* **🎛️ Goniometer & Phase Scope:**
  * Real-time 2D soundfield Lissajous scatter plot.
  * Live **Phase Correlation Meter ($\Phi$)** ranging from -1 (out-of-phase) to +1 (perfect in-phase).
  * **Dual Scope Views:** Switch between **Raw Track View** (unfiltered track stereo) and **Post Mono ON Routing View** (auditioned output signal).

* **📈 Logarithmic Spectrum Analyzer (RTA):**
  * Real-time frequency response curves for Left (Cyan) and Right (Magenta) channels.
  * Logarithmic frequency grid with dynamic dB level markers (0 dB to -72 dB).
  * Quick-select band presets (**Full Range**, **Bass**, **Mids**, **Highs**).
  * Isolated single-channel tracking when **Left Only** or **Right Only** is selected.

* **⚡ Stereo Width & Phase Waveform Overview:**
  * Whole-track amplitude overview with color-coded stereo health indicators:
    * 🟢 **Green:** In-Phase / Safe Stereo
    * 🟡 **Yellow:** Wide Stereo
    * 🔴 **Red:** Anti-Phase (High risk of mono cancellation)
  * Up to 25x horizontal zoom with playhead center-lock seeking.

* **🔀 Channel Routing & Auditioning:**
  * **Stereo:** Standard dual-channel playback.
  * **Left Only / Right Only:** Isolate individual stereo channels.
  * **Mono: ON:** Sums stereo audio into true mono `(L + R) / 2` to test mono-compatibility.

---

## 🔒 100% Client-Side Privacy

Your audio files are **never uploaded to any server or cloud database**. 

All audio decoding, Web Worker Fast Fourier Transform (FFT) signal processing, and canvas rendering happen locally on your device's CPU/GPU. Your unreleased tracks and confidential masters remain 100% private and secure on your computer.

---

## ⚙️ Technical Architecture & DSP Highlights

* **Zero External Dependencies:** Built completely without third-party frameworks, chart libraries, or UI kits.
* **Multi-Threaded FFT Processing:** Heavy 4096-point Radix-2 Fast Fourier Transforms run off the main thread inside **Web Workers**, keeping the UI responsive at steady high frame rates.
* **Zero-Allocation Memory Management:** Re-uses array buffers across animation frames to eliminate Garbage Collection (GC) latency spikes.
* **Full-Page Drag & Drop:** Native HTML5 Drag and Drop event handling for instantaneous file loading.

---

## 💻 How to Use

1. Open the [Live Web Application](https://varunmaurya-git.github.io/Master-Pro-Audio-Analyzer/).
2. Click **Choose File** or simply **Drag & Drop** any audio file (`.mp3`, `.wav`, `.flac`, `.ogg`, `.aac`) anywhere on the screen.
3. Press **Spacebar** or click **Play** to start playback and real-time visualization.

---

## 🌐 Browser Compatibility

Tested and supported across all modern evergreen desktop browsers:
* ✅ Google Chrome
* ✅ Mozilla Firefox
* ✅ Opera / Opera GX
* ✅ Microsoft Edge
* ✅ Apple Safari

---

## 📜 License

Distributed under the **MIT License**. Free for personal, commercial, and educational use.  
See `LICENSE` for more information.
