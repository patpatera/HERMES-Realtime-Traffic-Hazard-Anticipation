# HERMES: Real-Time Traffic Hazard Anticipation on Edge Devices

**Hierarchical Efficient RWKV with Multi-rate Event Sensing**

HERMES is a research-to-production project for real-time, causal traffic hazard anticipation using a CUDA/CoreML-optimized RWKV video model.

The system performs frame-by-frame online inference directly from video streams, deployed on iPhone and NVIDIA Jetson Orin Nano, and validated in real-world motorcycle riding scenarios.

---

## Demo

### Real-world iOS deployment

HERMES was optimized with CoreML and deployed on iPhone for real-time frame-by-frame inference.

| Motorcycle-mounted iPhone demo | Real-time hazard prediction |
|---|---|
| ![](demos/Demo_V1.gif) | ![](assets/demo_2.gif) |

---

## Highlights

- **Real-time online inference** with no access to future frames
- **CoreML-optimized iOS deployment**
- **Frame-by-frame inference on iPhone 17**
- **Motorcycle-mounted real-world testing**
- **Proposed custo spatio-temporal modeling** with linear complexity
- **Multi-task prediction**: anomaly occurrence, localization, and category
- **Edge deployment**: 31M parameters, 100 FPS on Jetson Orin Nano

---

## Method Overview

HERMES uses a Hierarchical Spatio-Temporal RWKV backbone for efficient causal video understanding.

Main components:

1. **HST-RWKV Backbone**  
   Hierarchical spatial encoding with recurrent temporal modeling.

2. **Multi-rate Event Sensing**  
   Stride-controlled recurrent updates capture both fast motion cues and long-range context.

3. **Causal Future Distillation**  
   Predictive self-supervision that teaches an online student model using future-aware targets during training only.

4. **Unified Multi-task Objective**  
   Joint anomaly anticipation, localization, and category prediction.

---

## System Pipeline

```mermaid
flowchart LR
    A[Camera Stream] --> B[Frame Preprocessing]
    B --> C[CoreML HERMES Model]
    C --> D[Risk Score]
    C --> E[Localization Map]
    C --> F[Anomaly Category]
    D --> G[Real-time Warning UI]
    E --> G
    F --> G
