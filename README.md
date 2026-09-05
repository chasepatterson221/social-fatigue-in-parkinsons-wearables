# Parkinson’s Disease & Social Interaction Patterns (SocialBit Study)

## Overview

This project explored how **Parkinson’s disease might affect everyday social interaction patterns** using wearable sensor data.

Instead of focusing directly on clinical symptoms such as tremor or rigidity, I wanted to examine a different aspect of day-to-day experience:

> **What does social engagement actually look like throughout the day for someone with Parkinson’s disease?**

I used data from a **SocialBit wearable**, which estimates social interactions while also collecting signals such as heart rate, movement, and activity state.

The original goal was to determine whether social interactions appeared **continuous or fragmented throughout the day**, and whether those patterns were associated with changes in activity or physiological measurements.

The project ultimately became an exploration of both **behavioral patterns and the challenges of working with real-world wearable data**.

---

## Research Question

**Are social interactions in a person with Parkinson’s more fragmented throughout the day, and do those patterns change depending on time of day or physical state?**

This was treated as an exploratory question rather than a clinical hypothesis.

---

## Why This Project

Much of Parkinson’s research focuses on clinical and motor symptoms. I wanted to explore a more everyday aspect of the condition: **how social interaction may vary throughout the day**.

Conversation and social engagement can involve both physical and cognitive effort, so I was interested in examining:

* How often someone engages socially
* How long those interactions last
* Whether interactions become shorter or more fragmented
* How social interaction relates to movement and heart rate
* Whether patterns differ across the day

The project was intended to study **behavior and daily experience**, not diagnose Parkinson’s disease.

---

## How I Approached It

### Phase 1 — Baseline: My Data

Before analyzing Parkinson’s data, I wore the SocialBit watch myself for approximately two weeks.

The purpose was to establish a personal baseline and understand how the device behaved in normal everyday conditions.

This helped me examine:

* Typical heart rate and movement patterns
* Sensor noise during relatively stationary periods
* Relationships between movement and heart rate
* How the device represented activity states
* The overall structure and quality of the exported data

### Baseline Results

| Metric                      |    Value |
| --------------------------- | -------: |
| Average Heart Rate          | 94.0 BPM |
| Stationary Noise (Variance) |    0.669 |
| HR / Movement Correlation   |    0.453 |
| AI Confidence               |    38.7% |

This baseline was **not intended to function as a clinical control**. It was primarily a way to understand the measurement system before working with Parkinson’s data.

---

### Phase 2 — Parkinson’s Data

I then collected approximately **one month of wearable data from a participant with Parkinson’s disease**.

The initial analysis focused on comparing daily patterns in:

* Social interaction
* Heart rate
* Movement
* Activity/state predictions
* Time-of-day behavior

The objective was to identify potentially interesting patterns rather than make a clinical diagnosis or claim a causal relationship.

---

## What the Watch Actually Measures

An important limitation is that **SocialBit was not specifically designed for Parkinson’s patients**.

The device is primarily designed to estimate social interactions and provides additional sensor information including:

* **Social interaction estimates**
* **Heart rate**
* **Movement / accelerometer data**
* **Activity state predictions**

Because these measurements were not designed to directly measure Parkinson’s symptoms, I treated them as **behavioral and physiological context rather than clinical measurements**.

---

## How I Interpreted the Data

### Social Interaction

Social interaction was the primary focus of the project.

I examined:

* Total interaction time per day
* Number of interaction blocks
* Average interaction duration
* Longest continuous interaction
* Gaps between interactions

The main concept was **interaction fragmentation**.

I was interested in whether social engagement tended to occur as:

**Longer, continuous interactions**

versus

**Shorter interactions separated by longer gaps**

---

### Heart Rate (`heartRate`)

Heart rate was used as a supporting signal.

For example, elevated heart rate during relatively low movement could occur during conversation, stress, cognitive effort, or other situations.

However, the data could not distinguish between these possibilities.

Therefore, heart rate was **not treated as a direct measure of social effort, cognitive effort, or fatigue**.

---

### Movement (`accelMagnitude`)

Movement data were used to provide physical context around social interaction.

This allowed me to examine questions such as:

* Are interactions occurring while the participant is moving or stationary?
* Does activity appear to change around social interactions?
* Does overall movement vary throughout the day?

---

### Stationary Variance (`accel_var`)

I also examined small movement variability during relatively stationary periods.

I initially considered whether this could provide information related to Parkinsonian tremor.

However, this signal was **not validated as a measure of tremor or Parkinson’s severity**, so I treated it only as a descriptive sensor measurement.

---

