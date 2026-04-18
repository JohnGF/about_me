---
layout: ../../layouts/ProjectLayout.astro
title: "Braille Anywhere"
description: "Patent-pending portable tactile display for the visually impaired."
tags: ["PCB Design", "C Firmware", "Patent Pending"]
problem: "Digital accessibility for the visually impaired is hindered by the exorbitant cost and bulkiness of traditional refreshable Braille displays. Most devices cost thousands of dollars and are confined to desktop setups."
tasks:
  - "Engineer a low-cost, highly portable tactile actuator mechanism."
  - "Design a custom Printed Circuit Board (PCB) using KiCad."
  - "Write optimized, low-latency C firmware to drive the electromechanical components."
  - "Develop an Android companion app for seamless text-to-braille translation via Bluetooth."
eureka: "The key to affordability and portability was moving away from traditional piezoelectric actuators. By inventing a novel electromechanical approach utilizing miniature custom solenoids and a 3D-printed continuous track, we drastically reduced the cost per braille cell while maintaining tactile fidelity."
results: "Built a fully functional, highly portable prototype that pairs with smartphones. The device brings the cost of a braille display down by an order of magnitude. A patent for the novel actuation mechanism is currently pending."
---

<div class="timeline-item">
  <span class="timeline-date">Phase 1: Mechanical Prototyping</span>
  <div class="timeline-content">Iterated through multiple 3D-printed designs (FreeCAD) to perfect the tactile feeling and miniaturize the actuator mechanism.</div>
</div>

<div class="timeline-item">
  <span class="timeline-date">Phase 2: Electronics & Firmware</span>
  <div class="timeline-content">Designed the custom PCB in KiCad and wrote the embedded C firmware to ensure real-time, low-latency actuation of the braille pins.</div>
</div>

<div class="timeline-item">
  <span class="timeline-date">Phase 3: Software Integration & Patent</span>
  <div class="timeline-content">Developed the Bluetooth Android companion app and successfully filed a patent for the unique, affordable tactile display technology.</div>
</div>
