---
layout: page
title: Speech Enhancement Using Wiener Filtering and Pitch-Synchronous STFT Phase Reconstruction
description:
img: /assets/img/psr.png
importance: 2
github: https://github.com/geetkhatri/speech-enhancement-psr
---

The algorithm reconstructs the phase spectrum of the pitch-synchronous STFT of the speech signal. Certain properties of the pitch-synchronous STFT of harmonic signals make estimation of the phase spectrum faster and more accurate compared to phase reconstruction of constant–window size STFT. The magnitude spectrum is estimated using Wiener filtering.

[This document](https://github.com/geetkhatri/speech-enhancement-psr/blob/master/Speech%20Enhancement%20Using%20Wiener%20Filtering%20and%20PSR%20Phase%20Reconstruction.pdf){:target="_blank"} explains how the algorithm works and the motivation behind it. The code is available on [GitHub](https://github.com/geetkhatri/speech-enhancement-psr){:target="_blank"}.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/psr.png' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    The algorithm
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/psr-1.png' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/psr-2.png' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    The magnitude spectrum of a speech signal before and after application of the algorithm
</div>
