# PhD Defense Speaker Script: Intent Prediction from Physiological Signals

This document provides the complete, slide-by-slide speaker script (speaker notes) for the PhD thesis proposal defense of **João Garcia Farinha**. 

The script is perfectly aligned to the **22 slides** defined in your compiled presentation (`public/presentation/index.html`). It uses a highly professional, academically rigorous, and authoritative tone suitable for Prof. Fonseca, Dr. von Lühmann, and the rest of your doctoral jury.

---

## Part 1: Introduction & Thesis Motivation (Minutes 0–4)

### Slide 1: Cover Page
* **Section**: Cover
* **Slide Title**: PhD Proposal: Intent Prediction from Physiological Signals
* **Source PDF Page**: 1
* **Visual Cue**: Sleek, academic dark blue cover with FCUL and LASIGE branding.

#### 🎤 Speaker Script:
> "Good morning, members of the jury, Prof. Fonseca, and Dr. von Lühmann. Thank you all for being here today. 
> 
> My name is João Garcia Farinha, and today I am honored to present my PhD thesis proposal: **'Intent Prediction from Physiological Signals'**. 
> 
> At its core, my research proposes a fundamental paradigm shift: reframing physical and physiological noise as privileged, predictive context to permanently cross the zero-calibration and deployment barriers in Brain-Computer Interfaces."

---

### Slide 2: Document Overview
* **Section**: Document Overview
* **Slide Title**: Thesis Source Document Roadmap
* **Source PDF Page**: 3
* **Visual Cue**: A structured tabular layout showing the correspondence between presentation sections and the chapters of your written 87-page proposal.

#### 🎤 Speaker Script:
> "Before we begin, let us review the roadmap of our source proposal document, establishing the structural alignment for today’s presentation. 
> 
> We begin in **Section 1** by defining our core problem statement and research inquiries. 
> **Section 2** establishes the literature grounding and details our strategic open-science BIDS dataset release. 
> **Section 3** outlines our hybrid Transformer architecture, comparative processing pipelines, and experimental VR protocols. 
> Finally, we address our **Section 4** Risk Mitigation framework, project Gantt timeline, and **Section 5** concluding impact. This roadmap mirrors the exact flow of the written document in your hands."

---

### Slide 3: Problem Statement: The Societal Gap
* **Section**: 1. Problem / Motivation
* **Slide Title**: Problem Statement: The Societal Gap
* **Source PDF Page**: 5
* **Visual Cue**: A two-column premium slide contrasting laboratory BCI capabilities with real-world accessibility issues.

#### 🎤 Speaker Script:
> "When I first began reviewing the Brain-Computer Interface landscape, I was inspired by its profound potential to restore human agency and upgrade human-computer communication. 
> 
> However, I quickly realized a sobering reality: because of high hardware costs and complex calibration requirements, this life-changing technology remains locked inside specialized laboratories. It is entirely unavailable to those who need it most—individuals living with locked-in syndrome, advanced ALS, stroke survivors, and those recovering from spinal cord injuries in their home environments. 
> 
> To make BCIs a practical reality, we must shift away from immobile lab arrays and engineer a computational framework designed for ubiquitous, daily-life translation."

---

### Slide 4: The Gaps in the Research
* **Section**: 1. Problem / Motivation
* **Slide Title**: The Gaps in the Research
* **Source PDF Page**: 20
* **Visual Cue**: Three structured cards detailing the Hardware Gap, Contextual Blind Spot, and Topological Rigidity.

#### 🎤 Speaker Script:
> "Our current laboratory-grade models collapse in real-world environments because of three fundamental gaps in current BCI research. 
> 
> First, the **Hardware Gap**: models trained on dense, 256-channel laboratory arrays cannot project their weights onto the sparse consumer-grade wearables actually used in homes and clinics. 
> Second, **Topological Rigidity**: standard Riemannian covariance manifolds assume fixed geometry. A headset movement of just 2 centimeters causes matrix rank-deficiency and instant mathematical collapse. 
> Third, the **Contextual Blind Spot**: traditional BCI pipelines treat the user's auxiliary physiological signals—such as muscle activity, eye movement, and autonomic arousal—as 'noise' to be aggressively rejected and scrubbed out."

