---
layout: archive
title: "Research"
permalink: /research/
author_profile: false
redirect_from:
  - /research
---


{% include base_path %}


Representation learning in reinforcement learning
======

Stochastic nonlinear control, even with known dynamics and rewards, remains a difficult problem with limited efficient algorithms. While deep reinforcement learning (RL) has advanced the field, these methods often lack rigorous theoretical guarantees and require complex tuning. In this line of work, we take a representation-based viewpoint to reinforcement learning, by using finite-dimensional spectral features for representing value functions via computing spectral decompositions of the transition operator. This approach, based on recent work in linear MDPs, enables more efficient single-agent RL algorithms with strong theoretical guarantees. Beyond the single-agent setting, our approach also scales to continuous state-action network multiagent control, demonstrating success in applications such as Kuramoto frequency synchronization and building heating control. 
<!-- I believe that representation learning has great potential to significantly improve sample efficiency in reinforcement learning, and there are many open questions both theoretically and in practice which I am currently actively exploring. For instance, can we design simple yet effective representation learning algorithms in the model-free case? How can we apply such methods to enable more tractable control in high-dimensional problems such as fluid control?   -->

**Selected work**:

<div style="display: flex; align-items: center;">
  <!-- Videos on the left -->
  <div style="display:flex; flex-shrink: 0; margin-right: 20px;">

  <figure style="display: grid; grid-template-rows: auto 1fr auto; text-align: center; height: 80px;">
    <video id="koopman" width="100" height="60" autoplay muted loop>
      <source src="{{ base_path }}/videos/koopman_3x_cropped.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="grid-row: 3;">Koopman</figcaption>
  </figure>

  <figure style="display: grid; grid-template-rows: auto 1fr auto; text-align: center; height: 80px;">
    <video id="ilqr" width="100" height="60" autoplay muted loop>
      <source src="{{ base_path }}/videos/ilqr_3x_cropped.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="grid-row: 3;">iLQR</figcaption>
  </figure>

  <figure style="display: grid; grid-template-rows: auto 1fr auto; text-align: center; height: 80px;">
    <video id="spectral" width="100" height="60" autoplay muted loop>
      <source src="{{ base_path }}/videos/sdec_3x_cropped.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="grid-row: 3;"><b>Spectral-rep</b></figcaption>
  </figure>

  </div>
  <!-- Text on the right -->
  <div>
    <h3 style="margin: 0;"><a href="https://arxiv.org/abs/2304.03907">Stochastic nonlinear nontrol via finite-dimensional spectral dynamic embedding</a></h3>
    <p style="margin: 0;"> <strong>Zhaolin Ren</strong>*, Tongzheng Ren*, Haitong Ma, Na Li, Dai Bo</p>
    <p style="margin: 0;"><em> Transactions on Automatic Control, 2025.</em></p>
  </div>
</div>


<div style="display: flex; align-items: center;">
  <!-- Videos on the left -->
  <div style="display:flex; flex-shrink: 0; margin-right: 20px;">

  <figure style="display: grid; grid-template-rows: auto 1fr auto; text-align: center; height: 120px;">
    <video id="kuramoto" width="300" height="100" autoplay muted loop>
      <source src="{{ base_path }}/videos/kuramoto_rsvd_2_cropped.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="grid-row: 3;">Kuramoto synchronization</figcaption>
  </figure>

  </div>
  <!-- Text on the right -->
  <div>
    <h3 style="margin: 0;"><a href="https://arxiv.org/abs/2410.17221">Scalable spectral representations for multi-agent reinforcement learning in network MDPs</a></h3>
    <p style="margin: 0;"> <strong>Zhaolin Ren</strong>*, Runyu Zhang*, Dai Bo, Na Li</p>
    <p style="margin: 0;"><em>AISTATS 2025.</em></p>
  </div>
</div>


Theory and practice of model-free optimization 
======

In many real-life problems, we may only be able to learn about a system through limited interactive feedback, with no knowledge of the exact form of the underlying dynamics. In optimization and control problems involving such systems, we do not have direct access to the gradients underpinning these problems, making it difficult for us to apply plug-and-play gradient-descent/ascent type methods which are the workhorse of modern machine learning. Instead, to optimize and control these systems, we need to leverage gradient-free optimization techniques, such as zeroth-order optimization and Bayesian optimization. For zeroth-order optimization, I have worked on theoretical guarantees for the ability of two-point zeroth-order algorithms to escape saddle points. This work was inspired by my interest in better understanding the convergence properties of two-point zeroth order gradient estimation, which is an important method often used in practice. For Bayesian optimization (BO), sample efficiency is often paramount as data collection can be expensive both in terms of time and cost. Can we leverage parallel/batch learning techniques to enable more efficient learning? In contrast to standard BO, batch BO presents both advantages (sampling more points per round) and questions (how to intelligently choose the points to sample every round whilst avoiding redundancy?). However, there is a dearth of efficient yet provable batch Bayesian optimization algorithms. To overcome this, I designed a novel batch BO algorithm, called TS-RSR, which samples a batch at each round by minimizing a term which refer to as TS-RSR (Thompson Sampling - Regret to Sigma Ratio). It avoids several of the practical problems faced by existing theoretical-backed algorithms such as Batch Upper-Confidence Bound (BUCB) and Thompson Sampling (TS), such as sensitivity to hyperparameter tuning and lack of redundancy avoidance, but also satisfies a rigorous convergence bound. In practice, we found that our algorithm achieves state-of-the-art performance on a range of synthetic and realistic test functions. 

**Selected work**:
<div style="display: flex; align-items: center; margin: 0; padding: 0;">
  <!-- Image on the left -->
  <div style="display:flex; flex-shrink: 1; margin-right: 20px; margin:0 padding:0;">
    <img src="{{ base_path }}/images/ts_rsr_schematics_v2.png" alt="tsRSR_schematics" style="width: 400px; height: 300px; object-fit: contain;">
  </div>
  <!-- Text on the right -->
  <div>
    <h3 style="margin: 0;"><a href="https://arxiv.org/abs/2403.04764">TS-RSR: A provably efficient approach for batch bayesian optimization </a></h3>
    <p style="margin: 0;"> <strong>Zhaolin Ren</strong>, Na Li</p>
    <p style="margin: 0;"><em>SIAM Journal for Optimization, 2025.</em></p>
  </div>
</div>

<div style="display: flex; align-items: center; margin: 0; padding: 0;">
  <!-- Image on the left -->
  <div style="display:flex; flex-shrink: 1; margin-right: 20px; margin:0 padding:0;">
    <img src="{{ base_path }}/images/zo_convergence.png" alt="zo_convergence" style="width: 500px; height: 300px; object-fit: contain;">
  </div>
  <!-- Text on the right -->
  <div>
    <h3 style="margin: 0;"><a href="https://arxiv.org/abs/2209.13555">Escaping saddle points in zeroth-order optimization: the power of two-point estimators </a></h3>
    <p style="margin: 0;"> <strong>Zhaolin Ren</strong>, Yujie Tang, Na Li</p>
    <p style="margin: 0;"><em>International Conference on Machine Learning 2023.</em></p>
  </div>
</div>

