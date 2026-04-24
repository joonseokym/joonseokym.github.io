---
layout: post
title: "Optimal pneumatic mechanomyography Sensor Placement for Knee Extensor Analysis"
# date: 2024-12-02
---

### 1. Overview / Abstract
This project introduces a wearable, pneumatic mechanomyography (pMMG) sensor system designed to overcome the practical limitations of conventional muscle activation sensors. As the first author and project lead, I directed the entire research cycle—from hardware design and protocol formulation to signal processing and algorithm validation—to establish optimal sensor placement guidelines for estimating knee extensor joint torque.

### 2. Motivation & Objective
Conventional sEMG sensors are highly susceptible to sweat-induced signal distortion, electrical noise, and require direct skin contact. To resolve these issues, we developed a robust pMMG sensor system capable of directly measuring mechanical muscle changes, even over clothing. Beyond simply building a sensor, the primary objective of this research is to mathematically identify the optimal sensor placements on the knee extensors (Rectus Femoris, Vastus Medialis, and Vastus Lateralis) to effectively estimate joint torque for lower limb biomechanical analysis.

### 3. Hardware System Design

<div style="text-align: center; margin-bottom: 30px;">
  <img src="{{ '/_assets/photos/pmmg-sensor/sensor_and_housing.jpeg' | relative_url }}" alt="Final assembled sensor and 3D housing" style="width: 50%; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/pmmg-sensor/sensor_and_housing.jpeg' | relative_url }}')">
  <p style="font-size: 0.9em; color: #666; font-style: italic; margin-top: 10px;">*Fig 1. Final assembled pMMG sensor and 3D-printed housing.*</p>
</div>

<div style="text-align: center; margin-bottom: 30px;">
  <img src="{{ '/_assets/photos/pmmg-sensor/thigh_pmmg.png' | relative_url }}" alt="Sensor attachment on the thigh" style="width: 50%; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/pmmg-sensor/thigh_pmmg.png' | relative_url }}')">
  <p style="font-size: 0.9em; color: #666; font-style: italic; margin-top: 10px;">*Fig 2. Sensor attachment on the thigh for data acquisition.*</p>
</div>

To accommodate diverse body types and control external variables like band tension, I designed a non-elastic Velcro-based sensor housing. The hardware incorporates a PVC film-based air pouch, an MS5607 pneumatic pressure sensor, and an STM32 (NUCLEO-G474RE) microcontroller. The firmware was developed utilizing **STM32CubeIDE** to ensure reliable and continuous data acquisition at a 200Hz sampling rate.

### 4. Signal Processing & Validation

<div style="display: flex; justify-content: center; gap: 10px; margin-bottom: 10px;">
  <img src="{{ '/_assets/photos/pmmg-sensor/squat_exp.png' | relative_url }}" alt="Squat Experiment" style="width: 49%; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/pmmg-sensor/squat_exp.png' | relative_url }}')">
  <img src="{{ '/_assets/photos/pmmg-sensor/gait_exp.png' | relative_url }}" alt="Gait Experiment" style="width: 49%; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/pmmg-sensor/gait_exp.png' | relative_url }}')">
</div>
<p style="text-align: center; font-size: 0.9em; color: #666; font-style: italic; margin-bottom: 30px;">
  *Fig 3. Experimental setup for simultaneous measurement of pMMG pressure and knee joint torque during squat and walking tasks.*
</p>

<div style="display: flex; gap: 20px; margin-bottom: 30px; align-items: flex-start;">
  <div style="flex: 1; text-align: center;">
    <img src="{{ '/_assets/photos/pmmg-sensor/datamonitoring.jpeg' | relative_url }}" alt="Data Monitoring Interface" style="width: 100%; height: 220px; object-fit: cover; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/pmmg-sensor/datamonitoring.jpeg' | relative_url }}')">
    <p style="font-size: 0.9em; color: #555; margin-top: 15px; line-height: 1.6; text-align: left;">
      <span style="display: block; font-style: italic; color: #666; margin-bottom: 5px;">*Fig 4: Real-time Data Monitoring Interface (Representative sEMG GUI)*</span>
      While pMMG-specific captures were not preserved, this representative interface illustrates the real-time acquisition system used, featuring core controls and multi-channel waveform displays for immediate signal verification.
    </p>
  </div>
  <div style="flex: 1; text-align: center;">
    <img src="{{ '/_assets/photos/pmmg-sensor/hwconfig.jpeg' | relative_url }}" alt="Hardware Configuration" style="width: 100%; height: 220px; object-fit: cover; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/pmmg-sensor/hwconfig.jpeg' | relative_url }}')">
    <p style="font-size: 0.9em; color: #555; margin-top: 15px; line-height: 1.6; text-align: left;">
      <span style="display: block; font-style: italic; color: #666; margin-bottom: 5px;">*Fig 5: Hardware Configuration*</span>
      Pinout configuration of the STM32G474RETx MCU in STM32CubeIDE, detailing SPI and ADC assignments essential for processing raw pMMG and sEMG signals.
    </p>
  </div>
</div>

To validate the sensor's reliability, I designed comprehensive experimental protocols involving squat and treadmill walking tasks. Real-time sensor data was continuously monitored and logged using **STM32CubeMonitor** and custom **Python** scripts. I built a signal processing pipeline utilizing Least Squares Fitting to remove passive muscle stretch offsets, successfully extracting only the active muscle force generation signals. Subsequent Z-normalization and custom linearity evaluation equations were applied to quantitatively analyze the pMMG signal's response to increasing load. Notably, the validation included simultaneous measurements of pMMG pressure and knee joint torque to rigorously verify the correlation between the two.

### 5. Outcomes & Current Status
The analysis proved that the Vastus Medialis exhibits the most linear and consistent response to load changes, allowing us to derive optimal placement guidelines for each target muscle (Rectus Femoris 50%, Vastus Lateralis 60%, Vastus Medialis 20%). Furthermore, walking experiments demonstrated a remarkable 1.97% error rate between the pMMG signal inflection points and the actual joint torque. Based on these strongly validated results, I am currently finalizing a first-author manuscript detailing this torque prediction model, intended for submission to **Biomedical Engineering Letters**.

<!-- Unified Image Modal -->
<div id="unified-image-modal" style="display: none; position: fixed; z-index: 2000; left: 0; top: 0; width: 100%; height: 100%; background-color: rgba(15, 23, 42, 0.85); backdrop-filter: blur(6px); -webkit-backdrop-filter: blur(6px); align-items: center; justify-content: center; cursor: zoom-out;" onclick="this.style.display='none'">
  <span style="position: absolute; top: 20px; right: 30px; color: rgba(255,255,255,0.8); font-size: 40px; font-weight: bold;">&times;</span>
  <img id="modal-img-src" src="" style="max-width: 90%; max-height: 90vh; border-radius: 12px; box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.5);">
</div>

<script>
  function openModal(imageSrc) {
    document.getElementById('modal-img-src').src = imageSrc;
    document.getElementById('unified-image-modal').style.display = 'flex';
  }
</script>