---

### Slide 5: Core Research Inquiry
* **Section**: 1. Problem / Motivation
* **Slide Title**: Core Research Inquiry (RQ1, RQ2, RQ3)
* **Source PDF Page**: 6
* **Visual Cue**: Three elegant key blocks displaying your primary Research Questions.

#### 🎤 Speaker Script:
> "My thesis argues the exact opposite of the traditional 'noise-erasure' paradigm. We argue that this physical and physiological noise is not waste—it is actually highly predictive, privileged context. By utilizing Asymmetric Knowledge Transfer, we can use this context to bridge the lab-to-wearable deployment gap. 
> 
> To prove this, I propose three central Research Questions:
> 
> * **RQ1 (Multimodal Fusion)**: How can auxiliary signals like electrodermal activity and thermal imaging prevent misclassifications of overlapping neural states under high cognitive load?
> * **RQ2 (Activity Gating)**: Can kinematics and activity vectors disambiguate concurrent motor imagery from actual physical walking to resolve non-stationarity?
> * **RQ3 (Asymmetric Transfer)**: How can Learning Using Privileged Information, or LUPI, allow highly constrained, sparse consumer wearables to match dense laboratory performance bounds?"

---

## Part 2: The Literature & Dataset Strategy (Minutes 4–7)

### Slide 6: Literature Roadmap & Grounding
* **Section**: 2. Literature
* **Slide Title**: Literature Roadmap & Grounding
* **Source PDF Page**: 18
* **Visual Cue**: Color-coded thematic blocks linking BCI literature concepts (Generalization, Illiteracy, Noise Shifts, Manifold Alignment).

#### 🎤 Speaker Script:
> "To ground our inquiries in the state-of-the-art, our literature roadmap focuses on four key pillars. 
> 
> We address the **Generalization Crisis**, where data leakage affects 73% of published BCI studies due to random segment-based splitting. 
> We examine **BCI Illiteracy Bounds**, where 20 to 50% of users fail to achieve voluntary control. 
> We leverage the **Noise Paradigm Shift**, moving away from strict artifact erasure to reframe physiological noise as predictive context. 
> And finally, we address **Manifold Alignment** to warp signals adaptively and overcome topological rigidity."

---

### Slide 7: Hybrid EEG-fNIRS: The Scarce Benchmarks
* **Section**: 2. Literature
* **Slide Title**: Hybrid EEG-fNIRS: The Scarce Benchmarks
* **Source PDF Page**: 18
* **Visual Cue**: Clean grids summarizing Shin et al. (2017), W. Yi et al. (2025), Gao et al. (2023), and M. Liu et al. (2025), with a red warning callout box.

#### 🎤 Speaker Script:
> "As we review the empirical literature, we discover a severe dataset bottleneck. The few publicly available hybrid EEG-fNIRS datasets are extremely small: Shin et al. contains only 29 subjects performing basic motor imagery; W. Yi et al. features 18 subjects; Gao et al. has 29; and M. Liu et al. contains 26. 
> 
> But the crucial blind spot is this: **none of these public benchmarks contain auxiliary physical or autonomic anchors**—such as electrodermal activity, thermal imaging, or kinematic IMU data. Classifiers remain completely blind to the user's peripheral body state."

---

### Slide 8: Legacy EEG-Only Baselines
* **Section**: 2. Literature
* **Slide Title**: Legacy EEG-Only Baselines
* **Source PDF Page**: 19
* **Visual Cue**: Four structured cards mapping standard single-modality baselines (PhysioNet, OpenBMI, GigaScience, BCI Competition IV-2a).

#### 🎤 Speaker Script:
> "Because hybrid datasets are so rare, the BCI community heavily relies on legacy, EEG-only baselines like PhysioNet, OpenBMI, GigaScience, and the classic BCI Competition IV-2a. 
> 
> While these repositories possess high subject counts, they are entirely blind to optical blood-flow hemodynamics and peripheral physiology. This single-modality bias leaves our deep learning architectures unprepared for the complex multimodal interactions of the real world."

---

