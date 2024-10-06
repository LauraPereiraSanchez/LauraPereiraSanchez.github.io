---
layout: page
title: Calibration of b-tagging algorithms
description: Correction of AI algorithm to account for the domain shift between data and simulation

img: assets/img/fig_lightSFs.png
importance: 1
category: work
related_publications: true
---

During 4 years I calibrated the AI algorithms used in ATLAS to find a specific type of particles, referred to as b-quarks, which leave a very specific mark in the detector. This process is absolutely crucial for many analyses and search or measure particles that decay to b-quarks, such as the Higgs boson!

These algorithms are trained on simulation and need to be calibrated to account for the domain shift between data and simulation so that they can be used accurately as a tool in data analysis. The calibration consists on performing a data analysis on a part of the phase space that is well known, and extract Scale Factors to correct the simulation to match the data. Given the repetitiveness of this process i.e. new algorithms and data often require calibration, my role consisted both on performind the calibration but also automatizing the process with bash scripts and the gitlab pipeline.

A general overview of the calibrations is shown in the poster I presented at <a href='https://indico.desy.de/event/28202/contributions/105247/attachments/67063/83289/FTAG_Poster_EPS21_LauraPereiraSanchez.pdf'>European Physics Society - High Energy Physics Conference 2021</a> and the respective proceeding {% cite PereiraSanchez:2022WW %}. In particular I calibrated the mis-identification rate, this is explained in detail in the poster that I presented at the <a href="https://agenda.infn.it/event/28874/contributions/168829/attachments/94031/128488/Final_poster.pdf">International Conference of High Energy Physics 2022</a>, and the journal article that I co-wrote {% cite ATLAS:2023lwk %}.

<div class="row">
    <div class="col-sm mt-0 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/fig_lightSFs.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
<div class="caption">
     The DL1r algorithm is a Neural Network capable of distinguishing b-quarks from other particles. The Scale Factors shown in this image account for the domain ship between data and simulation of the DL1r algorithm when selecting a sample enriched with at least 85% but less than 77% of b-quarks in the distirbution. The algorithm is calibrated also as a function of the jet pT, a variable that is particularly sensitive to the domain shift.
</div>
