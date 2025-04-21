---
# You can also start simply with 'default'
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: /sundog.jpg
# some information about your slides (markdown enabled)
title: Seminar II
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: false
pointer: true

slideNumber: true
---

## Lattice Boltzmann Method for Electromagnetic Wave Scattering and Radiation Force Computation

Mohd Meraj Khan

<div class="text-3.5 mt-10">
  <b>Advisor:</b> Prof. Anubhab Roy <br>
  <b>Co-advisor:</b> Prof. Sumesh P. Thampi
</div>

<div class="mt-5 py-1" >
  Seminar II <br>
  February 5, 2025
</div>

<div class="flex items-center justify-center mt-10">
  <img src="/figures/IITM_Logo.png" alt="" class="h-20 w-20">
</div>

<div class="text-3 mt-10">
  Fluid Mechanics Division, Department of Applied Mechanics and Biomedical Engineering <br>
  Indian Institute of Technology Madras, Chennai, India, 600036
</div>

<div class="abs-br m-1.5 text-2">
  Background image: https://pixabay.com
</div>

---

## Scattering of EM Waves in Climate Studies

<!-- <div v-click="1" class="text-center mt-5">
Scattering of electromagnetic waves in nature
</div> -->

<div v-click="1" class="grid grid-cols-3 gap-15 mt-10">
  <figure class="text-center">
    <img src="/figures/scattering/sky_unsplash.jpg" alt="Image 1" class="w-full h-auto">
    <figcaption class="text-3 mt-2">
      Blue sky and white cloud
      <div class="text-2">(Source: unsplash.com)</div>
    </figcaption>
  </figure>
  
  <figure class="text-center">
    <img src="/figures/scattering/rainbow_unsplash.jpg" alt="Image 2" class="w-full h-auto">
    <figcaption class="text-3 mt-2">
      Rainbow
      <div class="text-2">(Source: unsplash.com)</div>
    </figcaption>
  </figure>
  
  <figure class="text-center">
    <img src="/figures/scattering/halo_wgrz.com.png" alt="Image 3" class="w-full h-auto">
    <figcaption class="text-3 mt-2">
      Sundog and Halo
      <div class="text-2">(Source: wgrz.org)</div>
    </figcaption>
  </figure>
</div>

<div v-click="2" class="grid grid-cols-3 gap-15 mt-10">
  <figure class="text-center">
    <img src="/figures/energy-budget.jpg" alt="Image 1" class="w-full h-auto">
    <figcaption class="text-3 mt-2">
      Radiation budget
      <div class="text-2">(Source: climatesight.org)</div>
    </figcaption>
  </figure>
  
  <figure class="text-center">
    <img src="/figures/dust_storm.png" alt="Image 2" class="w-full h-auto">
    <figcaption class="text-3 mt-2">
      Dust storm
      <div class="text-2">(Source: icarda.org)</div>
    </figcaption>
  </figure>
  
  <figure class="text-center">
    <img src="/figures/hydrometeor.jpg" alt="Image 3" class="w-full h-auto">
    <figcaption class="text-3 mt-2">
      Precipitation
      <div class="text-2">(Source: pexels.com)</div>
    </figcaption>
  </figure>
</div>

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---



## Scattering of EM Waves in Remote Sensing



<div class="grid grid-cols-2 gap-5 mt-5 justify-center">
  <figure v-click="1" class="flex flex-col items-center text-center">
    <div class="flex justify-center">
      <img src="/figures/aerosol.jpg" alt="Image 1" class="w-3/4 h-auto">
    </div>
    <figcaption class="text-3 mt-2">
      Aerosol in the atmosphere
      <div class="text-2">(Source: wikipedia.org)</div>
    </figcaption>
  </figure>
  
  <figure v-click="2" class="flex flex-col items-center text-center">
    <div class="flex justify-center">
      <img src="/figures/ocean_optics.jpg" alt="Image 2" class="w-3/4 h-auto">
    </div>
    <figcaption class="text-3 mt-2">
      Ocean optics
      <div class="text-2">(Source: wikipedia.org)</div>
    </figcaption>
  </figure>
</div>


<div class="grid grid-cols-2 gap-5 mt-3 justify-center">
  <figure v-click="3" class="flex flex-col items-center text-center">
    <div class="flex justify-center">
      <img src="/figures/soil_moisture.jpg" alt="Image 1" class="w-3/4 h-auto">
    </div>
    <figcaption class="text-3 mt-2">
      Soil moisture
      <div class="text-2">(Source: nasa.gov)</div>
    </figcaption>
  </figure>
  
  <figure v-click="4" class="flex flex-col items-center text-center">
    <div class="flex justify-center">
      <img src="/figures/cloud.jpg" alt="Image 2" class="w-3/4 h-auto">
    </div>
    <figcaption class="text-3 mt-2">
      Cloud composition
      <div class="text-2">(Source: unsplash.com)</div>
    </figcaption>
  </figure>
</div>


<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---


## Light Scattering by Ice Crystals


<div class="grid grid-cols-2 gap-5 mt-15 justify-center">
  <figure v-click="1" class="flex flex-col items-center text-center">
    <div class="flex justify-center">
      <img src="/figures/cirrus.jpg" alt="Image 1" class="w-auto h-auto">
    </div>
    <figcaption class="text-3 mt-2">
      Optical depth of cirrus cloud
      <div class="text-2">(Source: nasa.gov)</div>
    </figcaption>
  </figure>
  
  <figure v-click="2" class="flex flex-col items-center text-center">
    <div class="flex justify-center">
      <img src="/figures/Ice_crystals.jpeg" alt="Image 2" class="w-auto h-auto">
    </div>
    <figcaption class="text-3 mt-2">
      Size of ice crystals
      <div class="text-2">(Source: wikipedia.org)</div>
    </figcaption>
  </figure>
</div>





<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>



---

## Radiation Force

<v-drag  pos="852,15,94,_">
<figure class="text-center">
  <img src="/figures/rad_force/paramecium.png" alt="Image 2" class="w-full h-auto">
</figure>
</v-drag>

<div class="relative w-full mt-0">

<div class="absolute grid grid-cols-2 gap-15 place-items-center mt-15 ">
  <figure  class="text-center">
    <video autoplay loop muted class="w-full h-auto">
      <source src="/figures/rad_force/Particl_Trapping_Nobel_2018.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption class="text-3 mt-2">
      Trapping of the fat particle of a Paramecium
      <div class="text-2"> A Ashkin and J M Dziedzic (1989)</div>
    </figcaption>
  </figure>
  
  <figure v-click="1" class="text-center">
    <video autoplay loop muted class="w-full h-auto">
      <source src="/figures/rad_force/Particl_Manipulation_Nobel_2018.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption class="text-3 mt-2">
      Manipulation of a diatom
      <div class="text-2"> A Ashkin and J M Dziedzic (1989)</div>
    </figcaption>
  </figure>
</div>

</div>

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---

## Scattering Parameters

