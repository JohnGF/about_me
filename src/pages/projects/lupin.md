---
layout: ../../layouts/ProjectLayout.astro
title: "LUPIN: Learning User Physiological Intent Networks"
description: "A major initiative to enable affordable, home-based neurorehabilitation for stroke and ALS patients."
tags: ["AI Transformer", "Multimodal EEG", "Neurorehabilitation"]
problem: "Currently, high-fidelity neurorehabilitation relies on expensive, $50k lab-grade EEG equipment. Consumer wearables exist, but their signal quality is sparse and noisy, making robust decoding difficult in uncontrolled, real-world environments."
tasks:
  - "Design a multimodal AI Transformer architecture capable of handling sparse consumer EEG data."
  - "Incorporate auxiliary physiological signals such as eye gaze, heart rate, and skin conductance into the model."
  - "Develop a framework that bridges the performance gap between lab equipment and consumer wearables using LUPI (Learning Using Privileged Information)."
eureka: "The breakthrough came when we realized that physiological 'noise' (like eye movements or heart rate fluctuations) shouldn't be filtered out. Instead, using the LUPI paradigm, we treated this 'noise' as predictive context during the training phase, allowing the model to perform robustly at inference time even when only the noisy EEG was available."
results: "By fusing sparse EEG data with auxiliary physiological signals via our Transformer network, we achieved near lab-grade decoding accuracy with a sub-$1k consumer wearable. This paves the way for accessible, home-based rehabilitation for patients with stroke or ALS."
---

<div class="timeline-item">
  <span class="timeline-date">Phase 1: Architecture Design</span>
  <div class="timeline-content">Formulated the core Transformer network to align asynchronous multimodal signals (EEG, HR, Eye Gaze).</div>
</div>

<div class="timeline-item">
  <span class="timeline-date">Phase 2: The LUPI Framework</span>
  <div class="timeline-content">Implemented the Learning Using Privileged Information paradigm. We trained the model in a lab setting where all signals were available (privileged information), and deployed a lighter version that relies solely on consumer EEG while retaining high accuracy.</div>
</div>

<div class="timeline-item">
  <span class="timeline-date">Phase 3: Validation & Testing</span>
  <div class="timeline-content">Validated the model on datasets mimicking real-world, noisy home environments, demonstrating significant improvements over traditional single-modal baselines.</div>
</div>
