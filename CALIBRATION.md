# Normalizer Pro 1.9 — Calibration Report

**55 of 55 checks passed** · verified 27 November 2026 on macOS 15.7.7 (Apple silicon).

Every Normalizer Pro release is checked automatically before it is published. Reference signals
with known correct answers are processed by the release build, and each result is compared with
the known answer, with the values Normalizer Pro writes in its own report, and with two reference
loudness meters developed independently of Normalizer Pro and of each other.

## Standards

- Integrated loudness: ITU-R BS.1770-4 (K-weighting, 400 ms blocks with 75% overlap, −70 LUFS absolute
  and −10 LU relative gates), as used by EBU R128 and the major streaming platforms.
- True peak: ITU-R BS.1770-4 Annex 2 (4× oversampling, so peaks between samples are included).
- Short samples: a sample shorter than 3 seconds is measured as if followed by silence up to 3 seconds,
  so even a 50 ms drum hit gets a stable, standards-based reading.

## Results

| Area | What is verified | Check | Reference | Normalizer Pro report | Reference meters | Result |
|---|---|---|---|---:|---:|:---:|
| Loudness target | A calibrated 997 Hz tone at −30 dBFS, normalised to −16 LUFS. | Input loudness | -33.01 LUFS ± 0.15 | -33.01 | -33.03 | ✅ |
|  |  | Input sample peak | -30 dBFS ± 0.05 | -30.00 | -30.00 | ✅ |
|  |  | Input rms | -33.01 dB ± 0.05 | -33.01 | -33.01 | ✅ |
|  |  | Output loudness | -16 LUFS ± 0.15 | -16.00 | -16.02 | ✅ |
|  |  | Output sample peak | -12.99 dBFS ± 0.05 | -12.99 | -12.99 | ✅ |
|  |  | Output bit depth | 24 bit | – | 24 | ✅ |
|  |  | Output length | same as input ± 0.5 | 4000.00 | 4000.00 | ✅ |
| True-peak ceiling | A drum hit normalised to −14 LUFS: it reaches the target or is held at the −1 dBTP ceiling, never above. | Output loudness | -14 LUFS, or TP at -1 dBTP | -18.12 | -18.13 | ✅ |
|  |  | Output true peak | ≤ -0.95 dBTP | -1.020 | -1.007 | ✅ |
|  |  | Output hit starts at | same as input ± 0.3 | – | 0.021 | ✅ |
| Very short samples | A 200 ms one-shot, shorter than one loudness measurement block, normalised to −16 LUFS. | Output loudness | -16 LUFS ± 0.15 | -16.00 | -16.02 | ✅ |
|  |  | Output length | 200 ms ± 0.5 | 200.00 | 200.00 | ✅ |
| Leading-silence trim | A drum hit after 100 ms of silence: exactly the silence is removed. | Input hit starts at | 99.9 to 100.2 ms | – | 100.02 | ✅ |
|  |  | Output length | input − 100 ms ± 0.5 | 300.00 | 300.00 | ✅ |
|  |  | Output hit starts at | ≤ 1 ms | – | 0.021 | ✅ |
| Timing with tone shaping | With trimming and low-end shaping on, the processed hit starts within 1.5 ms. | Output hit starts at | ≤ 1.5 ms | – | 0.000 | ✅ |
| Peak control | A spiky drum hit brought to −20 LUFS while its true peak stays at or below −1 dBTP. | Output true peak | ≤ -0.95 dBTP | -1.020 | -1.007 | ✅ |
|  |  | Output loudness | -20 LUFS ± 0.15 | -20.02 | -20.03 | ✅ |
|  |  | Output hit starts at | same as input ± 0.3 | – | 0.062 | ✅ |
| 16-bit export | 16-bit output with dither: correct format and loudness. | Output bit depth | 16 bit | – | 16 | ✅ |
|  |  | Output loudness | -16 LUFS ± 0.15 | -16.00 | -16.02 | ✅ |
| Envelope accuracy | A 5 ms linear fade-in and fade-out: silent ends, and 55% level 2.75 ms in. | Output first sample | ≤ 0.0005 | – | 0.000 | ✅ |
|  |  | Output last sample | ≤ 0.002 | – | 0.000 | ✅ |
|  |  | Output level 2.75 ms in | 0.55 x ± 0.02 | – | 0.550 | ✅ |
| Musical length | An 80 ms hit fitted to a 1/16 note at 120 BPM (125 ms). | Output length | 125 ms ± 0.5 | 125.00 | 125.00 | ✅ |
| Tail-silence trim | 500 ms of trailing silence removed. | Input length | 800 ms ± 0.5 | 800.00 | 800.00 | ✅ |
|  |  | Output length | ≤ 305 ms | 295.00 | 295.00 | ✅ |
| Polarity alignment | An inverted drum hit is returned the right way up. | Input polarity (+1 = up) | -1 | – | -1 | ✅ |
|  |  | Output polarity (+1 = up) | 1 | – | 1 | ✅ |
| Stereo and sample-rate conversion | Stereo 44.1 kHz 24-bit export: format, loudness and length. | Output sample rate | 44100 Hz | – | 44100 | ✅ |
|  |  | Output channels | 2 | 2 | 2 | ✅ |
|  |  | Output bit depth | 24 bit | – | 24 | ✅ |
|  |  | Output loudness | -16 LUFS, or TP at -1 dBTP | -16.00 | -16.02 | ✅ |
|  |  | Output length | same as input ± 0.5 | 1000.00 | 1000.00 | ✅ |
| Tuning | A tone 47 cents sharp of A4 is tuned to 440 Hz. | Input pitch | 452 Hz ± 0.5 | – | 452.00 | ✅ |
|  |  | Output pitch | 440 Hz ± 0.5 | – | 440.00 | ✅ |
| Filtering | A 500 Hz, 24 dB/octave high-pass leaves 40 Hz hum at least 50 dB below a 2 kHz tone. | Input 40 hz vs 2 khz | 0 dB ± 3 | – | 0.000 | ✅ |
|  |  | Output 40 hz vs 2 khz | ≤ -50 dB | – | -87.88 | ✅ |
| Effect plugins: targets | A drum hit through an effect plugin still lands on −16 LUFS under the −1 dBTP ceiling, and its hit does not move. | Output loudness | -16 LUFS, or TP at -1 dBTP | -18.39 | -18.41 | ✅ |
|  |  | Output true peak | ≤ -0.95 dBTP | -1.020 | -1.007 | ✅ |
|  |  | Output hit starts at | same as input ± 0.3 | – | 0.021 | ✅ |
| Effect plugins: set length | A delay's echo is kept, but never runs past a 250 ms set length. | Output length | 150 to 250 ms | 200.08 | 200.08 | ✅ |
|  |  | Output hit starts at | same as input ± 0.3 | – | 0.021 | ✅ |
| Effect plugins: tail limit | With no set length, an effect's tail stops at the 250 ms tail limit. | Output length | 280 to 350 ms | 300.08 | 300.08 | ✅ |
|  |  | Output hit starts at | same as input ± 0.3 | – | 0.021 | ✅ |
| Major / minor | A minor chord stab (A, C, E over an A bass) is reported as A minor. | Output major / minor | A minor | A minor | – | ✅ |
| Major / minor | An open C major voicing over three octaves is reported as C major. | Output major / minor | C major | C major | – | ✅ |
| Major / minor: tuning | An F minor chord tuned 30 cents sharp is still reported as F minor. | Output major / minor | F minor | F minor | – | ✅ |
| Major / minor: single notes | One pitched 808-style note is reported as a single note, not given a guessed mode. | Output major / minor | single note | single note | – | ✅ |
| Major / minor: unpitched | A noise burst like a hi-hat is reported as unpitched. | Output major / minor | unpitched | unpitched | – | ✅ |
| Effect plugins: no tail | With the tail limit set to none, a file through a delay plugin is exactly as long as the original, and ends without a click. | Output length | same as input ± 0.5 | 100.00 | 100.00 | ✅ |
|  |  | Output hit starts at | same as input ± 0.3 | – | 0.021 | ✅ |
|  |  | Output last sample | ≤ 0.001 | – | 0.000 | ✅ |
| Clean cuts | A tone cut to a 125 ms set length is exactly 125 ms long and ends on silence, with no click. | Output length | 125 ms ± 0.5 | 125.00 | 125.00 | ✅ |
|  |  | Output last sample | ≤ 0.001 | – | 0.000 | ✅ |