<table class="w-full border-collapse border text-3 mt-15">
  <thead>
    <tr class="bg-gray-100">
      <th class="border px-3 py-2">Application</th>
      <th class="border px-3 py-2">Size</th>
      <th class="border px-3 py-2">Wavelength</th>
      <th class="border px-3 py-2">Dielectric constant</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td class="border px-3 py-2">Light scattering by colloidal particles</td>
      <td class="border px-3 py-2">0.01 - 10 μm</td>
      <td class="border px-3 py-2">Visible Light (0.4-0.7 μm)</td>
      <td class="border px-3 py-2">Varies based on material</td>
    </tr>
    <tr>
      <td class="border px-3 py-2">Rainfall rate estimation</td>
      <td class="border px-3 py-2">0.01 - 0.7 cm</td>
      <td class="border px-3 py-2">Weather radars (1 - 30 cm)</td>
      <td class="border px-3 py-2"> 80 (for liquid water)</td>
    </tr>
    <tr>
      <td class="border px-3 py-2">Scattering by ice crystals</td>
      <td class="border px-3 py-2">A few micrometers to thousands of micrometers</td>
      <td class="border px-3 py-2">Ultraviolet to microwave regions</td>
      <td class="border px-3 py-2">3.15 (for ice)</td>
    </tr>
    <tr>
      <td class="border px-3 py-2">Particle traping and manipulations</td>
      <td class="border px-3 py-2">Micrometers</td>
      <td class="border px-3 py-2">Visible to IR</td>
      <td class="border px-3 py-2">Varies based on the specific biological material</td>
    </tr>

  </tbody>
</table>

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---

## Scattering Regimes

<div class="flex justify-center w-full mt-1">
  <div class="w-3/4 h-auto text-center">
    <img src="/figures/scattering_Schematic.png" alt="Image 1" class="mx-auto">
  </div>
</div>

<div class="grid grid-cols-3 gap-4 items-center">

<div v-click="1" style="display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center;">

$$ \frac{a}{\lambda} \ll 1, \varepsilon_r \sim 1$$
<span>Rayleigh regime</span>

</div>

<div v-click="3" style="display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center;">

$$ \frac{a}{\lambda} \sim 1$$
<span v-mark.circle.red="4" >Mie regime</span>

</div>

<div v-click="2" style="display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center;">

$$ \frac{a}{\lambda} \gg 1, \varepsilon_r \gg 1$$
<span>Geometric optics regime</span>

</div>
</div>

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---
layout: two-cols
layoutClass: gap-16
---

## Governing Equations

<div h-3 />

<div v-click>
Maxwell's equations in matter
$$
\begin{aligned}
\nabla \cdot \vec{D} &= \rho \\[1.0em]
\nabla \cdot \vec{B} &= 0 \\[1.0em]
\nabla \times \vec{E} &= -\frac{\partial\vec{B}}{\partial t} \\[1.0em]
\nabla \times \vec{H} &= \vec{J} + \frac{\partial\vec{D}}{\partial t}
\end{aligned}
$$
</div>

<div h-5 />

<div v-click>
For linear media
$$
\vec{E} = \frac{\vec{D}}{\varepsilon}  \hspace{10pt} \textcolor{gray}{and} \hspace{10pt} \vec{H} = \frac{\vec{B}}{\mu} 
$$

</div>

::right::

<div v-click class="mt-17">
Boundary conditions at the interface of two media
$$
\begin{aligned}
\hat{n} \cdot ( \vec{D}_{2} - \vec{D}_{1} ) &= \sigma \\[1.0em]
\hat{n} \times ( \vec{E}_{2} - \vec{E}_{1} ) &= 0 \\[1.0em]
\hat{n} \cdot \left( \vec{B}_2 -  \vec{B}_1 \right) &= 0 \\[1.0em]
\hat{n} \times ( \vec{H_2} - \vec{H_1}) &= \vec{K} \\[1.0em]
\end{aligned}
$$

</div>

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---

## Solution Methods

<table class="w-full border-collapse border text-center text-3.5 mt-5">
  <thead>
    <tr class="bg-gray-100">
      <th class="border px-3 py-2 text-center font-bold">Method Category</th>
      <th class="border px-3 py-2 text-center font-bold">Method</th>
      <th class="border px-3 py-2 text-center font-bold">Domain</th>
      <th class="border px-3 py-2 text-center font-bold">Applicable Shapes</th>
      <th class="border px-3 py-2 text-center font-bold">Challenges</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td class="border px-3 py-2" rowspan="2">Series expansion of basis function</td>
      <td class="border px-3 py-2">Mie</td>
      <td class="border px-3 py-2">Frequency domain</td>
      <td class="border px-3 py-2">Sphere, circular cylinder</td>
      <td class="border px-3 py-2"></td>
    </tr>
    <tr>
      <td class="border px-3 py-2">T-matrix</td>
      <td class="border px-3 py-2">''</td>
      <td class="border px-3 py-2">Shapes with symmetries</td>
      <td class="border px-3 py-2"></td>
    </tr>
    <tr>
      <td class="border px-3 py-2" rowspan="2">Solves IE at grids</td>
      <td class="border px-3 py-2">DDA</td>
      <td class="border px-3 py-2">''</td>
      <td class="border px-3 py-2">Arbitrary shape</td>
      <td class="border px-3 py-2">Size parameter 10 <div class="text-2" style="color: red"> Kahnert (2016) </div> </td>
    </tr>
    <tr>
      <td class="border px-3 py-2">MoM</td>
      <td class="border px-3 py-2">''</td>
      <td class="border px-3 py-2">''</td>
      <td class="border px-3 py-2">Low accuracy <div class="text-2" style="color: red"> Mishchenko (2014) </div> </td>
    </tr>
    <tr>
      <td class="border px-3 py-2" rowspan="2">Solves PDE at grids</td>
      <td class="border px-3 py-2">FEM</td>
      <td class="border px-3 py-2">''</td>
      <td class="border px-3 py-2">''</td>
      <td class="border px-3 py-2">Size parameter 10 <div class="text-2" style="color: red"> Mishchenko et. al (2000)  </div> </td>
    </tr>
    <tr>
      <td class="border px-3 py-2">FDTD</td>
      <td class="border px-3 py-2">Time domain</td>
      <td class="border px-3 py-2">''</td>
      <td class="border px-3 py-2">Size parameter 20 <div class="text-2" style="color: red"> Kahnert (2016)  </div> </td>
    </tr>
    <tr>
      <td class="border px-3 py-2" colspan="1">Solves particle populations at grids</td>
      <td class="border px-3 py-2"><span v-mark.circle.red="1">Lattice Boltzmann method</span></td>
      <td class="border px-3 py-2">''</td>
      <td class="border px-3 py-2">''</td>
    </tr>
  </tbody>
</table>

<v-drag pos="765,36,155,_">
<div class="text-3 ">
$$
\text{Size parameter}  = 2 \pi \frac{a}{\lambda}
$$
</div>
</v-drag>

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---
layout: two-cols-header
layoutClass: gap-10
---

## Lattice Boltzmann Method

::left::

<div class="mt-0">
  <img src="/figures/LBM_scale.png" alt="Image 1" class="h-auto">
</div>

::right::

<div v-click="1" class="mt-0 text-3">
Distribution function (Particle population)
$$
f (\vec{x}, \vec{c}, t)
$$
</div>

<div v-click="2" class="mt-0 text-3">
Lattice Boltzmann equation
$$
\begin{aligned}
f_i (\vec{x} + \vec{c}_i \Delta t, t + \Delta t) &= f_i (\vec{x}, t) + \Omega_i (\vec{x}, t) \\[1.0em]
\end{aligned}
$$
</div>

<div v-click="4" class="mt-0 text-3">
$$
\begin{aligned}
\Omega_i (\vec{x}, t) &= - \frac{f_i (\vec{x}, t) - f_i^{eq} (\vec{x}, t)}{\tau} \Delta t \\[1.0em]
\end{aligned}
$$
</div>

