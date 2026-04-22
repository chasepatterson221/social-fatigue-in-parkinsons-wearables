# Parkinson’s Disease & Social Interaction Patterns (SocialBit Study)

## Overview

This project looks at how Parkinson’s Disease (PD) might affect everyday social interaction. Instead of focusing on clinical symptoms like tremor or rigidity, I’m trying a different approach with the data that can be collected with SocialBit:

**What does social engagement actually look like day-to-day for someone with Parkinson’s?**

To explore this, I’m using data from a SocialBit wearable device. The watch estimates when social interactions happen and tracks basic signals like movement and heart rate. The goal is to see whether interactions tend to be **continuous or broken up throughout the day**, and whether those patterns line up with changes in activity or physiological strain.

This is still an **ongoing project**, and the Parkinson’s dataset is currently being collected.

---

## Research Question

**Are social interactions in a person with Parkinson’s more fragmented throughout the day, and do those patterns change depending on time of day or physical state?**

---

## Why This Project

A lot of Parkinson’s research focuses on motor symptoms. Which is most accurate clinically, but my objective is to see the day-to-day patterns in conversations based on different times and physical states.

Something I found interesting is that conversation itself can be effortful—mentally and physically. So instead of trying to measure Parkinson’s directly, I wanted to look at:

* How often someone engages socially
* How long those interactions last
* Whether they drop off over time

This project is really about **behavior and experience**, not diagnosis.

---

## How I’m Approaching It

### Phase 1 — Baseline (My Data)

Before analyzing Parkinson’s data, I wore the watch myself for about two weeks to get a sense of what “normal” looks like.

This helped me understand:

* What typical heart rate and movement patterns look like
* How noisy the sensors are at rest
* How the device behaves in everyday situations

Here’s a quick summary of my baseline data:

| Metric                      | Value    |
| --------------------------- | -------- |
| Avg Heart Rate              | 94.0 BPM |
| Stationary Noise (Variance) | 0.669    |
| HR / Movement Correlation   | 0.453    |
| AI Confidence               | 38.7%    |

This isn’t meant to be a clinical control—just a reference point so I’m not analyzing the PD data blindly.

---

### Phase 2 — Parkinson’s Data (In Progress)

Right now, I’m collecting about a month of data from a subject with Parkinson’s (my uncle).

The goal is to compare patterns—not to diagnose anything—but to see how daily structure might differ.

---

## What the Watch Actually Measures

It’s important to be clear here: **SocialBit is not a Parkinson’s device.**

It’s mainly designed to estimate:

* When social interactions happen
* How long they last

Along with that, it collects:

* **Heart rate**
* **Movement (accelerometer)**
* **Basic activity state predictions**

So everything I’m doing is built around those signals—not clinical metrics.

---

## How I’m Interpreting the Data

### Social Interaction (Main Focus)

This is the core of the project.

I’m looking at:

* Total interaction time per day
* Number of interaction “blocks”
* Average length of interactions
* Longest continuous interaction
* Gaps between interactions

The main idea is to measure **fragmentation**:

* Are interactions long and continuous?
* Or short and scattered throughout the day?

---

### Heart Rate (`heartRate`)

This is just supporting context.

For example:

* If heart rate is elevated during low movement, it *might* reflect conversation, stress, or cognitive effort

But I’m being careful not to over-interpret this. It’s not a direct measure of fatigue or “speech effort.”

---

### Movement (`accelMagnitude`)

Used to understand how active the person is.

Helps answer:

* Are interactions happening during movement or rest?
* Does activity drop off during the day?

---

### Stationary Variance (`accel_var`)

This shows how much small movement is happening when someone is mostly still.

I initially thought about linking this to tremor, but realistically:

* It’s just a rough signal
* Not a validated measure of Parkinson’s symptoms

So I treat it cautiously.

---

### State Predictions (`prediction`)

These are the watch’s guesses about what state the person is in (active, inactive, etc.).

I mainly use this to:

* Look at how the day is structured
* See if activity happens in long stretches or short bursts

---

## What I’m Actually Trying to Find

Instead of proving something clinical, I’m looking for patterns like:

* Do interactions become shorter later in the day?
* Are there more gaps between interactions over time?
* Does activity level drop before or after social engagement?
* Are there clear “fatigue-like” patterns in behavior (even if not clinically measured)?

---

## Current Status

* Baseline data: complete
* Parkinson’s data: **still being collected**
* Analysis: **ongoing / not finalized**

I haven’t drawn conclusions yet. The goal right now is to explore the data and see what patterns actually show up.

---

## Limitations

There are a few obvious ones:

* Only one Parkinson’s subject (case study)
* No clinical ground truth (fatigue scores, symptom ratings, etc.)
* The device isn’t designed specifically for Parkinson’s
* A lot of interpretation is indirect

Because of that, this project is more **exploratory than definitive**.

---

## Where This Could Go Next

If I were to take this further, I’d want to add:

* Self-reported fatigue or energy levels
* Medication timing (if applicable)
* Speech or voice data
* More participants

That would make the conclusions much stronger.

---

## Final Thought

At the end of the day, this project isn’t about diagnosing Parkinson’s.

It’s about using data to better understand:

> **how the disease might shape everyday social life**

Even if the signals are imperfect, there’s still value in trying to capture that real-world experience.

---
