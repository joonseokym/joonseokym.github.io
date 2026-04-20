---
layout: post
title: "Optimal pneumatic mechanomyography Sensor Placement for Knee Extensor Analysis"
date: 2024-12-02
---

### 1. Overview / Abstract
This project introduces a wearable, pneumatic mechanomyography (pMMG) sensor system designed to overcome the practical limitations of conventional muscle activation sensors. As the first author and project lead, I directed the entire research cycle—from hardware design and protocol formulation to signal processing and algorithm validation—to establish optimal sensor placement guidelines for estimating knee extensor joint torque.

### 2. Motivation & Objective
Conventional sEMG sensors are highly susceptible to sweat-induced signal distortion, electrical noise, and require direct skin contact. To resolve these issues, we developed a robust pMMG sensor system capable of directly measuring mechanical muscle changes, even over clothing. Beyond simply building a sensor, the primary objective of this research is to mathematically identify the optimal sensor placements on the knee extensors (Rectus Femoris, Vastus Medialis, and Vastus Lateralis) to effectively estimate joint torque for lower limb biomechanical analysis.

### 3. Hardware System Design

![Final assembled sensor and 3D housing](/assets/photos/sensor_and_housing.jpeg)
*Fig 1. Final assembled pMMG sensor and 3D-printed housing.*

![Sensor attachment on the thigh](/path/to/your/image2.jpg)
*Fig 2. Sensor attachment on the thigh for data acquisition.*

To accommodate diverse body types and control external variables like band tension, I designed a non-elastic Velcro-based sensor housing. The hardware incorporates a PVC film-based air pouch, an MS5607 pneumatic pressure sensor, and an STM32 (NUCLEO-G474RE) microcontroller. The firmware was developed utilizing **STM32CubeIDE** to ensure reliable and continuous data acquisition at a 200Hz sampling rate.

### 4. Signal Processing & Validation

![Squat and walking experiments](/path/to/your/image3.jpg)
*Fig 3. Experimental setup for simultaneous measurement of pMMG pressure and knee joint torque during squat and walking tasks.*

![Data monitoring interface](/path/to/your/image4.jpg)
*Fig 4. Real-time data acquisition and signal monitoring interface utilizing Python and STM32CubeMonitor.*

To validate the sensor's reliability, I designed comprehensive experimental protocols involving squat and treadmill walking tasks. Real-time sensor data was continuously monitored and logged using **STM32CubeMonitor** and custom **Python** scripts. I built a signal processing pipeline utilizing Least Squares Fitting to remove passive muscle stretch offsets, successfully extracting only the active muscle force generation signals. Subsequent Z-normalization and custom linearity evaluation equations were applied to quantitatively analyze the pMMG signal's response to increasing load. Notably, the validation included simultaneous measurements of pMMG pressure and knee joint torque to rigorously verify the correlation between the two.

### 5. Outcomes & Current Status
The analysis proved that the Vastus Medialis exhibits the most linear and consistent response to load changes, allowing us to derive optimal placement guidelines for each target muscle (Rectus Femoris 50%, Vastus Lateralis 60%, Vastus Medialis 20%). Furthermore, walking experiments demonstrated a remarkable 1.97% error rate between the pMMG signal inflection points and the actual joint torque. Based on these strongly validated results, I am currently finalizing a first-author manuscript detailing this torque prediction model, intended for submission to **Biomedical Engineering Letters**.