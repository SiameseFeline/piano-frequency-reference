# Equal Temperament: Mathematical Derivations and Acoustic Trade-offs

A mathematical and historical reference on **Twelve-Tone Equal Temperament (12-TET)**, the geometric division of the octave, and cent logarithmic measurement.

---

## 1. The Mathematical Axiom

The human auditory system perceives musical intervals based on **frequency ratios** rather than linear differences. The most consonant interval in nature is the **octave**, where the higher pitch vibrates at exactly twice the frequency of the lower pitch:

```
Octave Ratio = f2 / f1 = 2.0
```

To divide this 2:1 octave into 12 acoustically identical semitones such that each step represents the exact same perceptual musical distance, each step must multiply frequency by a constant ratio r:

```
r^12 = 2  =>  r = 2^(1/12) ≈ 1.059463094359
```

Every semitone step on a modern piano increases the fundamental frequency by approximately **5.946%**.

---

## 2. Deriving Note Frequencies from MIDI Numbers

In digital audio protocols (MIDI), notes are indexed sequentially from 0 to 127:
- Standard Concert A (A4) is assigned index **69**.
- Middle C (C4) is assigned index **60**.
- The lowest piano key (A0) is index **21**.
- The highest piano key (C8) is index **108**.

Given a reference pitch f0 = 440 Hz at MIDI note m0 = 69, the fundamental frequency f(m) for any MIDI note m is:

```
f(m) = 440 × 2^((m - 69) / 12)
```

### Example Calculation: Note G5
For **G5** (the G note in the fifth octave):
- MIDI Note Number m = 79
- Distance from A4: 79 - 69 = 10 semitones
- f(79) = 440 × 2^(10/12) = 440 × 1.781797 ≈ 783.99087 Hz

For a practical breakdown of how this frequency behaves in high-register treble instruments, explore the [G5 frequency reference](https://www.freepianotool.com/notes/G5).

---

## 3. Logarithmic Pitch Measurement: Cents

Because human pitch perception is logarithmic, acousticians use **cents** to measure tiny pitch deviations:
- An octave is defined as exactly **1,200 cents**.
- Each equal-tempered semitone is defined as exactly **100 cents**.

The difference in cents c between any two frequencies f1 and f2 is:

```
c = 1200 × log2(f2 / f1) ≈ 3986.31 × log10(f2 / f1)
```

---

## 4. The Historical Trade-Off: 12-TET vs. Just Intonation

Why did equal temperament replace earlier tuning systems like Pythagorean or Just Intonation?

- **Just Intonation**: Based on pure integer ratios derived from the overtone series (e.g., Major 3rd = 5:4 = 1.250; Perfect 5th = 3:2 = 1.500). In a single key, chords sound pure and free of acoustic beating. However, modulating to distant keys produces intolerable dissonance ("wolf fifths").
- **12-TET Compromise**: By slightly mistuning intervals (the equal-tempered 5th is 1.96 cents flat; the equal-tempered major 3rd is 13.69 cents sharp), 12-TET allows an instrument to play in all 24 major and minor keys with identical, acceptable intonation.
