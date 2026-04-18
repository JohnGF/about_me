---
layout: ../../layouts/ProjectLayout.astro
title: "NEUROREADY: Real-Time Operator Readiness"
description: "A joint project with the Portuguese Navy (CINAV) developing a real-time safety governor for extended military operations."
tags: ["EEG-fNIRS", "LUPI Paradigm", "Predictive AI"]
problem: "In high-stakes, 24/7 military surveillance operations, human operators are prone to cognitive saturation and mental fatigue. Current systems fail to detect early neural signatures of exhaustion, leading to critical, potentially catastrophic human errors."
tasks:
  - "Collaborate with CINAV to collect data in simulated extended military surveillance scenarios."
  - "Develop a hybrid EEG-fNIRS processing pipeline to monitor both electrical brain activity and cerebral hemodynamics."
  - "Build an AI governor that predicts human error *before* it occurs."
eureka: "We discovered a consistent 'Neural Signature of Exhaustion' by fusing EEG and fNIRS data. The lag between the fast electrical markers (EEG) and the slower metabolic markers (fNIRS) provided a temporal window. This allowed the AI to predict cognitive failure up to 15 minutes before behavioral errors manifested."
results: "The NEUROREADY system successfully identifies critical mental fatigue states and acts as a real-time safety governor. It is currently being evaluated for integration into extended mission protocols, enhancing operator safety and operational success."
---

<div class="timeline-item">
  <span class="timeline-date">Phase 1: Sensor Fusion Pipeline</span>
  <div class="timeline-content">Developed a synchronized data acquisition system combining portable EEG and fNIRS sensors, utilizing Lab Streaming Layer (LSL).</div>
</div>

<div class="timeline-item">
  <span class="timeline-date">Phase 2: Data Collection & Modeling</span>
  <div class="timeline-content">Conducted rigorous testing in simulated surveillance environments to gather data on operator fatigue, training predictive models on the fused dataset.</div>
</div>

<div class="timeline-item">
  <span class="timeline-date">Phase 3: Real-Time Governor</span>
  <div class="timeline-content">Deployed the optimized predictive AI onto embedded hardware, creating a system that triggers preemptive alerts when the 'Neural Signature of Exhaustion' is detected.</div>
</div>