<div v-click="5" class="mt-0 text-3">
$$
\begin{aligned}
f_i (\vec{x} + \vec{c}_i \Delta t, t + \Delta t) &= \left( 1 - \frac{\Delta t}{\tau} \right) f_i (\vec{x}, t) + \frac{\Delta t}{\tau} f_i^{eq} (\vec{x}, t)  \\[1.0em]
\end{aligned}
$$
</div>

<div v-click="6" class="mt-0 text-3">
Macroscopic quantity
$$
\Sigma_{i} f_i (\vec{x}, t)
$$
</div>

<v-drag v-click="3" pos="824,165,117,_">
  <div text-center text-3 border border-main rounded>
    Collision operator
  </div>
</v-drag>

<v-drag-arrow v-click="3" pos="854,189,-34,31" op70 />

<v-drag v-click="4"  pos="647,337,164,_">
  <div v-click.hide="5" text-center text-3 border border-main rounded>
    BGK collision operator
  </div>
</v-drag>

<div class="abs-bl m-2 text-2">
  Timm Kruger (2017)
</div>

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---
layout: two-cols-header
layoutClass: gap-10
---

## Lattice Boltzmann Method

::left::

<div class="flex justify-between items-center">
  <div class="text-center mr-5 ml-9">
    Post collision
  </div>
  <div class="text-center ml-5 mr-9">
    Pre collision
  </div>
</div>

<figure class="text-center item-center my-5">
  <img src="/figures/LBM_Kruger.png" alt="Image 1" class="h-auto">
</figure>

<v-drag pos="6,395,282,_">
<div v-click="1" class="text-3 text-left">
$$
f_i^* (\vec{x}, t) = f_i (\vec{x}, t) + \frac{\Delta t}{\tau} \left[f_i^{eq} (\vec{x}, t) - f_i (\vec{x}, t) \right]
$$
</div>
</v-drag>

<v-drag pos="306,369,198,_">
<div v-click="2"  class="text-3 text-left">
$$
f_i (\vec{x} + \vec{c}_i \Delta t, t + \Delta t) = f_i^* (\vec{x}, t)
$$
</div>
</v-drag>

<div class="abs-bl m-2 text-2">
  Timm Kruger (2017)
</div>

::right::

<figure v-click="3" class="text-center item-center">
  <video autoplay loop muted class="w-full h-auto">
    <source src="/figures/rad_force/lattice_boltzmann.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</figure>

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---
layout: two-cols-header
layoutClass: gap-10
---

## Chapman-Enskog Expansion

::left::

<div v-click class="text-3">
Lattice Boltzmann equation
$$
\begin{aligned}
f_{i}(\vec{x} + \vec{c}_i\Delta t, t + \Delta t) = f_{i}(\vec{x} ,t) + \frac{\Delta t}{\tau} \left[ f_{i}^{eq}(\vec{x} ,t) - f_{i}(\vec{x} ,t) \right]
\end{aligned}
$$
</div>




<div v-click class="text-3">
Assumptions 
$$
\begin{aligned}
\sum_{i} f_i &= \sum_{i} f_i^{eq} \hspace{10pt}\\[2.0em]
\tau &= \frac{1}{2}
\end{aligned}
$$
</div>


<div v-click class="text-3">
We get 
$$
\begin{aligned}
\color{red} \boxed{ \sum_{i} \frac{\partial}{\partial t} f_i^{eq} + \sum_{i} \left( \pmb{c}_i \cdot \pmb{\nabla} \right) f_i^{eq} \approx 0 }
\end{aligned}
$$
</div>





::right::

<div v-click class="mt-1 text-3">
Equilibrium distribution functions
$$
\color{blue}
\begin{aligned}
\vec{e}_i^{eq} = 
    \begin{cases}
      \frac{1}{6}\Big(\vec{E} -   \vec{c}_i \times \vec{H} \Big) & \text{if $i \neq 0$}\\
      (\varepsilon_{r} - 1 ) \vec{E} & \text{if $i = 0$}
    \end{cases} \\[2.0em]
\vec{h}_i^{eq} = 
    \begin{cases}
      \frac{1}{6}\Big(\vec{H} +  \vec{c}_i \times \vec{E} \Big) & \text{if $i \neq 0$}\\
      (\mu_{r} - 1 ) \vec{H} & \text{if $i = 0$}
    \end{cases}  
\end{aligned}
$$

</div>

<div v-click class="mt-1 text-3">
Recovered equations
$$
\color{green}
\begin{aligned}
\boxed{ \nabla \times \vec{E} = - 3 \mu_r \frac{\partial \vec{H}}{\partial t} } \hspace{10pt} \textcolor{grey}{and} \hspace{10pt}
\boxed{ \nabla \times \vec{H} =  3 \varepsilon_r \frac{\partial \vec{E}}{\partial t} }  
\end{aligned}
$$

</div>

<div v-click class="mt-1 text-3">
Initilization
$$
\begin{aligned}
\nabla \cdot \vec{E} = 0 \hspace{10pt} \textcolor{grey}{and} \hspace{10pt} \nabla \cdot \vec{H} =  0 
\end{aligned}
$$

</div>

<div v-click class="mt-1 text-3">
Wave velocity
$$
\begin{aligned}
v = \frac{1}{3 \sqrt{\mu_r \varepsilon_r}}
\end{aligned}
$$

</div>

<div class="abs-bl m-2 text-2">
  Hauser and Verhey (2017)
</div>

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---


## Normal Incidence at a Plane Wall

<div class="relative w-full mt-0">

<div v-click.hide="3" class="absolute grid grid-cols-2 gap-15 mt-15 place-items-center transition-opacity duration-100 opacity-100">
  <figure v-click="1"  class="text-center">
    <img src="/figures/normal_incidence.png" alt="Image 1" class="w-full h-auto">
  </figure>
  
  <div v-click="2" class="mt-10">

$$
\begin{aligned}
\left| \frac{\vec{E}_{0_R}}{\vec{E}_{0_I}}  \right| &= \left| \frac{1 - \beta}{1 + \beta} \right| \\[2.0em]
\left| \frac{\vec{E}_{0_T}}{\vec{E}_{0_I}}  \right| &= \left| \frac{2}{1 + \beta} \right| \\[3.0em]
\beta &= \frac{\mu_1 v_1}{\mu_2 v_2}
\end{aligned}
$$

  </div>

</div>

<div v-click="3" class="text-center text-4 mb-1 mt-5">
  Permeability of the wall is fixed
</div>

<div v-click="3" class="grid grid-cols-2 gap-10 place-items-center">
  <figure class="text-center">
    <img src="/figures/JCP/Normal_Inc_E_er_20.svg" alt="Image 1" class="w-auto h-auto">
  </figure>
  
  <figure class="text-center">
    <img src="/figures/JCP/Normal_Inc_H_er_20.svg" alt="Image 2" class="w-auto h-auto">
  </figure>
</div>

<div v-click="4" class="text-center text-4 mt-2 mb-1">
  Permittivity of the wall is fixed
</div>

<div v-click="4" class="grid grid-cols-2 gap-10 place-items-center mt-1">
  <figure class="text-center">
    <img src="/figures/JCP/Normal_Inc_E_mur_20.svg" alt="Image 3" class="w-auto h-auto">
  </figure>
  
  <figure class="text-center">
    <img src="/figures/JCP/Normal_Inc_H_mur_20.svg" alt="Image 4" class="w-auto h-auto">
  </figure>
