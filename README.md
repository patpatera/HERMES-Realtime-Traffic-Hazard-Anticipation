# HERMES: Real-Time Traffic Hazard Anticipation on Edge Devices

**Hierarchical Efficient RWKV with Multi-rate Event Sensing**

HERMES is a research-to-production project for real-time, causal traffic hazard anticipation using a CUDA/CoreML-optimized RWKV video model.

The system performs frame-by-frame online inference directly from video streams and predicts traffic risk without using future frames. HERMES is deployed on iPhone via CoreML and on NVIDIA Jetson Orin Nano via CUDA/TensorRT, and validated in real-world motorcycle riding scenarios.

> Paper currently under review. Code and pretrained weights will be released after the review process.

---

## Real-World iOS Deployment

HERMES was integrated into a real-time iOS prototype for motorcycle-mounted traffic hazard anticipation.  
The system performs causal frame-by-frame inference directly from the live camera stream and visualizes predicted traffic risk through an on-screen safety interface.

The app displays:

- real-time hazard state: **SAFE / WARNING**
- frame-level risk probability
- current riding speed
- visual localization overlay for potentially relevant traffic regions
- continuous online prediction without access to future frames

The model was optimized for mobile edge deployment using CoreML and tested in real-world urban riding scenarios, including daytime rain, nighttime traffic, dense scooter flows, intersections, and mixed vehicle environments.

---

## Demo Gallery

The following examples show HERMES running in real time on iPhone during motorcycle riding in urban traffic.  
Each demo is sampled from real-world riding footage and illustrates different traffic conditions, lighting, road layouts, and interaction patterns.

| Demo | Scenario | Description |
|---|---|---|
| ![](assets/demo_1.gif) | Dense urban interaction | Real-time **WARNING** prediction in dense scooter traffic near an intersection, where nearby vehicles create elevated short-range risk. |
| ![](assets/demo_2.gif) | Nighttime following | Stable **SAFE** prediction during nighttime riding with cars and scooters ahead under low-light conditions. |
| ![](assets/demo_3.gif) | Nighttime intersection zone | Online risk estimation while approaching a marked intersection area with complex road patterns and artificial lighting. |
| ![](assets/demo_4.gif) | Multi-lane night traffic | Causal frame-by-frame inference during normal multi-lane traffic flow at night. |
| ![](assets/demo_5.gif) | Rainy scooter traffic | Robust prediction under wet-road reflections and dense scooter interactions. |
| ![](assets/demo_6.gif) | Rainy urban corridor | Real-world deployment in rainy city traffic with storefront clutter, scooters, and mixed vehicles. |
| ![](assets/demo_7.gif) | Close-range scooter interaction | Hazard localization highlights nearby scooters and vehicles in close-proximity riding. |
| ![](assets/demo_8.gif) | Rainy intersection approach | Risk estimation while approaching an urban intersection under rainy conditions. |
| ![](assets/demo_9.gif) | Crowded scooter queue | Stable prediction in slow-moving dense scooter traffic with pedestrians and roadside activity. |
| ![](assets/demo_10.gif) | Higher-speed urban road | Real-time safety monitoring at higher speed with surrounding vehicles and lane-level motion. |

---

## App Interface

The iOS interface is designed for real-time riding feedback:

- **Status indicator**: displays `SAFE` or `WARNING`
- **Risk score**: frame-level probability of hazardous traffic evolution
- **Speed display**: current riding speed from device location sensors
- **Visual overlay**: highlights traffic regions contributing to the prediction
- **Live camera view**: continuous video stream processed on-device

The interface is intentionally lightweight to preserve real-time performance and avoid distracting the rider.

---

## System Pipeline

```mermaid
flowchart LR
    A[Live Camera Stream] --> B[Frame Preprocessing]
    B --> C[CoreML HERMES Model]
    C --> D[Risk Score]
    C --> E[Hazard Localization]
    C --> F[Traffic State]
    D --> G[iOS Safety Interface]
    E --> G
    F --> G