## Agreement with the reference meters

Largest difference between the value Normalizer Pro reports and either reference meter, over every
test file before and after processing:

| Measurement | Largest difference | Tolerance |
|---|---:|---:|
| Integrated loudness | 0.05 LU | 0.15 LU |
| True peak | 0.12 dB | 0.25 dB |
| Sample peak | 0.005 dB | 0.05 dB |

The reference meters print loudness to 0.1 LU in some cases, which the loudness tolerance allows for.

## Major / minor detection

Normalizer Pro reports whether each sample is major or minor, with a confidence score from 0 to 1.
A sample with only one pitch in it (most kicks, 808s and subs) is reported as a single note, because
one pitch on its own is neither major nor minor. The cases marked “Major / minor” above are checked on
every release. The detector was also measured on larger sets of synthetic test material with known
answers:

| Test material | What it contains | Keys correct | Single notes correct |
|---|---|---:|---:|
| Clean chords | Major and minor chords in all 12 keys and every inversion, sevenths, ninths, scales, single notes and drum sounds | 357 of 360 | 204 of 204 |
| Difficult conditions | The same chords with background noise, reverb, or a kick drum underneath | 118 of 120 | 36 of 36 |
| Unseen material | Chords and notes with random voicings, levels, tones, tuning (up to ±40 cents) and effects, never used while developing the detector | about 73% | about 94% |

On unseen material, plain major and minor chords were right about 85% of the time. Seventh chords
score lower because many genuinely fit two keys: C minor 7 contains a complete E♭ major chord.

The confidence score shows how far to trust each answer:

| Confidence | Answers correct |
|---|---:|
| 0.80 or above | 99% |
| 0.50 to 0.80 | 91% |
| 0.30 to 0.50 | 86% |
| below 0.30 | about 60% |

Below 0.30, treat the answer as “listen to this one” rather than a firm result.

## Check your own copy

Choose **Help ▸ Check Calibration…** in Normalizer Pro. It runs reference signals through the app on
your Mac in a few seconds and confirms that the meter, the processing and the reports agree.
