---
layout: post
title: "pMMG Sensor Placement for Knee Extension Torque Analysis"
# date: 2024-12-02
---

### Overview
A pneumatic mechanomyography (pMMG) sensor measures the local mechanical deformation of a contracting muscle as a pressure change inside a small air cell. In this exploratory study with one healthy participant, I measured pMMG responses at multiple attachment positions on the thigh and compared each one with reference knee joint torque, to find where the sensor best reflects knee extension. The squat-group results identified **vastus medialis (VM) 20%** and **vastus lateralis (VL) 30%** as candidate attachment positions. I led the project as first author, and the manuscript is currently under review at **Journal of Sensors (Wiley)**.

---

### Key Highlights

#### 1. Motivation & Objective
Wearable muscle sensors each have practical weaknesses: sEMG is sensitive to electrode–skin contact and electrical noise, force myography to wearing pressure and sensor position, and conventional MMG to vibration and motion artifacts. pMMG is noninvasive, resistant to electrical noise, and can measure over clothing. However, its pressure response depends on how well the muscle's deformation reaches the air cell, and unlike sEMG (with guidelines such as SENIAM), there is no established guidance on where to attach it. This study investigated attachment positions on the knee extensors VM and VL, with the knee flexor biceps femoris (BF) as a comparison muscle.

#### 2. Hardware & Experimental Setup

<div style="text-align: center; margin-top: 20px; margin-bottom: 30px;">
  <img src="{{ '/_assets/photos/pmmg-sensor/sensor_and_housing.jpeg' | relative_url }}" alt="Assembled pMMG sensors" style="width: 50%; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/pmmg-sensor/sensor_and_housing.jpeg' | relative_url }}')">
  <p style="font-size: 0.9em; color: #555; margin-top: 15px; line-height: 1.6; text-align: center; max-width: 80%; margin-left: auto; margin-right: auto;">
    <span style="display: block; font-style: italic; color: #666; margin-bottom: 5px;">Fig. 1: First-Round pMMG Sensors</span>
    Sensors and bands built for the first-round experiment.
  </p>
</div>

The project ran in two rounds. A first-round experiment (Fig. 1 and Fig. 3) was used to build the sensor system and refine the protocol. The manuscript is based on the second-round experiment, carried out at **Angel Robotics' Daejeon Planet** facility.

Each pMMG sensor contains an MS5607 pressure sensor and is read by an STM32 microcontroller (NUCLEO-G474RE) at 200 Hz, with the firmware developed in **STM32CubeIDE**. In the second round, the sensor was fixed with sports tape and then secured with an elastic band so it stayed at the same spot on the skin throughout the experiment. Reference knee joint torque was computed from a **Vicon** motion-capture system and a force-plate treadmill (MOTEK) using the plug-in gait dynamics model.

<div style="text-align: center; margin-top: 20px; margin-bottom: 30px;">
  <img src="{{ '/_assets/photos/pmmg-sensor/thigh_pmmg.jpg' | relative_url }}" alt="Sensor attachment on the thigh" style="width: 50%; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/pmmg-sensor/thigh_pmmg.jpg' | relative_url }}')">
  <p style="font-size: 0.9em; color: #555; margin-top: 15px; line-height: 1.6; text-align: center; max-width: 80%; margin-left: auto; margin-right: auto;">
    <span style="display: block; font-style: italic; color: #666; margin-bottom: 5px;">Fig. 2: Second-Round Setup</span>
    Thigh-mounted pMMG sensors with motion-capture markers on the force-plate treadmill.
  </p>
</div>

Attachment positions were expressed as a percentage of thigh length, from the distal femur (0%) to the top of the femoral head (100%). Responses were recorded at **20% to 60%** on each of VM, VL, and BF.

#### 3. Protocol & Analysis

<div style="display: flex; justify-content: center; gap: 10px; margin-top: 20px;">
  <img src="{{ '/_assets/photos/pmmg-sensor/squat_exp.jpg' | relative_url }}" alt="Squat task" style="width: 49%; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/pmmg-sensor/squat_exp.jpg' | relative_url }}')">
  <img src="{{ '/_assets/photos/pmmg-sensor/gait_exp.jpg' | relative_url }}" alt="Walking task" style="width: 49%; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/pmmg-sensor/gait_exp.jpg' | relative_url }}')">
</div>
<p style="font-size: 0.9em; color: #555; margin-top: 15px; margin-bottom: 30px; line-height: 1.6; text-align: center;">
  <span style="display: block; font-style: italic; color: #666; margin-bottom: 5px;">Fig. 3: First-Round Movement Tasks</span>
  Squat and walking tasks from the first-round experiment, used to develop the protocol.
</p>

The participant performed **squat, single-leg squat, crouch gait**, and **walking at 1.0 and 1.5 m/s**. Squat, single-leg squat, and crouch gait load the knee extensors heavily and were pooled as the *squat group*; walking served as a low-torque dynamic comparison. Each trial started and ended with three foot stomps, which were used to align the pMMG and motion-capture data in time.

For each sensor position, a passive knee movement trial (no voluntary contraction) gave a baseline pressure that was subtracted from the active trials. After a 4 Hz low-pass filter, I computed the squared Pearson correlation **R²** between the pMMG pressure response and knee joint torque for every muscle, position, and task. R² was used as a measure of linear association, not of torque-estimation accuracy.

<div style="text-align: center; margin-top: 20px; margin-bottom: 30px;">
  <img src="{{ '/_assets/photos/pmmg-sensor/hwconfig.jpeg' | relative_url }}" alt="STM32 pin configuration" style="width: 60%; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/pmmg-sensor/hwconfig.jpeg' | relative_url }}')">
  <p style="font-size: 0.9em; color: #555; margin-top: 15px; line-height: 1.6; text-align: center; max-width: 80%; margin-left: auto; margin-right: auto;">
    <span style="display: block; font-style: italic; color: #666; margin-bottom: 5px;">Fig. 4: MCU Configuration</span>
    Pin configuration of the STM32G474RE in STM32CubeIDE for the sensor interfaces.
  </p>
</div>

#### 4. Results
* **VM and VL track knee torque far better than BF.** Across squat, single-leg squat, and crouch gait, the position-averaged R² of VM and VL was higher than that of BF, consistent with their roles as knee extensors.
* **Candidate positions: VM 20% and VL 30%.** In the squat group, the strongest relationships with knee torque were at VM 20% and VL 30%, clearly stronger than at the other positions on each muscle.
* **Best positions sit distal to the muscle belly.** VL's best position lay distal to its largest cross-section, suggesting that soft-tissue thickness and signal transmission matter as well as muscle-belly location. Both candidates are close to the distal SENIAM sEMG electrode sites.
* **Walking gives weak, variable relationships.** With a narrow torque range and more movement artifacts, walking produced low R², so it was treated as a comparison condition rather than a basis for choosing positions.

#### 5. Limitations & Current Status
Because the study involved a single participant, VM 20% and VL 30% are candidate positions, not a definitive guideline. The 30% squat data were excluded due to a data-acquisition error, and knee joint torque is a net joint torque rather than an individual muscle's contribution. Future work should test more participants with repeated measurements. The manuscript, *Placement-Dependent pMMG Responses for Knee Extension Torque Analysis*, is under review at **Journal of Sensors (Wiley)**.

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
