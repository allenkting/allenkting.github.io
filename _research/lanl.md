---
toc: true
author_profile: true
title: "CNNs for Multiphase Flow"
excerpt: "Research I did as an intern at Los Alamos National Lab!"
header:
    teaser: /assets/images/sim_3d.png
read_time: true
order: 1
---  

At Los Alamos National Lab, I worked with two staff scientists on a project examining multiphase flow simulations in subsurface fractures. This is an abridged summary of the [**full article**](https://www.mdpi.com/1996-1073/15/23/8871) published in *Energies*!

#### Problem & Motivation

Multiphase flow properties of fractures are important for a variety of engineering applications, one being the injection and storage of fluid CO<sub>2</sub> underground. Lattice Boltzmann (LBM) simulations can be used to study these properties, but these physics-based simulations require high-performance computing resources and are limited in their domain size.  

We present a physics-constrained **deep convolutional neural network (CNN)** that trains on a few LBM simulations and can quickly and accurately predict the displacement of water by supercritical CO<sub>2</sub> through time with **95% accuracy**. The goal is to map the characteristics of a 3D fracture to the position of an injected fluid mass of CO<sub>2</sub> at multiple timesteps, interpolating between the original simulations with accurate ML predictions that take into account interfacial tension between fluids, fluid-solid interactions, and complex geometries.  

#### Methods 

<figure class="align-center">
  <img src="{{ site.url }}{{ site.baseurl }}/assets/images/workflow_chart.png" alt="">
  <figcaption align="center">Workflow Diagram showing mapping of 3D simulations to 2D images.</figcaption>
</figure>  

To make computations lightweight and scalable to different fracture sizes, we design a workflow to project the input 3D simulation into two 2D maps that represent the top and bottom surfaces of the fracture. For each timestep, we then use the fracture shape to output two 2D maps, representing the the position of the top and bottom of the menisci of the fluid CO<sub>2</sub> with respect to the fracture's aperture size. Finally, the predicted 3D simulation of the CO<sub>2</sub> (red) displacing water (blue) is reconstructed. For details on the convollutional neural network architecture, please read section 3 in the paper.

#### Results 

We tested our model using 40 timesteps from two fractures which had never been seen by the machine learning algorithm. Overall, the shape of the plume and phase distributions are accurately predicted. In general, the algorithm predicts sharper interfaces than the simulation, but if these model outputs were used as an input into an LBM simulation, capillary forces would immediately smooth this result. In this way, a coupled LBM and machine learning scheme could be devised where the LBM resolves the interface from the algorithm at certain intervals. The end result makes 3D multiphase flow predictions easy with applied boundary conditions. An example of one prediction that shows the model's accuracy in 3D is shown below.  

<figure class="align-center">
  <img src="{{ site.url }}{{ site.baseurl }}/assets/images/pred_3d.png" alt="">
  <figcaption align="center">Ground Truth Simulation vs. 3D Prediction.</figcaption>
</figure>  

Multiphase flow in fractures is important to many engineering applications, and for future work, we plan to create a larger dataset of simulations with different fractures and conditions to help further develop the capabilities of our machine learning algorithms.  

#### AGU Poster (2022)
I presented this research at the American Geophysical Union Fall Meeting in Chicago, IL in 2022. The full poster presentation is linked in the image below.

[![Poster Presentation](/assets/images/poster.png 'Poster Presentation')](/assets/files/symposium_poster.pdf)  

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