### Slide 9: The FRESH 2025 Reproducibility Hub
* **Section**: 2. Literature
* **Slide Title**: The FRESH 2025 Reproducibility Hub
* **Source PDF Page**: 21
* **Visual Cue**: A two-column layout displaying Yücel and von Lühmann's FRESH (2025) study metrics alongside its dual datasets.

#### 🎤 Speaker Script:
> "Furthermore, the literature faces an analytical reproducibility crisis. As the recent **FRESH** study led by Yücel and von Lühmann (2025) demonstrated, when 38 global research teams processed the exact same fNIRS datasets, their analytical flexibility led to widely divergent statistical conclusions. 
> 
> Traditional, hand-crafted artifact rejection pipelines are highly vulnerable to pipeline drift. This highlights the absolute necessity of establishing stable, automated analytical standards for multimodal releases."

---

### Slide 10: The Dataset Gap: Weaponizing Our Release
* **Section**: 2. Literature
* **Slide Title**: The Dataset Gap: Weaponizing Our Release
* **Source PDF Page**: 24
* **Visual Cue**: A glowing blue card showcasing the BIDS-compliant 420-block corpus specs, with a dark speaker presentation box at the bottom.

#### 🎤 Speaker Script:
> "This brings us to the first major contribution of my thesis: we are building foundational open-science infrastructure. 
> 
> We are releasing a BIDS-compliant, **420-Block Multimodal Corpus across 30 Subjects**. This dataset integrates **32-channel EEG, 8-optode fNIRS**, and a complete behavioral suite of **Thermal imaging, GSR, and IMU kinematics**. 
> 
> By releasing this in a standard format, we provide the first open benchmark specifically designed to test asymmetric hardware transfers and peripheral context-awareness under strict Leave-One-Subject-Out constraints."

---

## Part 3: Architectures & Pipelines (Minutes 7–9)

### Slide 11: Deep Learning: Hybrid Multimodal Transformer
* **Section**: 3. Plan
* **Slide Title**: Deep Learning: Hybrid Multimodal Transformer
* **Source PDF Page**: 26
* **Visual Cue**: A three-column grid outlining Spatial Tokenization, Temporal Fusion, and Transfer Learning.

#### 🎤 Speaker Script:
> "To process this rich corpus, we cannot rely on rigid linear decoders. We propose a **Hybrid Multimodal Transformer**. 
> 
> First, we use a **CNN spatial tokenizer** based on EEGNet to act as spatial filters, extracting features while preserving electrode topology. 
> Second, we deploy a **Temporal Cross-Attention mechanism** to handle loose, non-linear synchronization between electrical (EEG), optical (fNIRS), and behavioral signals. 
> Third, we use **Learning Using Privileged Information (LUPI) distillation** to map the rich, research-grade Teacher latent space directly to the sparse wearable Student, effectively bridging the spatial hardware gap."

---

### Slide 12: Comparative Processing Pipelines
* **Section**: 3. Plan
* **Slide Title**: Comparative Processing Pipelines
* **Source PDF Page**: 28
* **Visual Cue**: An animated flow diagram contrasting Pipeline A (ASR scrubbing) and Pipeline B (Generative contextual gating).

#### 🎤 Speaker Script:
> "To prove our thesis, we systematically compare two distinct processing paradigms. 
> 
> In **Pipeline A (the SOTA Baseline)**, we follow standard practice: we use Artifact Subspace Reconstruction (ASR) to aggressively clean and erase physiological noise like blinking or jaw clenching. 
> 
> In **Pipeline B (our End-to-End Generative Pipeline)**, we do the exact opposite. We preserve those behavioral signals. We pass them directly into our Transformer's cross-attention blocks as privileged context, allowing the AI to learn the underlying neurovascular coupling dynamically."

---

## Part 4: The Methodology & Protocols (Minutes 9–15)

### Slide 13: RQ1 Stress-Testing the SNR
* **Section**: 3. Plan
* **Slide Title**: RQ1 Stress-Testing the SNR
* **Source PDF Page**: 30
* **Visual Cue**: A visual setup card detailing the 7-Activity VR Protocol designed to drown the neural signal.

