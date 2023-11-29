---
toc: true
author_profile: true
title: "LANL"
excerpt: "Research I did as an intern at Los Alamos National Lab!"
header:
    teaser: /assets/images/lanl_logo.png
read_time: true
---  

At Los Alamos National Lab, I worked with two staff scientists on a project examining multiphase flow simulations in subsurface fractures.

#### Problem & Motivation

Multiphase flow properties of fractures are important for a variety of engineering applications, one being the injection and storage of fluid CO<sub>2</sub> underground. Lattice Boltzmann (LBM) simulations can be used to study these properties, but these physics-based simulations require high-performance computing resources and are limited in their domain size.  

We present a physics-constrained **deep convolutional neural network (CNN)** that trains on a few LBM simulations and can quickly and accurately predict the displacement of water by supercritical CO<sub>2</sub> through time with **95% accuracy**. The goal is to map the characteristics of a 3D fracture to the position of an injected fluid mass of CO<sub>2</sub> at multiple timesteps, interpolating between the original simulations with accurate ML predictions that take into account interfacial tension between fluids, fluid-solid interactions, and complex geometries.  

#### Methods 

![Workflow Diagram showing mapping of 3D simulations to 2D images.](/assets/images/workflow_chart.png)

#### Results 

Poster Presentation:
I presented this research at the American Geophysical Union Fall Meeting in Chicago, IL in 2022. The full poster presentation is shown below.

***Check out the poster here!***  

[![Poster Presentation](/assets/images/poster.png 'Poster Presentation')](/assets/files/symposium_poster.pdf)  


***Check out the*** [***full article***](https://www.mdpi.com/1996-1073/15/23/8871) ***published in Energies!***


<!-- ---
title: "Foo Bar Identity"
excerpt: "Foo Bar design system including logo mark, website design, and branding applications."
header:
  image: /assets/images/foo-bar-identity.jpg
sidebar:
  - title: "Role"
    image: http://placehold.it/350x250
    image_alt: "logo"
    text: "Designer, Front-End Developer"
  - title: "Responsibilities"
    text: "Reuters try PR stupid commenters should isn't a business model"
gallery:
  - url: /assets/images/unsplash-gallery-image-1.jpg
    image_path: assets/images/unsplash-gallery-image-1-th.jpg
    alt: "placeholder image 1"
  - url: /assets/images/unsplash-gallery-image-2.jpg
    image_path: assets/images/unsplash-gallery-image-2-th.jpg
    alt: "placeholder image 2"
  - url: /assets/images/unsplash-gallery-image-3.jpg
    image_path: assets/images/unsplash-gallery-image-3-th.jpg
    alt: "placeholder image 3"
--- -->