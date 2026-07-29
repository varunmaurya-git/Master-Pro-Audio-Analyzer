# 🎛️ Master Pro Audio Analyzer Suite

[![Live Application](https://img.shields.io/badge/Live%20App-Click%20Here-00f3ff?style=for-the-badge&logo=googlechrome&logoColor=black)](https://varunmaurya-git.github.io/Master-Pro-Audio-Analyzer/)
[![License: MIT](https://img.shields.io/badge/License-MIT-22c55e?style=for-the-badge)](LICENSE)
[![Vanilla JS](https://img.shields.io/badge/Language-Vanilla%20JS-f7df1e?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Privacy](https://img.shields.io/badge/Privacy-100%25%20Client--Side-9d72ff?style=for-the-badge)](#-100-client-side-privacy)

# Quick Access it from below link 
# https://varunmaurya-git.github.io/Master-Pro-Audio-Analyzer/

A full-fledged, zero-dependency, professional-grade real-time audio analysis application that operates 100% inside your web browser. Built with low-level **Vanilla JavaScript**, **Web Audio API**, **Canvas 2D**, and multi-threaded **Web Workers**.

---

### 👤 Created By
**VARUN MAURYA**  
[![LinkedIn Profile](https://img.shields.io/badge/LinkedIn-Connect%20with%20Varun-0A66C2?style=flat&logo=linkedin)](https://www.linkedin.com/in/maurya-varun)

---

### 🚀 Key Features

* **📊 Interactive Ultra-HD Spectrogram (8192-Point FFT)**
  * **8192-Point FFT Resolution:** Generates 4,096 vertical frequency bins with 5.38 Hz/bin precision for deep sub-bass, midrange, and high-frequency overtone separation.
  * **Blackman-Harris Windowing:** Employs 4-term Blackman-Harris windowing (-92 dB side-lobe suppression) to eliminate spectral leakage and fuzzy frequency smearing.
  * **Bilinear Anti-Aliased Engine:** Renders up to 16,000 high-density time columns with smooth, crisp, unpixelated clarity—even at maximum 64x horizontal zoom.
  * **Interactive Inspection:** Hover crosshairs provide instant readout of exact Frequency (Hz), Signal Level (dBFS), and Timestamp.
  * **Perceptual Scales & Gain:** Toggle between Mel Scale (perceptual pitch tuning) and Linear Scale, with variable gain boost controls (0.5x to 3.5x).

* **📈 Logarithmic Spectrum Analyzer (RTA) & PEAK dBFS Meter**
  * **Calibrated 0 dBFS to -90 dBFS Scale:** Features a uniform linear 6 dB step grid across the entire vertical dynamic range.
  * **Shared Middle dB Scale Axis:** A single, centered dB scale column sitting between the RTA graph and Peak Meter, serving both modules simultaneously.
  * **Pro RTA Display Boost:** Selectable display boost (+0 dB, +6 dB, +12 dB Default, +18 dB) matching FabFilter Pro-Q & Voxengo SPAN industry standards.
  * **Peak-Bin Aggregation & Ballistics:** Smooth temporal decay with peak max-pooling so no fast harmonic spikes are missed.
  * **Dedicated Peak Level Meter:** Fully labeled PEAK dBFS meter featuring white peak-hold lines and a 1:1 matched bottom readout container showing L (Cyan) and R (Magenta) numerical dB values.

* **🎛️ Goniometer & Phase Scope**
  * Real-time 2D soundfield Lissajous scatter plot.
  * Live Phase Correlation Meter (Φ) ranging from -1 (anti-phase) to +1 (perfect in-phase).
  * **Dual Scope Views:** Switch between Raw Track View (unfiltered audio file) and Post Mono ON Routing View (monitored signal that collapses visually into a straight vertical line in mono mode).

* **⚡ Stereo Width & Phase Waveform Overview**
  * Whole-track amplitude overview with color-coded stereo health indicators:
    * 🟢 **Green:** In-Phase / Safe Stereo
    * 🟡 **Yellow:** Wide Stereo
    * 🔴 **Red:** Anti-Phase (High risk of mono cancellation)
  * Up to 25x horizontal zoom with playhead center-lock seeking.

* **🔀 Channel Routing & Auditioning**
  * **Stereo:** Standard dual-channel playback.
  * **Left Only / Right Only:** Isolate individual stereo channels.
  * **Mono: ON:** Sums stereo audio into true mono (L + R) / 2 to test mono-compatibility.

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
