---
layout: post
title: "Development of a Circular Twisted String Continuous Passive Motion Actuator"
# date: 2021-04-01
---

### Overview
A lightweight, wearable Continuous Passive Motion (CPM) actuator for elbow rehabilitation that uses a twisted string mechanism and a 2-stage pulley system. The project received a Fourth Award (Biomedical Engineering) and the USAID Science Champion Award at Regeneron ISEF 2021, and the device was later registered as a Korean patent (KR102635233B1).

---

### Key Highlights

#### 1. Problem
Existing CPM devices are bulky and heavy, so patients have to visit hospitals for rehabilitation. A wearable device needs to be small and light while still producing enough force to move the forearm.

#### 2. Mechanism & Design
Designed a circular, wearable CPM actuator that transmits power through a twisted string. Twisted strings produce high force from a small motor, but their contraction length is short, which limits the Range of Motion (ROM). To solve this, a 2-stage pulley system was integrated inside the circular housing, quadrupling both the range of motion and the speed to reach a 10.6 cm operational range, enough for elbow rehabilitation.

#### 3. Performance
Load tests showed an output force of over 60N, well above the 32.6N required to move an adult male's forearm at a constant velocity. The mechanism achieved up to a 15-fold increase in output force relative to motor torque.

#### 4. Validation
A mathematical model was established to predict string displacement and output force from the number of twists, and it was validated experimentally using linear potentiometers. The results confirmed that the mechanism stays linear when string contraction is kept under 33%, showing that it is viable for practical, high-load rehabilitation tasks.

<div style="text-align: center; margin-top: 20px; margin-bottom: 30px;">
  <img src="{{ '/_assets/photos/twisted-string-cpm/ISEF Quad Chart_0421.png' | relative_url }}" alt="ISEF Quad Chart" style="width: 100%; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/twisted-string-cpm/ISEF Quad Chart_0421.png' | relative_url }}')">
  <p style="font-size: 0.9em; color: #555; margin-top: 15px; line-height: 1.6; text-align: center; max-width: 80%; margin-left: auto; margin-right: auto;">
    <span style="display: block; font-style: italic; color: #666; margin-bottom: 5px;">Fig. 1: Regeneron ISEF 2021 Quad Chart</span>
    Summary of the research question, mechanism design, experimental results, and conclusions presented at ISEF.
  </p>
</div>

---

<div style="text-align: center; margin-top: 40px;">
  <a href="{{ '/_assets/pdf/Research Plan.pdf' | relative_url }}" target="_blank" style="display: inline-block; padding: 12px 24px; background-color: #3b82f6; color: white; text-decoration: none; border-radius: 8px; font-weight: bold; transition: background-color 0.2s; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
    📄 Download Full Research Plan (PDF)
  </a>
</div>

<p style="margin-top: 20px; font-size: 0.9em; color: #666; font-style: italic; text-align: center;">
  Note: This research was conducted and originally published under the name Joonseo Kim.
</p>

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
