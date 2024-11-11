---
layout: page
title: Autonomous Driving
description: Applying AI experience in particle physics to other fun topics!
img: assets/img/AutonomousDriving.png
importance: 4
category: fun
related_publications: true
---

3D object detection at long-range is crucial for ensuring the safety and efficiency of self-driving vehicles, allowing them to accurately perceive and react to objects, obstacles, and potential hazards from a distance. This is especially relevant for heavy tracks which require longer reaction times. Most current state-of-the-art LiDAR based methods are range limited due to sparsity at long-range, which generates a form of domain gap between points closer to and farther away from the ego vehicle. Another related problem is the label imbalance for faraway objects, which inhibits the performance of Deep Neural Networks at long-range. In {% cite khoche2024longrange3dobjectdetection %} we investigate different ways to improve  long-range performance of current LiDAR-based 3D detectors.


<div class="row">
    <div class="col-sm mt-6 mt-md-2">
        {% include figure.liquid loading="eager" path="assets/img/mid_vs_long.png" title="Lidar sparsity" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-2 mt-md-2">
        {% include figure.liquid loading="eager" path="assets/img/GT_vs_range_coarsebins.png" title="Label imabalance" class="img-fluid rounded z-depth-1" %}
    </div>
<div class="caption">
Increased LiDAR sparsity with distance from ego vehicle is one of the major challenges facing long range (>100 m) 3D object detection. The left image shows shows that the two vehicles parked far away from the ego vehicle have fewer LiDAR points, as well as appear different compared to those parked nearby. The right image shows the label imbalance for objects at different ranges.
</div>


The large label imbalance between objects at long range (> 100 m) and mid range (< 100 m) is similar to that experienced in particle physics, where signals are much rare than backgrounds. To solve this issue we combine two 3D detection networks, referred to as range experts, one specializing at near to mid-range objects, and one at long-range 3D detection. To train a detector at long-range under a scarce label regime, we further weigh the loss according to the labelled point's distance from ego vehicle. This is very similar to the techniques exploited to train the parametrised Neural Networks capable of detecting rare multi-Higgs boson events in {% cite atlascollaboration2024searchresonancedecayingscalar %}.



