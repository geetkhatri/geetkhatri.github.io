---
layout: page
title: Image to Sound
description:
img: /assets/img/img2sound.png
importance: 1
github: https://github.com/geetkhatri/img2sound
---

For a given image, the algorithm creates a sound whose spectrogram looks like the image. It maps the pixel intensities of the image to the amplitudes of the spectrogram and randomizes the phase spectrum. Before the mapping, edge detection is applied to the image in order to make the sound more distinctive and the spectrogram’s features more pronounced.

I worked on this project for [Music Hack Day India, 2019](https://musichackdayindia.github.io){:target="\_blank"}, an event that focused on applications of technology in music and sound art.

The code is available on [GitHub](https://github.com/geetkhatri/img2sound){:target="_blank"}.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/img2sound.png' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    The original image (left) and the spectrogram of the generated audio (right)
    <p style="font-size: 0.9rem;font-style: italic;"><a href="https://www.flickr.com/photos/30924550@N04/29693349040"  target="_blank">"pattern"</a><span> by <a href="https://www.flickr.com/photos/30924550@N04"  target="_blank">walmarc04</a></span> is licensed under <a href="https://creativecommons.org/publicdomain/mark/1.0/?ref=ccsearch&atype=html" style="margin-right: 5px;" target="_blank">CC PDM 1.0</a><a href="https://creativecommons.org/publicdomain/mark/1.0/?ref=ccsearch&atype=html" target="_blank" rel="noopener noreferrer" style="display: inline-block;white-space: none;margin-top: 2px;margin-left: 3px;height: 22px !important;"><img style="height: inherit;margin-right: 3px;display: inline-block;" src="https://search.creativecommons.org/static/img/cc_icon.svg?image_id=f8d93a59-9810-4e9a-a6c1-1668b7d5c0ae" /><img style="height: inherit;margin-right: 3px;display: inline-block;" src="https://search.creativecommons.org/static/img/cc-pdm_icon.svg" /></a></p>
</div>

<div>
    <audio controls style="margin: 0 auto; display: block;">
        <source src="/assets/audio/img2sound-1.wav" type="audio/wav">
        Your browser does not support the audio element.
    </audio>
</div>

<br>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/img2sound-1.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/img2sound-2.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    <p style="font-size: 0.9rem;font-style: italic;"><a href="https://www.flickr.com/photos/93452909@N00/539670234"  target="_blank">"Interesting paving pattern - Ankara"</a><span> by <a href="https://www.flickr.com/photos/93452909@N00" target="_blank">brewbooks</a></span> is licensed under <a href="https://creativecommons.org/licenses/by-sa/2.0/?ref=ccsearch&atype=html" style="margin-right: 5px;" target="_blank">CC BY-SA 2.0</a><a href="https://creativecommons.org/licenses/by-sa/2.0/?ref=ccsearch&atype=html" target="_blank" rel="noopener noreferrer" style="display: inline-block;white-space: none;margin-top: 2px;margin-left: 3px;height: 22px !important;"><img style="height: inherit;margin-right: 3px;display: inline-block;" src="https://search.creativecommons.org/static/img/cc_icon.svg?image_id=34e387a7-233a-4143-98cb-0ddf6f5622b6" /><img style="height: inherit;margin-right: 3px;display: inline-block;" src="https://search.creativecommons.org/static/img/cc-by_icon.svg" /><img style="height: inherit;margin-right: 3px;display: inline-block;" src="https://search.creativecommons.org/static/img/cc-sa_icon.svg" /></a></p>
</div>

<div>
    <audio controls style="margin: 0 auto; display: block;">
        <source src="/assets/audio/img2sound-2.wav" type="audio/wav">
        Your browser does not support the audio element.
    </audio>
</div>

<br>

##### **Algorithm**
1. Convert the image to grayscale (if it's RGB)
2. Resize the image to a fixed height
3. Apply edge detection to the image so that the audio is more tone-like
4. Scale the pixel intensities of the image to control the loudness of the audio
5. Map the pixel intensities to the amplitudes of the spectrogram
6. Randomize the phase spectrum of the STFT
7. Compute the inverse STFT to produce samples of the audio
8. Generate an audio file from the samples
