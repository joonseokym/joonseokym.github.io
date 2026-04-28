---
layout: post
title: "Optimization of Deep Reinforcement Learning for Control Problems"
---

### Overview
An intensive algorithmic research project focused on stabilizing and optimizing a Double Deep Q-Network (DDQN) agent to solve the CartPole control problem by systematically tuning hyperparameters[cite: 281, 282, 318].

---

### Key Highlights

#### 1. Problem
While Deep Reinforcement Learning (DRL) is a powerful tool for robotic control, models like Q-Networks often suffer from training instability and overestimation[cite: 296, 297]. Achieving fast, reliable, and consistent convergence requires rigorous tuning of the algorithm's hyperparameters, which is traditionally a highly heuristic and time-consuming process.

#### 2. Methodology & Optimization
Implemented a DDQN algorithm using Keras and the OpenAI Gym CartPole environment[cite: 313]. To maximize learning efficiency, an extensive A/B testing framework was constructed to systematically tune 11 distinct variables—including learning rate, epsilon decay, network depth, and activation functions[cite: 282, 321, 429]. Each variation was trained for 100 episodes to evaluate its impact on mean scores and standard deviation[cite: 282, 283].

<div style="text-align: center; margin-top: 20px; margin-bottom: 30px;">
  <img src="{{ '/_assets/photos/PreURP/Fig1.jpeg' | relative_url }}" alt="CartPole Simulation Environment" style="width: 50%; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/PreURP/Fig1.jpeg' | relative_url }}')">
  <p style="font-size: 0.9em; color: #555; margin-top: 15px; line-height: 1.6; text-align: center; max-width: 80%; margin-left: auto; margin-right: auto;">
    <span style="display: block; font-style: italic; color: #666; margin-bottom: 5px;">*Fig. 1: CartPole Simulation Environment*</span>
    The OpenAI Gym CartPole environment where the DDQN agent was trained to balance the pole by applying lateral forces to the cart.
  </p>
</div>

#### 3. Performance
Successfully identified the optimal combination of hyperparameters that maximized reward acquisition[cite: 314, 434]. The finely tuned architecture—utilizing 4 hidden layers, 24 nodes, a batch size of 32, the Nadam optimizer, a learning rate of 0.001, and the ReLU activation function—demonstrated highly stable and efficient policy learning compared to the baseline[cite: 527].

#### 4. Validation
Evaluated the optimized DDQN model against the default model over 1,000 episodes, tracking the number of trials required to achieve the success threshold (an average score > 195 over the last 100 episodes)[cite: 451, 455]. The default model required an average of 549.6 episodes to pass and failed to converge 40% of the time[cite: 457, 458]. In contrast, the optimized model achieved the threshold in just 151.8 episodes on average across all trials, representing a ~72% improvement in learning efficiency[cite: 458, 788].

<div style="display: flex; gap: 20px; margin-top: 20px; margin-bottom: 30px; align-items: flex-start;">
  <div style="flex: 1; text-align: center;">
    <img src="{{ '/_assets/photos/PreURP/Fig2.jpeg' | relative_url }}" alt="Default Model Performance" style="width: 100%; height: 250px; object-fit: cover; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/PreURP/Fig2.jpeg' | relative_url }}')">
    <p style="font-size: 0.9em; color: #555; margin-top: 15px; line-height: 1.6; text-align: left;">
      <span style="display: block; font-style: italic; color: #666; margin-bottom: 5px;">*Fig. 2: Default Model Learning Curve*</span>
      Graph of 1000 running episodes using the default parameters. Note the instability and failure of two trials to reach the threshold.
    </p>
  </div>
  <div style="flex: 1; text-align: center;">
    <img src="{{ '/_assets/photos/PreURP/Fig3.jpeg' | relative_url }}" alt="Optimized Model Performance" style="width: 100%; height: 250px; object-fit: cover; border-radius: 8px; cursor: zoom-in; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.02)'" onmouseout="this.style.transform='scale(1)'" onclick="openModal('{{ '/_assets/photos/PreURP/Fig3.jpeg' | relative_url }}')">
    <p style="font-size: 0.9em; color: #555; margin-top: 15px; line-height: 1.6; text-align: left;">
      <span style="display: block; font-style: italic; color: #666; margin-bottom: 5px;">*Fig. 3: Optimized Model Learning Curve*</span>
      Graph of 1000 running episodes using the tuned hyperparameters. Convergence is much faster, achieving stability in an average of 151.8 episodes.
    </p>
  </div>
</div>

---

<div style="text-align: center; margin-top: 40px;">
  <a href="{{ '/_assets/pdf/preURP_JoonseoKym.pdf' | relative_url }}" target="_blank" style="display: inline-block; padding: 12px 24px; background-color: #3b82f6; color: white; text-decoration: none; border-radius: 8px; font-weight: bold; transition: background-color 0.2s; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
    📄 Download Full Research Report (PDF, Korean)
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
