![West 9 Studios — Normalizer Pro](Screenshots/header.png)

# Normalizer Pro

**Prepare a whole folder of samples in one pass.** Normalizer Pro is a free macOS app from West 9 Studios that cleans up, aligns and loudness-normalises drum and sample libraries, then shows you exactly what it did to every file.

[**Download Normalizer Pro 1.7**](https://github.com/west9studios/Normalizer-Pro-Releases/releases/latest) · macOS 13 or later · 133.5 MB · Free, no account or licence key

## What it does

![Normalizer Pro processing workspace](Screenshots/process.png)

Drop in files or folders, choose your settings, and process the queue. Your original files are never changed; results go into a separate output folder with a full report.

- **Loudness and true-peak control:** normalise every file to a LUFS target without exceeding a true-peak ceiling, checked after rendering. An optional lookahead limiter lets peaky kicks reach the target cleanly.
- **Fast:** several files are processed at once, so large folders finish quickly. Runs natively on Apple silicon and Intel Macs.
- **Cleanup and alignment:** trim leading and trailing silence, align polarity, convert to mono safely, balance stereo and tidy starts and ends.
- **Filtering and tone:** material profiles, high-pass and low-pass filters with selectable slopes, and Body Boost for low-end weight.
- **Pitch and key:** detect the pitch of tonal samples, tune them, and write the note into the filename.
- **Defect scan and repair:** find clicks and clipping on import and repair only the files you choose. Switch it off or set its sensitivity at any time.
- **Musical timing:** set a tempo and grid, trim to length, and stretch short samples while protecting the attack.
- **Attack and decay envelopes:** click-safe, muted or natural fades with a choice of curves, including extreme whipped and ramped shapes.
- **Audition before you commit:** compare Before and After with the arrow keys, and hear a filter on your samples before processing.
- **Reports:** a clear report page for every output folder (before-and-after loudness, true peak, settings used, defect scan results), a detailed spreadsheet for every file, and a folder length recommendation.
- **Built-in Help Center and one-click updates:** a searchable manual and Learn guides are included, and the app tells you when a new version is available and installs it for you.

## See it in action

<table>
  <tr>
    <td width="50%"><img src="Screenshots/repair.png" alt="Normalizer Pro defect detection and repair" /></td>
    <td width="50%"><img src="Screenshots/shape.png" alt="Normalizer Pro musical envelope shaping" /></td>
  </tr>
  <tr>
    <td align="center"><sub>Defect diagnostics and repair</sub></td>
    <td align="center"><sub>Musical envelope shaping</sub></td>
  </tr>
</table>

## What's new

- Much faster batches: each file is now read once and finished in one go, and several files are processed at the same time (Parallel workers, up to 8). Large folders of kicks finish many times sooner and leave your Mac more breathing room.
- The window stays smooth while a batch runs and with very large folders: the queue no longer redraws for every finished file.
- Fixed: Body Boost added about 10 ms of near-silence at the start of every file. Samples now start exactly on their first sample again.
- More accurate loudness for short samples: very short hits now land on your LUFS target instead of up to a few dB away.
- 16-bit exports work again with triangular dither on, and the dither is now applied properly.
- Optional lookahead limiter: peaky kicks that used to stay below target because of the true-peak ceiling can now reach it, cleanly and with no delay at the start.
- Clip spikes no longer adds harsh high-frequency grit.
- Attack and decay curves keep the curve you chose when you load a preset or change the fade length.
- A damaged file that stops responding is skipped after two minutes instead of stalling the whole batch.
- New processing report: a clear web page for each output folder with a summary, the settings used, every file’s before-and-after numbers and the length recommendation. Open it with the new Open Report button.
- The report now records what the defect scan found for each file, even after it has been repaired, and files with too many clicks to be real defects are marked unreliable.
- Runs natively on both Apple silicon and Intel Macs.

The full history is in the app under **Help > What's New**.

## Install

1. Download the DMG from the [latest release](https://github.com/west9studios/Normalizer-Pro-Releases/releases/latest).
2. Open it and drag **Normalizer Pro** into **Applications**.
3. Launch the app. If macOS blocks the first launch, open **System Settings > Privacy & Security** and choose **Open Anyway**.

Once installed, Normalizer Pro checks for new versions when it starts. Choose **Update & Relaunch** when the orange notice appears and the app updates itself. Each release also publishes a `.sha256` file if you want to verify your download.

Version 1.7 was released on 14 November 2026. DMG SHA-256: `28e121526ebee0ed9b78ea71b20884377cc0e32d721ada41b113b7190b91ff25`

## Licence

NORMALIZER PRO — PLAIN-LANGUAGE LICENCE NOTICE

Normalizer Pro is free to use. It remains the property of West 9 Studios.

You may not redistribute, resell, modify, or reverse-engineer Normalizer Pro, or
claim it as your own. No licence key or payment is required to use the app.

Normalizer Pro is provided “as is”, without any warranty, express or implied.
West 9 Studios is not responsible for loss or damage arising from its use.

This is a plain-language notice, not legal advice. It does not replace any
rights or obligations that may apply under the law.