</div>

</div>

<v-drag pos="781,44,131,_">
<div v-click="3"  class="text-3 text-left">
$$
\lambda_T  = 20 \times \Delta x
$$
</div>
</v-drag>

<div v-click="1" class="abs-bl m-2 text-2">
  Griffiths (2013)
</div>

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---
layout: two-cols-header
layoutClass: gap-10
---

## Normal Incidence Plane Wave Scattering by Circular Cylinder

::left::

<div v-click="1" class="text-3 mt-0">
Perfect electric conductor (PEC)
$$
\begin{aligned}
{E}_z^S &= \Re \left[ {E}_0 \sum_{m=-\infty}^{+\infty} (-i)^m A_m H_m^{(2)} \left(k_0 r \right) e^{im\phi} e^{i \omega t} \right] \\[2.0em]
A_m &= - \frac{J_m \left( k_0 a \right) }{H_m^{(2)} \left( k_0 a \right) }
\end{aligned}
$$
</div>

<div h-1 />

<div v-click="2" class="mt-0 text-3">
Dielectric
$$
\begin{aligned}
{E}_z^S &= \Re \left[ {E}_0 \sum_{m = - \infty}^{+ \infty} (-i)^m B_m H_m^{(2)}\left( k_0 r \right)e^{im\phi} e^{i \omega t} \right] \\[1.0em]
{E}_z^T &= \Re \left[ {E}_0 \sum_{m = - \infty}^{+ \infty} (-i)^m C_m J_m \left( k_1 r \right) e^{im\phi} e^{i \omega t} \right] \\[2.0em]
B_m &=  \frac{J_m^{'}(k_0 a) J_m(k_1 a) - \sqrt{\frac{\varepsilon_r}{\mu_r}} J_m(k_0 a) J_m^{'} (k_1 a)}{\sqrt{\frac{\varepsilon_r}{\mu_r}} H_m^{(2)}(k_0 a) J_m^{'} (k_1 a) - H_m^{(2)'} (k_0 a) J_m(k_1 a)} \\[1.0em]
C_m &= \frac{ J_m^{'}(k_0 a) H_m^{(2)}(k_0 a) - H_m^{(2)'} (k_0 a) J_m(k_0 a)}{\sqrt{\frac{\varepsilon_r}{\mu_r}} H_m^{(2)}(k_0 a) J_m^{'} (k_1 a) - H_m^{(2)'} (k_0 a) J_m(k_1 a)}
\end{aligned}
$$

</div>

::right::

<figure class="text-center mt-5">
    <img src="/figures/DomainSchematic.svg" alt="Image 1" class="w-full h-auto">
</figure>

<div v-click="1" class="abs-bl m-2 text-2">
  C.A. Balanis (2012)
</div>

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---
layout: two-cols-header
layoutClass: gap-5
---

## Normal Incidence Plane Wave Scattering by Circular Cylinder

Near-to-Far-Field Transformation

::left::

<div class="text-3">
Scattering width
$$
\begin{aligned}
\sigma = \lim_{r \to \infty} 2 \pi r \frac{|\vec{E}^S|^2}{|\vec{E}^I|^2}
\end{aligned}
$$
</div>

<figure v-click="1" class="flex text-center w-3/4 mt-10">
  <img src="/figures/farfield1.png" alt="Image 2" class="w-full h-auto">
</figure>

::right::

