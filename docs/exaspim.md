---
layout: page
title: "ExA-SPIM"
permalink: /exaspim/
nav_exclude: true
---
![ExA-SPIM Photo](/../images/LowRes.jpg){: width="650"}


The expansion assisted selective plane illumination microscope (ExA-SPIM) is a microscope developed at the Allen Institute for Neural dynamics by a team lead by Adam Glaser. The aim of the ExA-SPIM project is to image large expanded mammalian brain tissue for the purpose of full neuron reconstruction.

Reconstructing full mammalian neurons requires imaging full brain volumes at high resolutions to make out axons that can be thinner than 100 nm but extend centimers across the brain. Life science imaging objectives limit this possiblity due to tradeoffs between resolution, field of view (FOV), and working distance. As such, previous approaches have relied on tissue sectioning and extensive tiling. The ExA-SPIM leverages expansion microscopy along with a lens from the semiconductor inspection and metrology industry that has a high numerical aperture (NA), large FOV, and far working distance.

![Alpha Scope Diagram]({{ "/images/alpha-diagram.png" | absolute_url }}){: width="320" }
![Alpha Scope Diagram 2]({{ "/images/alpha-diagram2.png" | absolute_url }}){: width="320" }
<br> *Prototype ExA-SPIM optical path diagram and photograph*

A prototype system was developed in 2023, but it used off-the-shelf components that resulted in design trade-offs and performance limitations. I joined the Allen Institute at the beginning of the summer in 2024 as the design for an improved ExA-SPIM microscope was being finalized. The new design is based on custom machined parts that are precisely located relative to eachother using dowll pins. This makes the construction and alignment easier and more repeatable. The optical limitations of the prototype are addressed with a custom field curvature-corrected illumination objective and a custom acylindrical Powell lens that results in a uniform illumination profile. Additionally, the new design allows for dual sided illumination and more flexibility with maneuvering the sample.

![ExA-SPIM Cad](/images/beta.png){: width="550" }
<br> *Redesigned ExA-SPIM CAD showing features and improvements*

Joining this project was somewhat of a pivot into engineering for me, but I was able to get caught up on the necessary information about optics, mechanical construction, and microscope software and hardware. As we prepared to build three ExA-SPIM microscopes, I was able to learn a lot of new skills such as soldering custom control cables, simple CAD design projects, part modifications using a manual mill, specifiying/purchasing parts, and lots of organizing and cataloguing screws to prepare for the builds. 
{% include video.html
   src="/videos/timelapse.mp4"
   caption="Timelapse of an ExA-SPIM system being built"
   autoplay=false
%}

We built three redesigned systems total, but after finishing the first one, we realized that some aspects of the mechanical design needed to be reworked more to allow for additional degrees of freedom in the illumination path alignment. I employed temporary fixes with manual machining and 3D printed parts and then ordered new custom machined pieces that would fix the issues and complete the microscopes with both sides of illumination. With the subsequent builds 

There are several limitations and tradeoffs with parts used in our configuration of the microscope, chiefly related to the high-powered free-space lasers from Coherent, and the Powell lenses that generate the sheet. As such, one of my main roles for the past year has been troubleshooting and perfecting the design, optics, alignment, and acquisition parameters of the microscope to counteract or work within these limitations. 

After being constructed, aligned, and optimized, the microscopes are capable of imaging whole 3x expanded mouse brains in under one day using 20 tiles with negligable aberrations. The native optical resolution is around 1x1x3.5 µm; combined with the 3x tissue expansion factor, this is more than enough to trace full neurons in sparsely labeled samples.
{% include video.html
   src="/videos/neuron-trace-trim.mp4"
   caption="Demonstration of neuron tracing alongside reconstructed neuron"
   autoplay=false
%}

In addition to the three ExA-SPIM microscopes which use a 5x zoom imaging objective, we have designed and built a lower resolution microscope using a 1x imaging objective and a greatly expanded light-sheet that can image 3x expanded mouse brains in a single tile in less than 30 minutes. This microscope is used for screening brains and doing simple experiments that don't require high resolution.
{% include video.html
   src="/videos/1x-sheet.mp4"
   caption="Low-res 1x scope light-sheet scanning through expanded mouse brain"
   autoplay=false
%}

We are also in the process of prepairing to build a higher resolution microscope (ExA-SPIM 2.0) that will use four cameras to simulatneously image four color channels. This will be used as part of a large proteomics project at the Allen Institute led by Tim Wang.

# Experiments
We are currently preparing a manuscript for the redesigned ExA-SPIM system. It will detail the specs and characterization of the microscope and the custom optical components contained within it, as well as discussion on alternative configurations of the microscope that can avoid the tradoffs of the Powell lenses and free-space lasers. 

We will additionally showcase experiments related to tissue photobleaching and the attenuating effects of tissue expansion factor on image aberration. 

<br>

# Documentation
The ExA-SPIM project is open-source and meant to be disseminated for others to build. It is a unique microscope that allows for fast volumetric imaging of large samples, and could have a variety of different use cases.

Detailed instructions for building and setting up an ExA-SPIM microscope can be found [here](https://github.com/KaelinWulf/ExA-SPIM_2.0_Documentation) (work in progress)

The custom acquisition software can be found [here](https://github.com/AllenNeuralDynamics/exa-spim-control)

The image acquisition protocol can be found [here](https://www.protocols.io/view/exa-spim-imaging-protocol-g4xwbyxpf)

The paper on the prototype ExA-SPIM and the general project pipeline can be found [here](https://elifesciences.org/reviewed-preprints/91979v3)


