---
layout: page
title: "ExA-SPIM"
permalink: /exaspim/
nav_exclude: true
---
![ExA-SPIM Photo](/../images/IMG_2282.jpg)

<br>

The expansion assisted selective plane illumination microscope (ExA-SPIM) is a microscope developed at the Allen Institute for Neural dynamics. The aim of the ExA-SPIM project is to image large expanded mammalian brain tissue for the purpose of full neuron reconstruction.

Reconstructing full mammalian neurons requires imaging full brain volumes at high resolutions to make out axons that can be thinner than 100 nm but extend centimers across the brain. Life science imaging objectives limit this possiblity due to tradeoffs between resolution, field of view (FOV), and working distance. As such, previous approaches have relied on tissue sectioning and extensive tiling. The ExA-SPIM leverages expansion microscopy along with a lens from the semiconductor inspection and metrology industry that has a high numerical aperture (NA), large FOV, and far working distance.

![Alpha Scope Diagram]({{ "/images/alpha-diagram.png" | absolute_url }}){: width="340" }
![Alpha Scope Diagram 2]({{ "/images/alpha-diagram2.png" | absolute_url }}){: width="340" }
<br> *Prototype ExA-SPIM optical path diagram and photograph*

A prototype system was developed in 2023, but it used off-the-shelf components that resulted in design trade-offs and performance limitations. I joined the Allen Institute at the beginning of the summer in 2024 as the design for an improved ExA-SPIM microscope was being finalized. The new design is based on custom machined parts that are precisely located relative to eachother using dowll pins. This makes the construction and alignment easier and more repeatable. The optical limitations of the prototype are addressed with a custom field curvature-corrected illumination objective and a custom acylindrical Powell lens that results in a uniform illumination profile. Additionally, the new design allows for dual sided illumination and more flexibility with maneuvering the sample.
![ExA-SPIM Beta](/images/.jpg)
<br> *Redesigned ExA-SPIM CAD showing features and improvements*

Because working on this project was somewhat of a pivot into engineering for me, I started off by getting caught up on the necessary information about optics, mechanical construction, and microscope software and hardware. As we prepared to build three ExA-SPIM microscopes, I was able to learn a lot of new skills. I began with soldering custom control cables, simple CAD design projects, part modifications using a manual mill, specifiying/purchasing parts, and lots and lots of organizing and cataloguing screws to prepare for the builds. 
{% include video.html
   src="/images/build_timelapse.mp4"
   caption="Timelapse of the third ExA-SPIM Beta system being built"
   autoplay=false
%}



<br>

# Documentation

Detailed instructions for building and setting up an ExA-SPIM microscope can be found [here](https://github.com/KaelinWulf/ExA-SPIM_2.0_Documentation)

The custom acquisition software can be found [here](https://github.com/AllenNeuralDynamics/exa-spim-control)

The image acquisition protocol can be found [here](https://www.protocols.io/view/exa-spim-imaging-protocol-g4xwbyxpf)