<div v-click="2" class="mt-1 text-3">
Currents at the fictitous boundary
$$
\begin{aligned}
\vec{J}(\vec{r'}) = \hat{n'} \times \vec{H} (\vec{r'}) \\[1.0em]
\vec{M}(\vec{r'}) = - \hat{n'} \times \vec{E} (\vec{r'})
\end{aligned}
$$
</div>

<div v-click="3" class="mt-1 text-3">
Vector potentails at far-distance
$$
\begin{aligned}
\vec{A}(\vec{r}) = - i \frac{\mu}{4} \oint_L \vec{J} (\vec{r'}) H_0^{(2)} ( k_0 | \vec{r} - \vec{r'} | ) dl' \\[1.0em]
\vec{F}(\vec{r}) = - i \frac{\varepsilon}{4} \oint_L \vec{M} (\vec{r'}) H_0^{(2)} ( k_0 | \vec{r} - \vec{r'} | ) dl'
\end{aligned}
$$
</div>

<div v-click="4" class="mt-1 text-3">
Far-field electric and magnetic fields
$$
\begin{aligned}
\vec{E}(\vec{r}) = - i \omega \left[ \vec{A} (\vec{r}) + \frac{1}{k_0^2} \nabla \left\{ \nabla \cdot \vec{A} (\vec{r}) \right\} \right] - \frac{1}{\varepsilon} \nabla \times \vec{F} (\vec{r}) \\[1.0em]
\vec{H}(\vec{r}) = - i \omega \left[ \vec{F} (\vec{r}) + \frac{1}{k_0^2} \nabla \left\{ \nabla \cdot \vec{F} (\vec{r}) \right\} \right] + \frac{1}{\mu} \nabla \times \vec{A} (\vec{r})
\end{aligned}
$$

</div>

<div class="abs-bl m-2 text-2">
  https://eecs.wsu.edu/~schneidj/ufdtd/
</div>

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---

## Normal Incidence Plane Wave Scattering by Circular Cylinder

Considering size

<div v-click="1" class="text-center text-3 mb-0 mt-0">
  Perfect electric conductor
</div>

<div v-click="1" class="grid grid-cols-3 gap-0 place-items-center mb-0">
  <figure class="text-center">
    <img src="/figures/JCP/RCS_PEC_Rayleigh.svg" alt="Image 1" class="w-7/8 h-auto">
  </figure>
  
  <figure class="text-center">
    <img src="/figures/JCP/RCS_PEC_Mie.svg" alt="Image 2" class="w-7/8 h-auto">
  </figure>

  <figure class="text-center">
    <img src="/figures/JCP/RCS_PEC_GO.svg" alt="Image 3" class="w-7/8 h-auto">
  </figure>
</div>

<div v-click="2" class="text-center text-3 mt-0 mb-0">
  Dielectric of dielectric constant
</div>

<div v-click="2" class="grid grid-cols-3 gap-0 place-items-center">
  <figure class="text-center">
    <img src="/figures/JCP/RCS_polar_er_2_0.1.svg" alt="Image 4" class="w-7/8 h-auto">
  </figure>
  
  <figure class="text-center">
    <img src="/figures/JCP/RCS_polar_er_2_1.0.svg" alt="Image 5" class="w-7/8 h-auto">
  </figure>

  <figure class="text-center">
    <img src="/figures/JCP/RCS_polar_er_2_10.0.svg" alt="Image 6" class="w-7/8 h-auto">
  </figure>
</div>

<v-drag pos="578,316,55,_">
<div v-click="2"  class="text-3 text-left">
$$
\varepsilon_r = 2
$$
</div>
</v-drag>

<v-drag pos="36,461,55,_">
<div v-click="2"  class="text-3 text-left">
$$
\frac{a}{\lambda} = \frac{1}{10}
$$
</div>
</v-drag>

<v-drag pos="327,455,55,_">
<div v-click="2"  class="text-3 text-left">
$$
\frac{a}{\lambda} = 1
$$
</div>
</v-drag>

<v-drag pos="624,467,55,_">
<div v-click="2"  class="text-3 text-left">
$$
\frac{a}{\lambda} = 10
$$
</div>
</v-drag>

<v-drag pos="830,74,139,_">
<div v-click="1"  class="text-2.5 text-left">
$$
\min \{ \lambda_{inc}, a \} = 50 \times \Delta x
$$
</div>
</v-drag>

<v-drag pos="11,316,69,_">
<div v-click="3"  class="text-3 text-left">
$$
L/a = 20
$$
</div>
</v-drag>

<v-drag pos="259,312,95,_">
<div v-click="3"  class="text-3 text-left">
$$
L/a = 10
$$
</div>
</v-drag>

<v-drag pos="875,304,72,_">
<div v-click="3"  class="text-3 text-left">
$$
L/a = 4
$$
</div>
</v-drag>

<v-drag-arrow v-click="3" pos="909,357,-45,61"  op70 />

<v-drag-arrow v-click="3" pos="911,315,-57,-42" op70 />

<v-drag-arrow v-click="3" pos="312,356,71,44" op70 />

<v-drag-arrow v-click="3" pos="317,328,65,-59" op70 />

<v-drag-arrow v-click="3" pos="55,363,47,35" op70 />

<v-drag-arrow v-click="3" pos="56,331,49,-42" op70 />

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---

## Normal Incidence Plane Wave Scattering by Circular Cylinder

Considering size

<div v-click="1" class="text-center text-3 mb-0 mt-0">
  Perfect electric conductor
</div>

<div v-click="1" class="grid grid-cols-3 gap-0 place-items-center mb-0">
  <figure class="text-center">
    <img src="/figures/JCP/EzTot_er_1_Real_0.02.png" alt="Image 1" class="w-4/5 h-auto">
  </figure>
  
  <figure class="text-center">
    <img src="/figures/JCP/EzTot_er_1_Real_1.0.png" alt="Image 2" class="w-4/5 h-auto">
  </figure>

  <figure class="text-center">
    <img src="/figures/JCP/EzTot_er_1_Real_50.0.png" alt="Image 3" class="w-4/5 h-auto">
  </figure>
</div>

<div v-click="2" class="text-center text-3 mt-0 mb-0">
  Dielectric constant
</div>

<div v-click="2" class="grid grid-cols-3 gap-0 place-items-center mb-0">
  <figure class="text-center">
    <img src="/figures/JCP/EzTot_er_2_Real_0.02.png" alt="Image 4" class="w-4/5 h-auto">
  </figure>
  
  <figure class="text-center">
    <img src="/figures/JCP/EzTot_er_2_Real_1.0.png" alt="Image 5" class="w-4/5 h-auto">
  </figure>

  <figure class="text-center">
    <img src="/figures/JCP/EzTot_er_2_Real_50.0.png" alt="Image 6" class="w-4/5 h-auto">
  </figure>
</div>

<v-drag pos="543,319,55,_">
<div v-click="2"  class="text-3 text-left">
$$
\varepsilon_r = 2
$$
</div>
</v-drag>

<v-drag pos="11,298,55,_">
<div v-click="1"  class="text-2.5 text-left">
$$
\frac{a}{\lambda} = \frac{1}{50}
$$
</div>
</v-drag>

<v-drag pos="313,301,55,_">
<div v-click="1"  class="text-2.5 text-left">
$$
\frac{a}{\lambda} = 1
$$
</div>
</v-drag>

<v-drag pos="869,300,55,_">
<div v-click="1"  class="text-2.5 text-left">
$$
\frac{a}{\lambda} = 50
$$
</div>
</v-drag>

<!-- <v-drag pos="15,474,55,_">
<div v-click="2"  class="text-2 text-left">
$$
\frac{a}{\lambda} = \frac{1}{10}
$$
</div>
</v-drag>

<v-drag pos="312,482,55,_">
<div v-click="2"  class="text-2 text-left">
$$
\frac{a}{\lambda} = 1
$$
</div>
</v-drag>


<v-drag pos="885,459,55,_">
<div v-click="2"  class="text-2 text-left">
$$
\frac{a}{\lambda} = 10
$$
</div>
</v-drag> -->

<v-drag pos="830,74,139,_">
<div v-click="1"  class="text-2.5 text-left">
$$
\min \{ \lambda_{inc}, a \} = 50 \times \Delta x
$$
</div>
</v-drag>

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---

## Normal Incidence Plane Wave Scattering by Circular Cylinder

Considering dielectric constant

<div v-click="1" class="grid grid-cols-2 gap-10 place-items-center mt-10">
  <figure class="text-center">
    <img src="/figures/JCP/RCS_er_2_1.svg" alt="Image 1" class="w-auto h-auto">
  </figure>
  
  <figure class="text-center">
    <img src="/figures/JCP/RCS_er_5_1.svg" alt="Image 2" class="w-auto h-auto">
  </figure>
</div>

<div v-click="1" class="grid grid-cols-2 gap-10 place-items-center mt-10">
  <figure class="text-center">
    <img src="/figures/JCP/RCS_er_10_1.svg" alt="Image 3" class="w-auto h-auto">
  </figure>
  
  <figure class="text-center">
    <img src="/figures/JCP/RCS_er_20_1.svg" alt="Image 4" class="w-auto h-auto">
  </figure>
</div>

<v-drag pos="263,113,55,_">
<div v-click="1"  class="text-3 text-left">
$$
\varepsilon_r = 2
$$
</div>
</v-drag>

<v-drag pos="730,119,55,_">
<div v-click="1"  class="text-3 text-left">
$$
\varepsilon_r = 5
$$
</div>
</v-drag>

<v-drag pos="259,334,55,_">
<div v-click="1"  class="text-3 text-left">
$$
\varepsilon_r = 10
$$
</div>
</v-drag>

<v-drag pos="725,332,55,_">
<div v-click="1"  class="text-3 text-left">
$$
\varepsilon_r = 20
$$
</div>
</v-drag>

<v-drag pos="749,79,228,_">
<div v-click="1"  class="text-3 text-left">
$$
\lambda_{\varepsilon_r} = 50 \times \Delta x, \hspace{10pt} L/a = 10
$$
</div>
</v-drag>


<v-drag pos="481,91,55,_">
<div v-click="1"  class="text-3 text-left">
$$
a / \lambda = 1
$$
</div>
</v-drag>

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---

## Normal Incidence Plane Wave Scattering by Circular Cylinder

Considering dielectric constant

<div v-click="1" class="grid grid-cols-2 gap-1 place-items-center justify-center mt-2">
  <figure class="flex flex-col items-center">
    <img src="/figures/JCP/EzTot_er_2_Real_1.png" alt="Image 1" class="w-2.35/4 h-auto">
  </figure>

  <figure class="flex flex-col items-center">
    <img src="/figures/JCP/EzTot_er_5_Real_1.png" alt="Image 2" class="w-2.35/4 h-auto">
  </figure>

  <figure class="flex flex-col items-center">
    <img src="/figures/JCP/EzTot_er_10_Real_1.png" alt="Image 3" class="w-2.35/4 h-auto">
  </figure>

  <figure class="flex flex-col items-center">
    <img src="/figures/JCP/EzTot_er_20_Real_1.png" alt="Image 4" class="w-2.35/4 h-auto">
  </figure>
</div>

<v-drag pos="905,77,55,_">
<div v-click="1"  class="text-3 text-left">
$$
a / \lambda = 1
$$
</div>
</v-drag>

<v-drag pos="73,196,55,_">
<div v-click="1"  class="text-3 text-left">
$$
\varepsilon_r = 2
$$
</div>
</v-drag>

<v-drag pos="513,193,55,_">
<div v-click="1"  class="text-3 text-left">
$$
\varepsilon_r = 5
$$
</div>
</v-drag>

<v-drag pos="69,406,55,_">
<div v-click="1"  class="text-3 text-left">
$$
\varepsilon_r = 10
$$
</div>
</v-drag>

<v-drag pos="509,408,55,_">
<div v-click="1"  class="text-3 text-left">
$$
\varepsilon_r = 20
$$
</div>
</v-drag>

<v-drag pos="652,76,228,_">
<div v-click="1"  class="text-3 text-left">
$$
\lambda_{\varepsilon_r} = 50 \times \Delta x, \hspace{10pt} L/a = 10
$$
</div>
</v-drag>

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---
layout: two-cols-header
layoutClass: gap-10
---

## Plane Wave Scattering by Dielectric Sphere

::left::

<figure class="text-center mt-5">
    <img src="/figures/sphere.png" alt="Image 1" class="w-auto h-auto">
</figure>

::right::

<div class="relative w-full mt-0">

<div v-click.hide="3" class="absolute mt-5 place-items-center transition-opacity duration-100 opacity-100">

<div v-click="1" class="mt-1 text-3">
Scattered electric fields
$$
\begin{aligned}
E_r^S &= -i E_0 \cos{\phi} \sum_{n = 1}^{+ \infty} b_n \left[ \hat{H}_n^{(2)''}(k_1 r) + \hat{H}_n^{(2)}(k_1 r) \right] P_n^1 (\cos{\theta}) \\[1.0em]
E_{\theta}^S &= \frac{E_0}{k_1 r} \cos{\phi} \sum_{n = 1}^{+ \infty} \left[ i b_n \hat{H}_n^{(2)'}(k_1 r) \sin{\theta} P'{_n}^1 (\cos{\theta}) - c_n \hat{H}_n^{(2)}(k_1 r) \frac{P_n^1 (\cos{\theta})}{\sin{\theta}} \right]  \\[1.0em]
E_{\phi}^S &= \frac{E_0}{k_1 r} \sin{\phi} \sum_{n = 1}^{+ \infty} \left[ i b_n \hat{H}_n^{(2)'}(k_1 r) \frac{P_n^1 (\cos{\theta})}{\sin{\theta}} - c_n \hat{H}_n^{(2)}(k_1 r) \sin{\theta} P'{_n}^1 (\cos{\theta}) \right]  \\[1.0em]
\end{aligned}
$$
</div>

<div v-click="2" class="mt-1 text-3">
Constants
$$
\begin{aligned}
b_n &=  \frac{- \sqrt{\varepsilon_r} \hat{J}_n^{'}(k_0 a) \hat{J}_n(k_1 a) + \sqrt{\mu_r} \hat{J}_n(k_0 a) \hat{J}_n^{'} (k_1 a)}{\sqrt{\varepsilon_r} 
\hat{H}_n^{(2')}(k_0 a) \hat{J}_n (k_1 a) - \sqrt{\mu_r} \hat{H}_n^{(2)} (k_0 a) \hat{J}_n^{'}(k_1 a)} \\[1.0em]
c_n &=  \frac{- \sqrt{\varepsilon_r} \hat{J}_n(k_0 a) \hat{J}_n^{'}(k_1 a) + \sqrt{\mu_r} \hat{J}_n^{'}(k_0 a) \hat{J}_n (k_1 a)}{\sqrt{\varepsilon_r} 
\hat{H}_n^{(2)}(k_0 a) \hat{J}_n^{'} (k_1 a) - \sqrt{\mu_r} \hat{H}_n^{(2')} (k_0 a) \hat{J}_n(k_1 a)} \\[1.0em]
\end{aligned}
$$
</div>

</div>

<figure v-click="3" class="absolute flex flex-col text-center item-center mt-35">
    <img src="/figures/RCS_PEC_sphere.svg" alt="Image 1" class="w-auto h-auto">
</figure>

</div>

<v-drag v-click="3" pos="591,109,186,_">
<div  class="text-4 text-left">
$$
\sigma = \lim_{r \to \infty} 4 \pi r^2 \frac{| \vec{E}^S|^2}{| \vec{E}^I|^2}
$$
</div>
</v-drag>

<v-drag v-click="3" pos="493,455,72,_">
<div class="text-4 text-left">
$$
r/a = 5
$$
</div>
</v-drag>

<div class="abs-bl m-2 text-2">
  C.A. Balanis (2012)
</div>

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---

## Sharp Edged Scatterer

<v-drag pos="225,101,540,_">
<div v-click.hide="1"  class="mt-3">
  <figure class="text-center">
    <img src="/figures/ice_crystal.png" alt="Image 1" class="w-auto h-auto">
  </figure>
</div>
</v-drag>

<div v-click.hide="1" class="abs-bl m-2 text-2">
  Lamb and Verlinde (2011)
</div>

<div class="grid grid-cols-2 gap-0 items-center justify-center mt-10">

  <figure v-click class="flex flex-col items-center justify-center">
    <img src="/figures/hexagonalEzTot.png" alt="Image 1" class="w-full h-auto">
  </figure>
  
  
  <figure v-click class="flex flex-col items-center justify-center">
    <img src="/figures/UHexagon.svg" alt="Image 3" class="w-4/5 h-auto">
  </figure>
  
</div>

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---

## Multiple Scatterers


Applications in finding effective dielectric constant of composite materials


<div class="grid grid-cols-3 gap-1 place-items-center text-center mt-15">

  <figure v-click class="text-center self-end">
    <img src="/figures/PEC_Multi_Particles.png" alt="Image 1" class="w-full h-auto">
    <figcaption class="text-3">
      Perfect electric conductor
    </figcaption>
  </figure>
  
  <figure v-click class="text-center self-end">
    <img src="/figures/er5_Multi_Particles.png" alt="Image 2" class="w-full h-auto">
    <figcaption class="text-3">
      Dielectric
    </figcaption>
  </figure>
  
  <figure v-click class="text-center self-end">
    <img src="/figures/MA_energy_multi_particles.svg" alt="Image 3" class="w-full h-auto">
    <figcaption class="text-3 mt-5">
      Energy
    </figcaption>
  </figure>
  
</div>

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---
layout: two-cols-header
---

## Radiation Force on Circular Conducting Cylinder

::left::

<v-drag pos="76,218,355,_">
<div class="text-3 text-left">
$$
\langle \mathbb{T} \rangle = \frac{1}{2} \Re \left[ \varepsilon_0  {\bf E}  {\bf E}^* + \mu_0 {\bf H}  {\bf H}^*- \frac{1}{2}  \left( \varepsilon_0 |{\bf E}|^2 + \mu_0 |{\bf H}|^2 \right) \mathbb{I} \right]
$$
</div>
</v-drag>

<v-drag pos="142,328,184,_">
<div class="text-3 text-left">
$$
\langle {\bf F} \rangle = \oint \langle \mathbb{T} \rangle \cdot  {\bf \hat{n}} dl
$$
</div>
</v-drag>

::right::

<div class="flex flex-col justify-center items-center w-auto mb-15">
  <img src="/figures/Fx_PEC1.svg" alt="Image 1">
</div>

<div class="abs-bl m-2 text-2">
  M.I. Mishchenko and L. D. Travis (2002)
</div>

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---

## Radiation force on Dielectric Circular Cylinder

<div class="grid grid-cols-3 gap-6 mt-5">
  <figure v-click class="text-center">
    <img src="/figures/FxDielRayleigh.svg" alt="Image 1" class="w-full h-auto">
    <figcaption class="text-3 mt-2">
      Rayleigh regime
    </figcaption>
  </figure>
  
  <figure v-click class="text-center">
    <img src="/figures/FxDielMie.svg" alt="Image 2" class="w-full h-auto">
    <figcaption class="text-3 mt-2">
      Mie regime
    </figcaption>
  </figure>
  
  <figure v-click class="text-center">
    <img src="/figures/FxDielGO.svg" alt="Image 3" class="w-full h-auto">
    <figcaption class="text-3 mt-2">
      Geometrical optics regime
    </figcaption>
  </figure>
  
</div>

<div v-click class="text-3 mt-10">

| $a / \lambda$ | $\varepsilon_r$ | $a / \Delta x$ | $\lambda / \Delta x$ (within scatterer) | Time (seconds) |               $\%$ Error                |
| :-----------: | :-------------: | :------------: | :-------------------------------------: | :------------: | :-------------------------------------: |
|      1.0      |        2        |       15       |  <span v-mark.circle.red="5">10</span>  |      0.98      | <span v-mark.circle.red="6">4.33</span> |
|      1.0      |        4        |       20       |  <span v-mark.circle.red="5">10</span>  |      2.53      | <span v-mark.circle.red="6">3.20</span> |
|      0.9      |        9        |       30       |  <span v-mark.circle.red="5">11</span>  |     10.41      | <span v-mark.circle.red="6">5.19</span> |

</div>

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---

## Resonance Peak

<div class="grid grid-cols-3 gap-6 mt-5">
  <figure class="text-center">
    <img src="/figures/FxMie_er4.svg" alt="Image 1" class="w-full h-auto">
  </figure>
  
  <figure v-click="1" class="text-center">
    <img src="/figures/Fx_Mie_err.svg" alt="Image 2" class="w-full h-auto">
  </figure>
  
  <figure v-click="2" class="text-center">
    <img src="/figures/Fx_Mie_peaks_0.95.svg" alt="Image 3" class="w-full h-auto">
  </figure>
  
</div>

<div v-click="3" class="relative w-full mt-10">
 
  <div v-click="3" v-click.hide="4" class="absolute inset-0 grid grid-cols-3 gap-6 place-items-center transition-opacity duration-500 opacity-100">
    <figure class="text-center">
      <img src="/figures/trac91_er_4_avg.svg" alt="Image 1" class="w-full h-auto">
    </figure>
    <figure class="text-center">
      <img src="/figures/trac93_er_4_avg.svg" alt="Image 2" class="w-full h-auto">
    </figure>
    <figure class="text-center">
      <img src="/figures/trac95_er_4_avg.svg" alt="Image 3" class="w-full h-auto">
    </figure>
  </div>

  <!-- Second group of images -->
  <div v-click="4" class="absolute inset-0 grid grid-cols-2 gap-6 place-items-center transition-opacity duration-500 opacity-100">
    <figure class="text-center">
      <img src="/figures/MA_er_4.0.svg" alt="Image 4" class="w-full h-auto">
    </figure>
    <figure class="text-center">
      <img src="/figures/energy_er_4.0.svg" alt="Image 5" class="w-full h-auto">
    </figure>
  </div>
</div>

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---

## Radiation Force on Corrugated Elliptical Conducting Cylinder

<div class="flex justify-center w-full">
  <div class="w-3/4 h-auto text-center">
    <img src="/figures/JAP/corrugatedSnap.png" alt="Image 1" class="mx-auto">
  </div>
</div>

<div class="flex justify-center w-full mb-1">
  <img src="/figures/JAP/corrugatedPEC.svg" alt="Image 1" class="m-auto">
</div>

<v-drag pos="693,414,105,_">
  <div text-center text-3 border border-main rounded>
    F.G. Mitri (2019)
  </div>
</v-drag>

<v-drag pos="13,333,288,_">
<div class="text-3 text-left">
$$
r = a \left[ \frac{1}{\sqrt{\left( \cos{\phi} \right)^2 + \left(A \sin{\phi} \right)^2}} + d \cos{(N \phi)} \right]
$$
</div>
</v-drag>

<v-drag pos="103,439,76,_">
<div class="text-3 text-left">
$$
A = \frac{a}{b}
$$
</div>
</v-drag>

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---
layout: two-cols-header
---

## Composite Cylinder

Scattering width

::left::

<figure class="text-center item-center my-5">
  <img src="/figures/Janus/JanusHalf_schematic.png" alt="Image 1" class="w-3/4 h-auto">
</figure>

::right::

<v-drag pos="526,126,55,_">
<div v-click="1"  class="text-3 text-left">
$$
\varepsilon_{r_1} = 1
$$
</div>
</v-drag>

<v-drag pos="426,173,225,_">
<div v-click="1" class="mt-3">
  <figure class="text-center">
    <img src="/figures/Janus/RCS_1.svg" alt="Image 1" class="w-auto h-auto">
  </figure>
</div>
</v-drag>

<v-drag pos="822,129,55,_">
<div v-click="1"  class="text-3 text-left">
$$
\varepsilon_{r_1} = 2
$$
</div>
</v-drag>

<v-drag pos="717,175,225,_">
<div v-click="1" class="mt-3">
  <figure class="text-center">
    <img src="/figures/Janus/RCS_2.svg" alt="Image 1" class="w-auto h-auto">
  </figure>
</div>
</v-drag>

<v-drag pos="515,386,55,_">
<div v-click="1"  class="text-3 text-left">
$$
\varepsilon_{r_1} = 5
$$
</div>
</v-drag>

<v-drag pos="363,491,228,_">
<div v-click="1"  class="text-3 text-left">
$$
\lambda_{\varepsilon_{r_1}} = 50 \times \Delta x, \hspace{10pt} L/a = 10
$$
</div>
</v-drag>

<v-drag pos="593,341,224,_">
<div v-click="1" class="mt-3">
  <figure class="text-center">
    <img src="/figures/Janus/RCS_5.svg" alt="Image 1" class="w-auto h-auto">
  </figure>
</div>
</v-drag>

<v-drag v-click="1" pos="622,75,168,_">
  <div text-center text-3 border border-main rounded>
    Hurd and Sachdeva (1975)
  </div>
</v-drag>

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---

## Radiation Force and Torque

<div v-click="1" class="text-center">
Analytical solution (Hurd and Sachdeva 1975)
</div>

<div v-click="1" class="grid grid-cols-3 gap-0 mt-3">
  <figure class="text-center">
    <img src="/figures/Janus/Fx_Exact_Hurd.svg" alt="Image 1" class="w-full h-auto">
  </figure>
  
  <figure class="text-center">
    <img src="/figures/Janus/Fy_Exact_Hurd.svg" alt="Image 2" class="w-full h-auto">
  </figure>
  
  <figure class="text-center">
    <img src="/figures/Janus/Tz_Exact_Hurd.svg" alt="Image 3" class="w-full h-auto">
  </figure>
</div>

<div v-click="2" class="text-center mt-5">
LBM solutions
</div>

<div v-click="2" class="grid grid-cols-3 gap-0 mt-3">
  <figure class="text-center">
    <img src="/figures/Janus/Fx_LBM_Hurd.svg" alt="Image 1" class="w-full h-auto">
  </figure>
  
  <figure class="text-center">
    <img src="/figures/Janus/Fy_LBM_Hurd.svg" alt="Image 2" class="w-full h-auto">
  </figure>
  
  <figure class="text-center">
    <img src="/figures/Janus/Tz_LBM_Hurd.svg" alt="Image 3" class="w-full h-auto">
  </figure>
  
</div>

<v-drag pos="820,17,94,_">
<figure class="text-center">
  <img src="/figures/Janus/janus.png" alt="Image 2" class="w-full h-auto">
</figure>
</v-drag>

<v-drag pos="624,24,169,_">
<div v-click="2"  class="text-3 text-left">
$$
a = 40 \times \Delta x,  \hspace{10pt} L/a = 4
$$
</div>
</v-drag>



<v-drag pos="140,286,53,_">
<div v-click="1"  class="text-3 text-left">
$$
\langle \vec{F}_x \rangle
$$
</div>
</v-drag>

<v-drag pos="376,274,53,_">
<div v-click="1"  class="text-3 text-left">
$$
\langle \vec{F}_y \rangle
$$
</div>
</v-drag>

<v-drag pos="757,289,53,_">
<div v-click="1"  class="text-3 text-left">
$$
\langle \vec{T}_z \rangle
$$
</div>
</v-drag>



<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---

## Radiation Force and Torque

<div v-click="1" class="grid grid-cols-3 gap-2 mt-3 ml-10">
  <figure class="text-center">
    <img src="/figures/Janus/Fx_Janus_er_1.svg" alt="Image 1" class="w-full h-auto">
  </figure>
  
  <figure class="text-center">
    <img src="/figures/Janus/Fy_Janus_er_1.svg" alt="Image 2" class="w-full h-auto">
  </figure>
  
  <figure class="text-center">
    <img src="/figures/Janus/Tz_Janus_er_1.svg" alt="Image 3" class="w-full h-auto">
  </figure>
</div>

<div v-click="2" class="grid grid-cols-3 gap-2 mt-3 ml-10">
  <figure class="text-center">
    <img src="/figures/Janus/Fx_Janus_er_2.svg" alt="Image 1" class="w-full h-auto">
  </figure>
  
  <figure class="text-center">
    <img src="/figures/Janus/Fy_Janus_er_2.svg" alt="Image 2" class="w-full h-auto">
  </figure>
  
  <figure class="text-center">
    <img src="/figures/Janus/Tz_Janus_er_2.svg" alt="Image 3" class="w-full h-auto">
  </figure>
</div>

<div v-click="3" class="grid grid-cols-3 gap-2 mt-3 ml-10">
  <figure class="text-center">
    <img src="/figures/Janus/Fx_Janus_er_5.svg" alt="Image 1" class="w-full h-auto">
  </figure>
  
  <figure class="text-center">
    <img src="/figures/Janus/Fy_Janus_er_5.svg" alt="Image 2" class="w-full h-auto">
  </figure>
  
  <figure class="text-center">
    <img src="/figures/Janus/Tz_Janus_er_5.svg" alt="Image 3" class="w-full h-auto">
  </figure>
</div>

<v-drag pos="197,54,53,_">
<div v-click="1"  class="text-3 text-left">
$$
\langle \vec{F}_x \rangle
$$
</div>
</v-drag>

<v-drag pos="472,55,53,_">
<div v-click="1"  class="text-3 text-left">
$$
\langle \vec{F}_y \rangle
$$
</div>
</v-drag>

<v-drag pos="749,52,53,_">
<div v-click="1"  class="text-3 text-left">
$$
\langle \vec{T}_z \rangle
$$
</div>
</v-drag>

<v-drag pos="19,114,60,_">
<div v-click="1"  class="text-3 text-left">
$$
\varepsilon_{r_1} = 1
$$
</div>
</v-drag>

<v-drag pos="22,266,53,_">
<div v-click="2"  class="text-3 text-left">
$$
\varepsilon_{r_1} = 2
$$
</div>
</v-drag>

<v-drag pos="19,422,53,_">
<div v-click="3"  class="text-3 text-left">
$$
\varepsilon_{r_1} = 5
$$
</div>
</v-drag>

<v-drag pos="850,0,94,_">
<figure class="text-center">
  <img src="/figures/Janus/janus.png" alt="Image 2" class="w-full h-auto">
</figure>
</v-drag>

<v-drag pos="663,1,169,_">
<div v-click="1"  class="text-3 text-left">
$$
a = 3
0 \times \Delta x,  \hspace{10pt} L/a = 4
$$
</div>
</v-drag>

<v-drag pos="436,26,222,_">
<div v-click="1"  class="text-3 text-left">
4 Parallel threads, 35 secs / simulation 18281 simulations,  1 week
</div>
</v-drag>

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---

## Conclusion






<div class="flex items-start justify-left h-full mt-20">
  <ul class="list-disc text-left">
    <li>Verified LBM's accuracy for electromagnetic scattering and radiation force computations.</li>
    <li>Achieved excellent agreement with analytical results across all scattering regimes.</li>
    <li>Demonstrated efficiency and adaptability for complex geometries.</li>
    <li>Positioned LBM as a reliable tool for computational electrodynamics.</li>
  </ul>
</div>

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---
class: text-4
---

## Visible Research Output

| Publications                                                                                                                                                                                                                                 |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1. Electromagnetic scattering by curved surfaces and calculation of radiation force: Lattice Boltzmann simulations <br> <span class="text-3" ><b>Mohd. Meraj Khan</b>, Sumesh P Thampi and Anubhab Roy <i> J. App. Phys. 136, 19</i> </span> |
| 2. Scattering of electromagnetic waves using lattice Boltzmann method <br> <span class="text-3" ><b>Mohd. Meraj Khan</b>, Sumesh P Thampi and Anubhab Roy <i> Under preparation for J. Comput. Phys </i> </span>                             |
| 3. Radiation Force and Torque on a Dielectric Janus Cylinder by Lattice Boltzmann Method <br> <span class="text-3" ><b>Mohd. Meraj Khan</b>, Sumesh P Thampi and Anubhab Roy <i> Under preparation for Phys. Rev. E </i> </span>             |

<div h-3 />

| Code                                                                                                                                                           |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1. Developed <a href="https://github.com/mohd-meraj-khan/LBM-for-scattering" target="_blank">in-house code</a> for scattering and radiation force calculations |

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---
layout: center
class: text-center
---

## Thank you!

<div class="m-5 text-center">
  <a href="https://github.com/mohd-meraj-khan/LBM-for-scattering" target=_blank>https://github.com/mohd-meraj-khan/LBM-for-scattering</a> 
</div>

---
class: text-4
---
## Visible Research Output

| Conferences                                                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1. Attended “DSFD 2022", conducted online, and presented a talk titled ‘Lattice Boltzmann method for scattering of electromagnetic waves by curved geometries', 22-26 Aug 2022, Suzhou, China |
| 2. Attended CompFlu 2022", and presented a poster titled ‘Electromagnetic wave scattering by dielectric Janus particles', 19-21 Dec 2022, IIT Kharagpur                                       |
| 3. Attended ISMC 2023", and presented a poster titled ‘Radiation force and torque on a dielectric Janus particle', 04-08 Sep 2023, Osaka Japan                                                |

<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>
