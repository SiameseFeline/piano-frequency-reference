# Piano Frequency Reference & Acoustic Calibration Standards

An open-source acoustic and musical reference detailing the frequencies, MIDI note numbers, acoustic wavelengths, and tuning mathematics for all 88 keys on a standard concert piano.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Standard: ISO 16](https://img.shields.io/badge/Standard-ISO%2016-green.svg)](https://www.iso.org/standard/3601.html)

---

## Overview

In acoustic physics and modern music production, notes are not merely artistic symbols—they represent exact mechanical vibration frequencies. This repository serves as a verified, formulaic reference guide for musicians, audio engineers, acousticians, and developers building musical applications.

### Key References Included
- **[Complete 88-Key Frequency Chart](piano-frequency-chart.md)**: Full table listing note names (A0 to C8), scientific pitch notation, MIDI note numbers, exact frequencies in Hertz (Hz), and physical wavelengths in air.
- **[A440 & Concert Pitch Specification](a440.md)**: Analysis of the ISO 16 international standard, historical pitch drift, and reference calibration.
- **[Equal Temperament Mathematics](equal-temperament.md)**: Derivations of the 12-TET formula, twelfth root of two, cent calculations, and comparison with Just Intonation.

---

## Quick Reference: Core Pitch Benchmarks

| Note | Scientific Notation | MIDI Note | Frequency (Hz) | Description |
|---|---|---|---|---|
| A0 | A₀ | 21 | 27.50 Hz | Lowest key on a standard 88-key piano |
| C1 | C₁ | 24 | 32.70 Hz | Deep contra-octave bass register |
| C4 | C₄ | 60 | 261.63 Hz | Middle C (boundary between bass & treble clefs) |
| **A4** | **A₄** | **69** | **440.00 Hz** | **Concert Pitch standard (ISO 16 / A440)** |
| G5 | G₅ | 79 | 783.99 Hz | High treble register |
| C8 | C₈ | 108 | 4,186.01 Hz | Highest key on a standard 88-key piano |

---

## Mathematical Derivation Formula

Under standard Twelve-Tone Equal Temperament (12-TET) calibrated to A440, the fundamental frequency f(n) for any MIDI note number n in [21, 108] is defined as:

```
f(n) = 440 × 2^((n - 69) / 12)
```

Where:
- 440 is the reference frequency of A4 in Hertz (Hz).
- 69 is the MIDI note number assigned to A4.
- 12 represents the twelve semitones per octave.

### Acoustic Wavelength Calculation
The acoustic wavelength λ in dry air at room temperature (20°C / 68°F, speed of sound c ≈ 343.2 m/s) is calculated as:

```
λ = c / f
```

- **A0 (27.5 Hz)**: λ ≈ 12.48 meters (~ 40.9 feet)
- **A4 (440 Hz)**: λ ≈ 0.78 meters (~ 30.7 inches)
- **C8 (4186 Hz)**: λ ≈ 0.082 meters (~ 3.2 inches)

---

## Live Interactive Demonstrations

For interactive browser demonstrations and auditory reference tone generators:
- For practical pitch testing and instrument calibration by ear, see the [A440 reference guide](https://www.freepianotool.com/a440-guide).
- For individual acoustic profiles, harmonic breakdowns, and frequency conversions of high-treble notes, see the [G5 frequency reference](https://www.freepianotool.com/notes/G5).

---

## License

This reference data and documentation are released under the [MIT License](LICENSE).
