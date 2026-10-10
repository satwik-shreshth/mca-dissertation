# Implementation of a Communication-Integrated Mobile Environmental Monitoring Framework

**MCA Dissertation** | Department of Computer Applications, Sikkim University, Gangtok

This repository contains the LaTeX source and the compiled PDF of my Master of Computer Applications (MCA) dissertation.

- **Author:** Satwik Shreshth (Roll No. 24MCA014)
- **Supervisor:** Mr. Partha Pratim Ray, Assistant Professor, Department of Computer Applications, Sikkim University
- **Co-Supervisor:** Dr. Ravi Kant Jain, Scientist F, Intelligent Systems Engineering Group, CSIR-Central Mechanical Engineering Research Institute (CSIR-CMERI)

**Read the thesis:** [`Dissertation/Satwik Dissertation Report.pdf`](Dissertation/Satwik Dissertation Report.pdf)

## Abstract

Fixed-location indoor environmental monitoring systems fail to capture spatial variation in air quality, temperature, and humidity across a room. This work presents a communication-integrated mobile environmental monitoring framework that mounts a real-time sensor suite on an autonomous mobile robot.

- **Navigation (Raspberry Pi 5):** A YOLOv8n-seg instance segmentation model, exported to ONNX for CPU inference, detects a red adhesive tape path through a downward-facing camera. The lateral deviation drives a PID steering controller.
- **Environmental monitoring (Raspberry Pi 3):** A DHT11 and an MQ-135 air quality sensor, read through an Arduino, provide temperature, humidity, and calibrated CO2 estimates, with a six-level rule-based alert classification.
- **Communication:** Sensor data is sent concurrently to a local SQLite database, Firebase Realtime Database, a ThingSpeak IoT channel, and a Flask web dashboard.
- **Architecture:** The dual-processor design keeps navigation and monitoring tasks computationally isolated.

Experimental results validate the feasibility of real-time, spatially aware indoor environmental monitoring on low-cost embedded hardware.

**Keywords:** Mobile Robot, Path Segmentation, PID Control, Autonomous Navigation, Environmental Monitoring

## Contents

1. Introduction
2. Literature Review
3. Methodology (hardware design, path dataset and YOLOv8 training, autonomous path following, environmental monitoring system)
4. Results and Discussion
5. Conclusion and Future Work

## Repository Structure

```
.
├── Dissertation/     # Compiled dissertation (PDF)
├── TeX files/        # LaTeX source files (.tex, bibliography, figures)
├── LICENSE           # CC BY 4.0
└── README.md
```

- **`Dissertation/`**: the final PDF of the thesis.
- **`TeX files/`**: everything needed to rebuild the PDF from source.

## How to Cite

```bibtex
@mastersthesis{shreshth2026mobilemonitoring,
  author  = {Shreshth, Satwik},
  title   = {Implementation of a Communication-Integrated Mobile Environmental Monitoring Framework},
  school  = {Sikkim University},
  address = {Gangtok, India},
  year    = {2026},
  type    = {MCA Dissertation}
}
```

## License

Copyright (c) 2026 Satwik Shreshth.

This work is licensed under the [Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). You are free to share and adapt the material, provided you give appropriate credit, link to the license, and indicate if changes were made. See [`LICENSE`](LICENSE) for the full legal text.
