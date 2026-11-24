---
layout: post
title: "Automatic Shuttlecock Classification & Arrangement Sweeper"
---

### Overview
A mechanical sweeper designed to automatically collect, evaluate, and arrange badminton shuttlecocks using a wheel-driven conveyor system and optical sensors.

---

### Key Highlights

#### 1. Problem
Manually collecting and sorting damaged shuttlecocks after badminton practice is inefficient, time-consuming, and physically demanding.

#### 2. Mechanical Design
Engineered a wheel-powered conveyor belt system with brush-type propellers to sweep and lift shuttlecocks without requiring an external power source for mobility.

<div style="text-align: center; margin-top: 20px; margin-bottom: 30px;">
  <img src="{{ '/_assets/photos/shuttlecock-sweeper/CADAssembly.png' | relative_url }}" alt="CAD Assembly" style="width: 40%; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/shuttlecock-sweeper/CADAssembly.png' | relative_url }}')">
  <p style="font-size: 0.9em; color: #555; margin-top: 15px; line-height: 1.6; text-align: center; max-width: 80%; margin-left: auto; margin-right: auto;">
    <span style="display: block; font-style: italic; color: #666; margin-bottom: 5px;">Fig. 1: CAD Assembly</span>
    CAD assembly of the sweeping mechanism.
  </p>
</div>

#### 3. Smart Classification
Developed an Arduino-controlled sorting module utilizing 16 IR light sensors to evaluate the structural integrity of shuttlecock feathers, automatically separating damaged units from reusable ones.

<div style="text-align: center; margin-top: 20px; margin-bottom: 30px;">
  <img src="{{ '/_assets/photos/shuttlecock-sweeper/datavisualize.jpeg' | relative_url }}" alt="Data Visualization" style="width: 100%; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/shuttlecock-sweeper/datavisualize.jpeg' | relative_url }}')">
  <p style="font-size: 0.9em; color: #555; margin-top: 15px; line-height: 1.6; text-align: center; max-width: 80%; margin-left: auto; margin-right: auto;">
    <span style="display: block; font-style: italic; color: #666; margin-bottom: 5px;">Fig. 2: Feather Integrity Evaluation</span>
    Data visualization of light transmission used to evaluate feather integrity.
  </p>
</div>

#### 4. Tech Stack & Fabrication
* SolidWorks (CAD & Mechanism Design)
* Arduino / C++ (Sensor integration & Motor control)
* 3D Printing & Aluminum Profile Assembly

<div style="display: flex; justify-content: space-between; gap: 10px; margin-top: 20px;">
  <img src="{{ '/_assets/photos/shuttlecock-sweeper/prototype_left.png' | relative_url }}" alt="Prototype Left" style="width: 32%; height: 200px; object-fit: cover; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/shuttlecock-sweeper/prototype_left.png' | relative_url }}')">
  <img src="{{ '/_assets/photos/shuttlecock-sweeper/prototype_back.png' | relative_url }}" alt="Prototype Back" style="width: 32%; height: 200px; object-fit: cover; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/shuttlecock-sweeper/prototype_back.png' | relative_url }}')">
  <img src="{{ '/_assets/photos/shuttlecock-sweeper/prototype_top.png' | relative_url }}" alt="Prototype Top" style="width: 32%; height: 200px; object-fit: cover; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/shuttlecock-sweeper/prototype_top.png' | relative_url }}')">
</div>
<p style="font-size: 0.9em; color: #555; margin-top: 15px; margin-bottom: 30px; line-height: 1.6; text-align: center;">
  <span style="display: block; font-style: italic; color: #666; margin-bottom: 5px;">Fig. 3: Assembled Prototype</span>
  The 3D-printed and fully assembled prototype from various angles.
</p>

#### 5. Validation
Conducted extensive A/B testing, focus group interviews, and competitive analysis against existing commercial products, demonstrating superior cost-effectiveness and user convenience.

<div style="display: flex; gap: 20px; margin-top: 20px;">
  <video controls style="flex: 1; width: 50%; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
    <source src="{{ '/_assets/videos/shuttlecock-sweeper/test1.mp4' | relative_url }}" type="video/mp4">
    Your browser does not support the video tag.
  </video>
  <video controls style="flex: 1; width: 50%; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
    <source src="{{ '/_assets/videos/shuttlecock-sweeper/test2.MP4' | relative_url }}" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</div>
<p style="font-size: 0.9em; color: #555; margin-top: 15px; margin-bottom: 30px; line-height: 1.6; text-align: center;">
  <span style="display: block; font-style: italic; color: #666; margin-bottom: 5px;">Fig. 4: Performance Validation</span>
  Test videos showing the shuttlecock sweeping and lifting process.
</p>

---

<div style="text-align: center; margin-top: 40px;">
  <a href="{{ '/_assets/pdf/Final report ME340 group7.pdf' | relative_url }}" target="_blank" style="display: inline-block; padding: 12px 24px; background-color: #2f5d8a; color: white; text-decoration: none; border-radius: 8px; font-weight: bold; transition: background-color 0.2s; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
    📄 Download ME340 Final Report (PDF)
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
