---
layout: page
title: Searching for new Higgs bosons with AI
description: Parametrised Neural Network to search for 2 new particles of unkown masses at the LHC.

img: assets/img/event_display.png
importance: 1
category: work
related_publications: true
---

I was co-coordinator of the Search for two new Higgs bosons, X and S, with unkown masses that interact with the Standard-Model Higgs boson (H) {% cite atlascollaboration2024searchresonancedecayingscalar %}. I also designed the analysis strategy based on AI and developed the required <a href="https://github.com/LauraPereiraSanchez/Keras_NN">software</a>. In this post I present a short overview of the analysis with a focus on the AI strategy. Please read the full paper for details.

This analysis required a wide search for possible X and S masses (mX and mS), which made it especially challenging, as we had to scan a large mass range with fine enough granularity as to avoid any sensitivity gaps, but not too fine as to unnecessarily increase the “look-elsewhere effect”. This effect takes into account the larger probability that an excess is produced by a statistical fluctuation by looking at not one but many points.

<div class="row">
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/figaux_10.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/figaux_04c.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Phase space of masses of the X and S particles or parameters that are targeted in this search. In total 359 points. Right: Parametrised Neural Network targeting X and S masses of (1000, 500) GeV, respectively. Note that signal peaks towards one and all backgrounds peak towards zero. 
</div>

To overcome this challenge, we trained a parametrized neural network (PNN) to differentiate signal from background for a range of X and S masses. As shown in the figure, by specifying the targeted X and S masses, the PNN is able to separate a signal with those characteristics from background processes. This technique not only allowed us to probe a range of X and S masses with fine granularity, ensuring no signal was missed, but also enabled a clear understanding of the masses of the new bosons if found.

<div class="row">
    <div class="col-sm mt-0 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/figaux_05.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
<div class="caption">
  Parametrised Neural Network targeting X and S masses of (250, 100)	GeV, respectively.  Note	that only the signal with masses equal to the parameters set	by the PNN i.e.	PNN(250, 100) peaks towards 1, while backgrounds peak	towards	0. The signal with  X and S masses of (240, 100) GeV, which has similar parameters to those targeted by the PNN shows a flat distribution. This behaviour shows the resilience	of this	method to sensitivity gaps.
</div>

A total of 359 (mX, mS) pairs are probed, and an excess is found for a signal where mX is 575 GeV and mS is 200 GeV, with a local significance of 3.5 standard deviations (in yellow), as depicted in Figure 2. The global significance, which takes into account the look-elsewhere effect of all 359 points, reduces the excess to 2.0 standard deviations suggesting it is likely a statistical fluctuation.

<div class="row">
    <div class="col-sm mt-0 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/figaux_14.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-0 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/figaux_07.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
<div class="caption">
     Left: Observed significance for the full phase space. An excess is found for a signal where mX is 575 GeV and mS is 200 GeV, with a local significance of 3.5 standard deviations (in yellow).  The global significance, which takes into account the look-elsewhere effect of  all 359 points, reduces the excess to 2.0 standard deviations suggesting it is likely a statistical fluctuation. Right: The data to simulation comparison is shown for the PNN(575, 200) distribution where a local excess is observed. The most sensitive bin with PNN values close to 1 shows 6 events in data while only one events is expected from the background simulation.
</div>