### State Predictions (`prediction`)

The wearable also produced predictions about the participant's activity state.

I used these primarily to understand **how activity was distributed throughout the day**, rather than treating the predictions as clinical classifications.

---

## Data Quality & Missing Data

One of the most significant issues emerged during the analysis: **large portions of the Parkinson’s dataset were missing**.

On some days, approximately **4–6 hours of data were absent**, particularly during the middle-to-later portions of the day.

I examined the available files and data structure to determine why these gaps occurred.

However, I could not establish with enough confidence whether the missing periods were caused by:

* Device non-wear
* Recording interruptions
* Synchronization or export problems
* Another source of missingness

This distinction mattered because the missing periods could not simply be interpreted as periods with **zero social interaction or zero activity**.

For example, if fewer interactions appeared later in the day, that could represent an actual behavioral change — or it could simply reflect missing observations during that period.

Because the underlying reason for the missingness could not be established reliably, I decided **not to use those gaps to make strong conclusions about time-of-day behavior**.

---

## What I Was Able to Analyze

Despite the missing data, the available dataset still allowed me to explore:

* The structure of wearable-derived social interaction data
* Interaction duration and fragmentation
* Heart-rate patterns
* Movement patterns
* Relationships between movement and heart rate
* Activity-state predictions
* Sensor variability
* The practical challenges of working with continuously collected wearable data

The baseline dataset also provided a useful reference for understanding how the wearable behaved under normal conditions.

However, the incomplete Parkinson’s dataset meant that some of the original questions — particularly questions involving **full-day or time-of-day trends** — could not be answered reliably.

---

## Limitations

There were several important limitations:

* **Single-participant case study:** The Parkinson’s dataset represented one participant and cannot support population-level conclusions.
* **Incomplete daily coverage:** Several hours of data were missing on some days.
* **Uncertain missingness mechanism:** The available information was insufficient to confidently determine why the gaps occurred.
* **Device mismatch:** SocialBit was not specifically designed for Parkinson’s monitoring.
* **No clinical ground truth:** There were no validated fatigue scores, symptom scales, or clinical measurements to compare against the wearable data.
* **Indirect measurements:** Heart rate, movement, and social interaction estimates cannot independently establish fatigue, symptom severity, or conversational effort.
* **Potential bias from missing observations:** The available data may not represent the participant's complete daily routine.

Because of these limitations, the project is best considered **exploratory rather than confirmatory**.

---

## What I Learned

One of the most important lessons from the project was that **data analysis does not begin with finding a pattern — it begins with determining whether the data can support the pattern you want to measure**.

The project raised practical questions that are easy to overlook in controlled datasets:

* Can a period of missing sensor data be distinguished from inactivity?
* Is missing data random or systematic?
* How much confidence should be placed in a pattern when entire portions of the day are absent?
* Can a device designed for one population or purpose be meaningfully applied to another?
* How far can indirect physiological measurements be interpreted?
* When is the evidence too incomplete to justify a conclusion?

In this case, I found that some of the original hypotheses could **not be evaluated reliably from the available data**.

Rather than filling the missing periods or treating them as zero activity, I chose to preserve the missingness and treat it as a limitation of the dataset.

---

## What a Stronger Follow-Up Study Would Require

A stronger version of this project would include:

* Verified continuous wear time
* Device removal and charging logs
* Multiple participants
* Medication timing
* Self-reported fatigue and energy measurements
* Clinical symptom assessments
* A device validated for Parkinson’s-specific measurements
* A predefined strategy for identifying and handling missing data

These additions would make it easier to distinguish actual behavioral patterns from artifacts caused by the measurement process.

---

## Current Status

* **Baseline data:** Complete
* **Parkinson’s data collection:** Completed
* **Exploratory analysis:** Completed
* **Final clinical conclusions:** Not supported by the available data

The project did **not** produce a reliable clinical finding about Parkinson’s disease or social fatigue.

Instead, it demonstrated the practical challenges of taking real-world wearable data and attempting to translate it into behavioral conclusions.

---

## Final Takeaway

This project started with a question about Parkinson’s disease and everyday social interaction.

It ultimately taught me a broader lesson about working with real-world data:

> **Before asking what the data says, you have to establish whether the data is complete and reliable enough to say anything at all.**

The incomplete data and device limitations prevented me from making the conclusions I originally hoped to make. But identifying those limitations — and choosing not to overstate what the data showed — became one of the most important parts of the project.

The project gave me hands-on experience with **wearable sensor data, exploratory analysis, data-quality investigation, missing-data problems, measurement validity, and responsible interpretation of imperfect real-world datasets**.