#### 🎤 Speaker Script:
> "Let us look at the experimental protocols. To address **RQ1**, we test our 'Informative Artifact' paradigm using a **7-Activity VR Protocol** designed to systematically drown the primary EEG signal. 
> 
> We introduce startling virtual events and memory-heavy N-Back tasks to force frontal theta bleed that masks motor rhythms. In the final activity, the user chews and blinks rapidly to completely saturate the electrical channels. 
> 
> Our hypothesis is validated if our multimodal fusion framework maintains classifier accuracy by dynamically shifting its attention onto autonomic anchors—like GSR and Gaze—when neural channels become saturated."

---

### Slide 14: RQ2 Simulating the Everyday World
* **Section**: 3. Plan
* **Slide Title**: RQ2 Simulating the Everyday World
* **Source PDF Page**: 32
* **Visual Cue**: A visual setup card illustrating the Treadmill Gait Protocol with rhythmic artifacts.

#### 🎤 Speaker Script:
> "For **RQ2**, we test **Situational Gating** in ambulatory settings. We must prove that our network can distinguish between a user *imagining* movement and a user *actually* walking. 
> 
> We place subjects on a treadmill at 2 kilometers per hour, creating 0.5 to 2 Hertz physical gait artifacts that directly mimic neural sensorimotor rhythms, blinding traditional filters. 
> 
> By feeding continuous IMU kinematics into our Transformer as a kinematic Activity Vector, it acts as a gatekeeper. The network learns to ignore gait noise when the physical movement vectors are active, protecting the neural intent classifier from false positives."

---

### Slide 15: RQ3 Hardware Transfer Scenarios
* **Section**: 3. Plan
* **Slide Title**: RQ3 Hardware Transfer Scenarios
* **Source PDF Page**: 34
* **Visual Cue**: A grid mapping the 32-channel dense research headset down to 4-channel frontal wearables.

#### 🎤 Speaker Script:
> "For **RQ3**, we address the **Asymmetric Hardware Transfer**. We mathematically delete the channels that consumer wearables lack. 
> 
> We take our pristine 32-channel Teacher data and distill it down to a highly constrained 4-channel Student. 
> 
> If our Generative Student—equipped with heart rate, thermal, and gaze context—can successfully reconstruct the missing motor imagery features and match the Teacher's performance bounds, we have bypassed the hardware gap. We prove that cheap consumer wearables can achieve laboratory-grade accuracy."

---

### Slide 16: Evaluation Metrics & Anti-Shortcutting
* **Section**: 3. Plan
* **Slide Title**: Evaluation Metrics & Anti-Shortcutting
* **Source PDF Page**: 36
* **Visual Cue**: Visual cards detailing LOSO validation and the ablation control test.

#### 🎤 Speaker Script:
> "To guarantee maximum validation rigor, we employ strict Leave-One-Subject-Out cross-validation to prevent data leakage. 
> 
> Crucially, we implement an **Anti-Shortcutting Ablation Control**. The scientific risk is that our AI ignores the brain entirely and simply guesses motor intent based on eye gaze or facial muscle cues. 
> 
> To falsify this, we zero-out all EEG and fNIRS inputs at test time. If model accuracy does *not* collapse, it proves the model has learned a shortcut. Performance *must* drop to the baseline, scientifically proving that our auxiliary signals are enhancing—not replacing—the neural features."

---

### Slide 17: Dataset Cohort Design
* **Section**: 3. Plan
* **Slide Title**: Dataset Cohort Design
* **Source PDF Page**: 38
* **Visual Cue**: A timeline chart and detailed table laying out subject runs, durations, and variables.

#### 🎤 Speaker Script:
> "Our experimental cohort design maps out the structured sessions for our 30 subjects. Each subject completes 14 runs of Motor Imagery, combining physical execution, pure imagery, and active cognitive load conditions. 
> 
> We strictly catalog sensor layout configurations and monitor raw physical variables—like core temperature and skin conductance—to ensure our BIDS-compliant dataset is meticulously annotated and structured for the scientific community."

---

### Slide 18: Stressing the System (Mockup Sandbox)
* **Section**: 3. Plan
* **Slide Title**: Stressing the System (Mockup)
* **Source PDF Page**: 40
* **Visual Cue**: Live BCI simulator interface containing real-time canvas waves, a gating plane indicator, and interactive action buttons.
* **⚠️ Interactive Action**: Click the "Show Sandbox" and "Gait/Motion" buttons in your browser to demonstrate the transition!

