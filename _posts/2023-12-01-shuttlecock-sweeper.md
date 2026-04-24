---
layout: post
title: "Automatic Shuttlecock Classification & Arrangement Sweeper"
---

### Overview
A mechanical sweeper designed to automatically collect, evaluate, and arrange badminton shuttlecocks using a wheel-driven conveyor system and optical sensors. 

### Key Highlights
* **Problem:** Manually collecting and sorting damaged shuttlecocks after badminton practice is inefficient, time-consuming, and physically demanding. 
* **Mechanical Design:** Engineered a wheel-powered conveyor belt system with brush-type propellers to sweep and lift shuttlecocks without requiring an external power source for mobility.
* **Smart Classification:** Developed an Arduino-controlled sorting module utilizing 16 IR light sensors to evaluate the structural integrity of shuttlecock feathers, automatically separating damaged units from reusable ones. 
* **Validation:** Conducted extensive A/B testing, focus group interviews, and competitive analysis against existing commercial products, demonstrating superior cost-effectiveness and user convenience. 

### Tech Stack & Fabrication
* SolidWorks (CAD & Mechanism Design) 
* Arduino / C++ (Sensor integration & Motor control) 
* Processing / Java (Data Visualization)
* 3D Printing & Aluminum Profile Assembly

<br>

<div style="display: flex; justify-content: space-between; gap: 10px; margin-bottom: 20px;">
  <img src="{{ '/_assets/photos/shuttlecock-sweeper/prototype_left.png' | relative_url }}" alt="Prototype Left" style="width: 32%; height: 200px; object-fit: cover; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/shuttlecock-sweeper/prototype_left.png' | relative_url }}')">
  <img src="{{ '/_assets/photos/shuttlecock-sweeper/prototype_back.png' | relative_url }}" alt="Prototype Back" style="width: 32%; height: 200px; object-fit: cover; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/shuttlecock-sweeper/prototype_back.png' | relative_url }}')">
  <img src="{{ '/_assets/photos/shuttlecock-sweeper/prototype_top.png' | relative_url }}" alt="Prototype Top" style="width: 32%; height: 200px; object-fit: cover; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/shuttlecock-sweeper/prototype_top.png' | relative_url }}')">
</div>

<img src="{{ '/_assets/photos/shuttlecock-sweeper/CADAssembly.png' | relative_url }}" alt="CAD Assembly" style="width: 50%; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s; margin-bottom: 20px;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/shuttlecock-sweeper/CADAssembly.png' | relative_url }}')">

<img src="{{ '/_assets/photos/shuttlecock-sweeper/datavisualize.jpeg' | relative_url }}" alt="Data Visualization" style="width: 100%; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s; margin-bottom: 20px;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/shuttlecock-sweeper/datavisualize.jpeg' | relative_url }}')">

<div style="display: flex; gap: 20px; margin-bottom: 20px;">
  <video controls style="flex: 1; width: 50%; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
    <source src="{{ '/_assets/videos/shuttlecock-sweeper/test1.MP4' | relative_url }}" type="video/mp4">
    브라우저가 동영상을 지원하지 않습니다.
  </video>

  <video controls style="flex: 1; width: 50%; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
    <source src="{{ '/_assets/videos/shuttlecock-sweeper/test2.MP4' | relative_url }}" type="video/mp4">
    브라우저가 동영상을 지원하지 않습니다.
  </video>
</div>

<br>

<a href="{{ '/_assets/pdf/Final report ME340 group7.pdf' | relative_url }}" target="_blank" style="display: inline-block; margin-top: 20px; padding: 10px 20px; background-color: #3b82f6; color: white; text-decoration: none; border-radius: 8px; font-weight: bold; transition: background-color 0.2s;">
  📄 Download ME340 Final Report (PDF)
</a>

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
