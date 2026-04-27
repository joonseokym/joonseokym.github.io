---
layout: post
title: "Development of a Drone Landing Gear Mimicking Cat Skeletal Structure"
# date: 2019-04-01
---

### Overview
A drone landing gear designed to ensure safe landings and prevent cargo damage by mimicking the shock-absorbing skeletal structure of a cat.

---

### Key Highlights

#### 1. Problem
During drone deliveries, packages and their internal contents are at risk of damage upon landing or dropping, necessitating an improved landing gear system for effective shock absorption.

#### 2. Mechanism & Design
Developed a 3D-printed landing gear that replicates the leg proportions of a cat's skeleton. To mitigate impact, neodymium magnets were integrated between the joints to utilize repulsive forces like a spring, and PVC foam was attached to the bottom of the feet. The legs were arranged radially, rather than straight, for enhanced stability and buffering.

<div style="display: flex; gap: 20px; margin-top: 20px; margin-bottom: 30px; align-items: flex-start;">
  <div style="flex: 1; text-align: center;">
    <img src="{{ '/_assets/photos/landing-gear/straightleg.jpeg' | relative_url }}" alt="Straight Leg Arrangement" style="width: 100%; height: 250px; object-fit: cover; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/landing-gear/straightleg.jpeg' | relative_url }}')">
    <p style="font-size: 0.9em; color: #555; margin-top: 15px; line-height: 1.6; text-align: left;">
      <span style="display: block; font-style: italic; color: #666; margin-bottom: 5px;">*Fig. 1: Straight (11-shaped) Leg Arrangement Model*</span>
      Initial design mimicking a cat's straight leg stance. Neodymium magnets between joints act as shock-absorbing springs.
    </p>
  </div>
  <div style="flex: 1; text-align: center;">
    <img src="{{ '/_assets/photos/landing-gear/radialleg.jpeg' | relative_url }}" alt="Radial Leg Arrangement" style="width: 100%; height: 250px; object-fit: cover; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/landing-gear/radialleg.jpeg' | relative_url }}')">
    <p style="font-size: 0.9em; color: #555; margin-top: 15px; line-height: 1.6; text-align: left;">
      <span style="display: block; font-style: italic; color: #666; margin-bottom: 5px;">*Fig. 2: Radial Leg Arrangement Model*</span>
      Legs are attached radially to distribute impact evenly, offering superior shock absorption and landing stability.
    </p>
  </div>
</div>

#### 3. Performance
Drop tests demonstrated that a 1.5kg model could reliably land from a height of 1m. Furthermore, when the drop height was kept under 50cm, the system successfully supported a heavier 3kg model. The radial leg arrangement also proved to have superior buffering performance compared to a straight, 11-shaped arrangement.

#### 4. Validation
Drop experiments were conducted using a PASCO motion (ultrasonic) sensor to continuously measure position, velocity, and acceleration. The results verified that the mechanism successfully generated a damped oscillation, which effectively prolonged the impact time and significantly reduced the overall impact force.

<div style="text-align: center; margin-top: 20px; margin-bottom: 30px;">
  <img src="{{ '/_assets/photos/landing-gear/expsetup.jpeg' | relative_url }}" alt="Setup for the Drop Experiment" style="width: 60%; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/landing-gear/expsetup.jpeg' | relative_url }}')">
  <p style="font-size: 0.9em; color: #555; margin-top: 15px; line-height: 1.6; text-align: center; max-width: 80%; margin-left: auto; margin-right: auto;">
    <span style="display: block; font-style: italic; color: #666; margin-bottom: 5px;">*Fig. 3: Drop Experiment Setup*</span>
    A central rod ensures a straight vertical drop, while weights are distributed circularly to prevent structural damage.
  </p>
</div>

---

<div style="text-align: center; margin-top: 40px;">
  <a href="/_assets/pdf/DroneLandingGear_Cat.pdf" target="_blank" style="display: inline-block; padding: 12px 24px; background-color: #3b82f6; color: white; text-decoration: none; border-radius: 8px; font-weight: bold; transition: background-color 0.2s; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
    📄 Download Full Research Paper (PDF, Korean)
  </a>
</div>

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