#### 🎤 Speaker Script:
> "As demonstrated in our BCI Signal Sandbox mockup, we can simulate these dynamics in real-time. 
> 
> *[Action: Click 'Show Sandbox' in slide button]* 
> 
> When a user transitions from calm motor imagery to active gait or physical chewing, our pipeline dynamically updates the gating parameters. In motor imagery state, the classifier gates directly to 'INTENT'. 
> 
> *[Action: Click 'Gait/Motion' in slide button]*
> 
> But when physical kinematics spike, our IMU telemetry registers a gait artifact and gates the classifier to prevent noise saturation, maintaining manifold invariance."

---

## Part 5: Validation & Contingencies (Minutes 15–18)

### Slide 19: Risks & Contingencies
* **Section**: 4. Risks
* **Slide Title**: Risks & Contingencies
* **Source PDF Page**: 44
* **Visual Cue**: A distinct warning-bordered slide containing Strategy A, B, and C cards.

#### 🎤 Speaker Script:
> "As we conclude our methodology, I want to address our **Risk Mitigation Framework**. 
> 
> The primary algorithmic risk we anticipate is **Teacher Over-Specialization**: the Teacher model might build such complex dependencies on the privileged fNIRS features that the Student collapses when deployed on sparse hardware. 
> 
> If this occurs, we deploy a tiered contingency plan:
> * **Strategy A (Constrained Teacher)**: Train the Teacher exclusively on sparse EEG and behavioral signals, keeping fNIRS as a diagnostic control.
> * **Strategy B (Balanced Distillation)**: Apply balanced distillation with an auxiliary Mean Squared Error loss mapping.
> * **Strategy C (Prototype Learning)**: If the absolute performance floor is breached, we abandon feature alignment entirely and align per-class prototype boundaries."

---

## Part 6: Timeline & Conclusion (Minutes 18–20)

### Slide 20: Project Timeline & Project Gates
* **Section**: Timeline
* **Slide Title**: Project Timeline & Project Gates
* **Source PDF Page**: 43
* **Visual Cue**: A clean embedded SVG Gantt chart displaying tasks, publication targets, and project gates.

#### 🎤 Speaker Script:
> "We have mapped these milestones across a rigorous **4-year Gantt plan**. 
> 
> The project is structured around hierarchical gates—specifically at the Dataset Release, Fusion Validation, and Wearable Distillation phases. 
> 
> This ensures that every computational and clinical deliverable has a clear timeline and risk checkpoint, preventing schedule overruns and guaranteeing high-impact scientific publications."

---

### Slide 21: Potential Global Impact
* **Section**: 5. Conclusion
* **Slide Title**: Potential Global Impact
* **Source PDF Page**: 45
* **Visual Cue**: Three column blocks detailed with Clinical, Scientific, and Industrial impacts.

#### 🎤 Speaker Script:
> "The potential global impact of this work is extensive. 
> 
> In the **Clinical sphere**, it paves the way for zero-calibration neuro-rehabilitation lifelines that patients can use independently at home. 
> In the **Scientific sphere**, our BIDS dataset will empower open-science research. 
> and in the **Industrial sphere**, it lays the computational foundation for context-aware, consumer-grade neural interfaces."

---

### Slide 22: Conclusion Slide
* **Section**: 5. Conclusion
* **Slide Title**: Informative Artifacts &times; Contextual Gating &times; LUPI Transfer
* **Source PDF Page**: 46
* **Visual Cue**: Bold mathematical formula summarizing your thesis framework, with LASIGE/FCUL brand layouts.

#### 🎤 Speaker Script:
> "In conclusion: currently, the dream of restoring human agency through brain-computer interfaces is severely limited by immobile laboratory environments and massive calibration burdens. 
> 
> By successfully combining the **Informative Artifact paradigm, Contextual Gating, and LUPI Transfer**, we reframe physical and physiological noise as privileged context. This framework permanently eliminates the training-serving hardware skew and crosses the zero-calibration barrier. It is the computational engine required to transition brain-computer interfaces from brittle lab prototypes into resilient, real-world lifelines. 
> 
> Thank you for your time, and I am happy to open the floor to your questions."
