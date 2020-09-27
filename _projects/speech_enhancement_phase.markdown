---
layout: page
title: Speech Enhancement Through STFT Phase Reconstruction
description: 
img: /assets/img/speech-enhancement-phase.png
importance: 4
---

The algorithm estimates the phase spectrum of the underlying speech signal. The voiced part of the speech is modeled using the harmonic model. As a prerequisite step, the fundamental frequencies of the voiced speech are estimated. The phase reconstruction algorithm makes it possible to enhance speech using only the fundamental frequencies and the noisy signal.

I later improved upon this algorithm by using pitch-synchronous window size for STFT instead of constant window size. This made the estimation of phase spectrum faster and more accurate. Visit the [project's page](/projects/speech_enhancement_psr) to see how it works.
