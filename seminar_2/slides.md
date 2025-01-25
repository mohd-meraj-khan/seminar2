---
# You can also start simply with 'default'
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: /figures/sundog.jpg
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
  Fluid mechanics division, Department of Applied Mechanics and Biomedical Engineering <br>
  Indian Institute of Technology Madras, Chennai, India, 600036
</div>

<div class="abs-br m-6 text-xl">
  <a href="https://github.com/mohd-meraj-khan/LBM-for-scattering" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

<div class="abs-br m-1 text-2">
  Background image: https://pixabay.com
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---

# Scattering of electromagnetic waves


<div v-click="1" class="text-center">
Scattering of electromagnetic waves in nature
</div>


<div v-click="1" class="grid grid-cols-3 gap-15 mt-3">
  <figure class="text-center">
    <img src="/figures/scattering/sky_unsplash.jpg" alt="Image 1" class="w-full h-auto">
    <figcaption class="text-3 mt-2">
      Blue sky and white cloud
      <div class="text-1.25">(Source: unsplash.com)</div>
    </figcaption>
  </figure>
  
  <figure class="text-center">
    <img src="/figures/scattering/rainbow_unsplash.jpg" alt="Image 2" class="w-full h-auto">
    <figcaption class="text-3 mt-2">
      Rainbow
      <div class="text-1.25">(Source: unsplash.com)</div>
    </figcaption>
  </figure>
  
  <figure class="text-center">
    <img src="/figures/scattering/halo_wgrz.com.png" alt="Image 3" class="w-full h-auto">
    <figcaption class="text-3 mt-2">
      Sundog and Halo
      <div class="text-1.25">(Source: wgrz.com)</div>
    </figcaption>
  </figure>
  
</div>


<div v-click="2" class="text-center mt-5">
Engineering applications of electromagnetic scattering
</div>


<div v-click="2" class="grid grid-cols-3 gap-15 mt-3">
  <figure class="text-center">
    <img src="/figures/scattering/tower_unsplash.jpg" alt="Image 1" class="w-full h-auto">
    <figcaption class="text-3 mt-2">
      Telecommunication tower
      <div class="text-1.25">(Source: unsplash.com)</div>
    </figcaption>
  </figure>
  
  <figure class="text-center">
    <img src="/figures/scattering/radar_noaa.gov.jpg" alt="Image 2" class="w-full h-auto">
    <figcaption class="text-3 mt-2">
      Radar
      <div class="text-1.25">(Source: noa.gov)</div>
    </figcaption>
  </figure>
  
  <figure class="text-center">
    <img src="/figures/scattering/NDT_sigmatest.org.jpg" alt="Image 3" class="w-full h-auto">
    <figcaption class="text-3 mt-2">
      Non destructive testing
      <div class="text-1.25">(Source: sigmatest.org)</div>
    </figcaption>
  </figure>
  
</div>


---


<div class="flex justify-between mb-0">
  <!-- Slide Title -->
  <h1>Radiation force</h1>
  
  <!-- Small Image -->
  <div v-click="3" class="w-25 h-auto">
    <img src="/figures/rad_force/paramecium.png" alt="Small Slide Image" class="rounded shadow">
  </div>
</div>


<div class="relative w-full mt-0">

<div v-click.hide="3" class="absolute grid grid-cols-2 gap-15 mt-3 place-items-center transition-opacity duration-100 opacity-100">
  <figure v-click="1"  class="text-center">
    <img src="/figures/rad_force/comet_tail_forbes.com.gif" alt="Image 1" class="w-full h-auto">
    <figcaption class="text-3 mt-2">
      Comet tail
      <div class="text-1.25">(Source: forbes.com)</div>
    </figcaption>
  </figure>
  
  <figure v-click="2"  class="text-center">
    <img src="/figures/rad_force/IKAROS_solar_sail_wikimedia.jpg" alt="Image 2" class="w-full h-auto">
    <figcaption class="text-3 mt-2">
      IKAROS solar sail
      <div class="text-1.25">(Source: wikimedia.org)</div>
    </figcaption>
  </figure>
</div>




<div class="absolute grid grid-cols-2 gap-15 mt-3 place-items-center transition-opacity duration-100 opacity-100">
  <figure v-click="3" class="text-center">
    <video autoplay loop muted class="w-full h-auto">
      <source src="/figures/rad_force/Particl_Trapping_Nobel_2018.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption class="text-3 mt-2">
      Trapping of the fat particle of a Paramecium
      <div class="text-1.5"> A Ashkin and J M Dziedzic (1989)</div>
    </figcaption>
  </figure>
  
  <figure v-click="4" class="text-center">
    <video autoplay loop muted class="w-full h-auto">
      <source src="/figures/rad_force/Particl_Manipulation_Nobel_2018.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption class="text-3 mt-2">
      Manipulation of a diatom
      <div class="text-1.5"> A Ashkin and J M Dziedzic (1989)</div>
    </figcaption>
  </figure>
</div>

</div>





---





# Electromagnetic spectrum

<div style="height: 100%; display: flex; align-items: center; justify-content: center;">
    <img src="/figures/EM_Spectrum_Properties_edit.svg" alt="Image 1" style="max-height: 100%; width: auto;">
</div>


<div class="abs-br m-1 text-2">
  Image source: wikipedia
</div>

---
layout: default
---

# Scattering regimes

<div style="display: flex; justify-content: center; text-align: center;">
    <img src="/figures/scattering_Schematic.svg" alt="Image 1">
</div>


<div class="grid grid-cols-3 gap-4 items-center">

<div v-click style="display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center;">

$$ \frac{a}{\lambda} \ll 1$$
<span>Rayleigh regime</span>
</div>


<div v-click style="display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center;">

$$ \frac{a}{\lambda} \sim 1$$
<span>Mie regime</span>
</div>

<div v-click style="display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center;">

$$ \frac{a}{\lambda} \gg 1$$
<span>Geometric optics regime</span>
</div>
</div>

---

# 

---
layout: two-cols
layoutClass: gap-16
---

# Governing equations



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
\hat{n} \cdot \left( B_{2} -  B_{1} \right) &= 0 \\[1.0em]
\hat{n} \times ( \vec{H_2} - \vec{H_1}) &= \vec{K} \\[1.0em]
\end{aligned}
$$

</div>




---
layout: two-cols-header
layoutClass: gap-10
---

# Lattice Boltzmann method

::left::

<div class="mt-0">
  <img src="/figures/LBM_scale.png" alt="Image 1" class="h-auto">
</div>

<div v-click="6" class="mt-10">
Macroscopic quantity
$$
\Sigma_{i} f_i (\vec{x}, t)
$$
</div>



::right::

<div v-click="1" class="mt-0">
Distribution function (Particle population)
$$
f (\vec{x}, \vec{c}, t)
$$
</div>


<div v-click="2" class="mt-0">
Lattice Boltzmann equation
$$
\begin{aligned}
f_i (\vec{x} + \vec{c}_i \Delta t, t + \Delta t) &= f_i (\vec{x}, t) + \Omega_i (\vec{x}, t) \\[1.0em]
\end{aligned}
$$
</div>


<div v-click="4" class="mt-0">
$$
\begin{aligned}
\Omega_i (\vec{x}, t) &= - \frac{f_i (\vec{x}, t) - f_i^{eq} (\vec{x}, t)}{\tau} \Delta t \\[1.0em]
\end{aligned}
$$
</div>


<div v-click="5" class="mt-0">
$$
\begin{aligned}
f_i (\vec{x} + \vec{c}_i \Delta t, t + \Delta t) &= \left( 1 - \frac{\Delta t}{\tau} \right) f_i (\vec{x}, t) + \frac{\Delta t}{\tau} f_i^{eq} (\vec{x}, t)  \\[1.0em]
\end{aligned}
$$
</div>




<v-drag v-click="3" pos="809,191,117,_">
  <div text-center text-3 border border-main rounded>
    Collision operator
  </div>
</v-drag>


<v-drag-arrow v-click="3" pos="856,220,-30,37" op70 />


<v-drag v-click="4" v-click.hide="5" pos="640,393,164,_">
  <div text-center text-3 border border-main rounded>
    BGK collision operator
  </div>
</v-drag>




<div class="abs-br m-1 text-2">
  Timm Kruger (2017)
</div>

---
layout: two-cols-header
layoutClass: gap-10
---

# Lattice Boltzmann method


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



<div class="abs-bl m-1 text-2">
  Timm Kruger (2017)
</div>


::right::

  
<figure v-click="3" class="text-center item-center">
  <video autoplay loop muted class="w-full h-auto">
    <source src="/figures/rad_force/lattice_boltzmann.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</figure>

---
layout: two-cols-header
layoutClass: gap-10
---

# Lattice Boltzmann method for electrodynamics


::left::

<figure class="text-center item-center my-0">
  <img src="/figures/LBM_Kruger.png" alt="Image 1" class="h-auto">
</figure>

<div v-click="1" class="justify-between item-center mt-0 text-3">
$$
\vec{e}_{i}(\vec{x} + \vec{c}_i\Delta t, t + \Delta t) = \left(1 - \frac{\Delta t}{\tau} \right) \vec{e}_{i}(\vec{x} ,t) + \frac{\Delta t}{\tau} \vec{e}_{i}^{eq}(\vec{x} ,t)
$$
</div>

<div v-click="2" class="mt-0 text-3">
$$
\vec{h}_{i}(\vec{x} + \vec{c}_i\Delta t, t + \Delta t) = \left(1 - \frac{\Delta t}{\tau} \right) \vec{h}_{i}(\vec{x} ,t) + \frac{\Delta t}{\tau} \vec{h}_{i}^{eq}(\vec{x} ,t)
$$
</div>



::right::



<div class="abs-bl m-1 text-2">
  Hauser and Verhey (2017)
</div>

---


# Research focus



<div class="flex flex-col items-start justify-center h-3/4 text-5 space-y-3">
  <div class="opacity-100">
    1. This text fades out partially.
  </div>
  
  <div class="opacity-100">
    2. This text fades in partially.
  </div>

  <div class="opacity-100">
    3. This text fades in partially.
  </div>
</div>



---

# Circular conducting cylinder

Scattering width and radiation force


<div class="grid grid-cols-3 place-items-center gap-3 mt-3">
  <figure class="text-center">
    <img src="/figures/JAP/PEC_Es_2D_2_column.svg" alt="Image 1" class="w-full h-auto">
  </figure>
  
  <figure v-click="1"  class="text-center">
    <img src="/figures/JAP/RCS_PEC.svg" alt="Image 2" class="w-full h-auto">
  </figure>
  
  <figure v-click="2"  class="text-center">
    <img src="/figures/JAP/FxPEC.svg" alt="Image 3" class="w-full h-auto">
  </figure>
  
</div>


<v-drag pos="661,102,129,_">
<div v-click="1"  class="text-3 text-left">
$$
\sigma = \lim_{r \to \infty} 2 \pi r \frac{| \vec{E}^S|^2}{| \vec{E}^I|^2}
$$
</div>
</v-drag>


<v-drag pos="629,412,355,_">
<div v-click="2"  class="text-3 text-left">
$$
\langle \mathbb{T} \rangle = \frac{1}{2} \Re \left[ \varepsilon_0  {\bf E}  {\bf E}^* + \mu_0 {\bf H}  {\bf H}^*- \frac{1}{2}  \left( \varepsilon_0 |{\bf E}|^2 + \mu_0 |{\bf H}|^2 \right) \mathbb{I} \right]
$$
</div>
</v-drag>


<v-drag pos="715,468,184,_">
<div v-click="2"  class="text-3 text-left">
$$
\langle {\bf F} \rangle = \oint \langle \mathbb{T} \rangle \cdot  {\bf \hat{n}} dl
$$
</div>
</v-drag>

<div class="abs-bl m-1 text-2">
  C.A. Balanis (2012), M.I. Mishchenko and L. D. Travis (2002)
</div>




---

# Corrugated elliptical conducting cylinder

<div class="flex flex-col gap-10 place-items-center">
  <figure class="text-center">
    <img src="/figures/JAP/corrugatedSnap.svg" alt="Image 1" class="w-auto h-auto">
  </figure>

  <figure class="text-center">
    <img src="/figures/JAP/corrugatedPEC.svg" alt="Image 2" class="w-3/4 h-auto">
  </figure>
</div>


<v-drag pos="156,429,105,_">
  <div text-center text-3 border border-main rounded>
    F.G. Mitri (2019)
  </div>
</v-drag>

---

# Circular dielectric cylinder

Scattering width

<div class="text-center">
Fixed dielectric constant
</div>


<div class="grid grid-cols-3 gap-3 mt-0">
  <figure class="text-center">
    <img src="/figures/JAP/RCS_Rayleigh_er_2.svg" alt="Image 1" class="w-full h-auto">
  </figure>
  
  <figure class="text-center">
    <img src="/figures/JAP/RCS_Mie_er_2.svg" alt="Image 2" class="w-full h-auto">
  </figure>
  
  <figure class="text-center">
    <img src="/figures/JAP/RCS_GO_er_2.svg" alt="Image 3" class="w-full h-auto">
  </figure>
  
</div>


<div v-click="1" class="text-center mt-5">
Fixed size
</div>


<div v-click="1" class="grid grid-cols-2 gap-3 mt-3 place-items-center">
  <figure class="text-center">
    <img src="/figures/JAP/BRCS_ratio_0.5.svg" alt="Image 1" class="w-7/8 h-auto">
  </figure>
  
  <figure class="text-center">
    <img src="/figures/JAP/MRCS_ratio_0.5.svg" alt="Image 2" class="w-7/8 h-auto">
  </figure>
  
</div>



<v-drag pos="673,27,315,_">
  <figure class="text-center">
    <img src="/figures/JAP/legend.png" alt="Image 1" class="w-7/8 h-auto">
  </figure>
</v-drag>

---

Radiation force

<div class="grid grid-cols-3 gap-6">
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

| $a / \lambda$  | $\varepsilon_r$ | $a / \Delta x$ | $\lambda / \Delta x$ (within scatterer) | Time (seconds) | $\%$ Error |
|:--------------:|:---------------:|:--------------:|:---------------------------------------:|:--------------:|:----------:|
| 1.0            | 2               | 15             | <span v-mark.circle.red="5">10</span> | 0.98           | <span v-mark.circle.red="6">4.33</span> |
| 1.0            | 4               | 20             | <span v-mark.circle.red="5">10</span> | 2.53           | <span v-mark.circle.red="6">3.20</span> |
| 0.9            | 9               | 30             | <span v-mark.circle.red="5">11</span> | 10.41          | <span v-mark.circle.red="6">5.19</span> |

</div>

---

Resonance peak


<div class="grid grid-cols-3 gap-6">
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


---

# Sharp edged scatterer


<div class="grid grid-cols-3 gap-0 place-items-center text-center mt-0">

  <figure class="text-center self-end">
    <img src="/figures/hexagonalEzTot.svg" alt="Image 1" class="w-full h-auto">
  </figure>
  
  <figure v-click class="text-center self-end">
    <img src="/figures/FxHexagon.svg" alt="Image 2" class="w-full h-auto">
  </figure>
  
  <figure v-click class="text-center self-end">
    <img src="/figures/UHexagon.svg" alt="Image 3" class="w-full h-auto">
  </figure>
  
</div>




<v-drag pos="210,336,591,_">
<div v-click class="text-2 mt-0">

| Code       | Number of Threads | Time (minutes) |
|:-----------:|:-----------------:|:---------------:|
| Sequential | -                 | 1.42           |
| Parallel   | 1                 | 1.67           |
| Parallel   | 2                 | 0.90           |
| Parallel   | 3                 | 0.71           |
| Parallel   | 4                 | 0.63           |

</div>
</v-drag>

---


# Multiple scatterers




<div class="grid grid-cols-3 gap-1 place-items-center text-center mt-20">

  <figure v-click class="text-center self-end">
    <img src="/figures/PEC_Multi_Particles.svg" alt="Image 1" class="w-full h-auto">
    <figcaption class="text-3">
      Perfect electric conductor
    </figcaption>
  </figure>
  
  <figure v-click class="text-center self-end">
    <img src="/figures/er5_Multi_Particles.svg" alt="Image 2" class="w-full h-auto">
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

---


# Normal incidence at a plane wall (1 D)

<div v-click="1" class="text-center text-4 mb-1">
  Permeability of the wall is fixed
</div>

<div v-click="1" class="grid grid-cols-2 gap-10 place-items-center">
  <figure class="text-center">
    <img src="/figures/JCP/Normal_Inc_E_er_20.svg" alt="Image 1" class="w-auto h-auto">
  </figure>
  
  <figure class="text-center">
    <img src="/figures/JCP/Normal_Inc_H_er_20.svg" alt="Image 2" class="w-auto h-auto">
  </figure>
</div>

<div v-click="2" class="text-center text-4 mt-2 mb-1">
  Permittivity of the wall is fixed
</div>

<div v-click="2" class="grid grid-cols-2 gap-10 place-items-center mt-1">
  <figure class="text-center">
    <img src="/figures/JCP/Normal_Inc_E_mur_20.svg" alt="Image 3" class="w-auto h-auto">
  </figure>
  
  <figure class="text-center">
    <img src="/figures/JCP/Normal_Inc_H_mur_20.svg" alt="Image 4" class="w-auto h-auto">
  </figure>
</div>

---

# Circular cylinder of infinite length (2 D)

<div v-click="1" class="text-center text-4 mb-1">
  Perfect electric conductor
</div>

<div v-click="1" class="grid grid-cols-3 gap-1 place-items-center mb-5">
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



<div v-click="2" class="text-center text-4 mt-1 mb-1">
  Dielectric of dielectric constant
</div>

<div v-click="2" class="grid grid-cols-3 gap-1 place-items-center">
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


<v-drag pos="608,310,55,_">
<div v-click="2"  class="text-4 text-left">
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

---

Dielectric for $a / \lambda = 1$



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



<v-drag pos="264,76,55,_">
<div v-click="1"  class="text-3 text-left">
$$
\varepsilon_r = 2
$$
</div>
</v-drag>

<v-drag pos="724,76,55,_">
<div v-click="1"  class="text-3 text-left">
$$
\varepsilon_r = 5
$$
</div>
</v-drag>

<v-drag pos="259,295,55,_">
<div v-click="1"  class="text-3 text-left">
$$
\varepsilon_r = 10
$$
</div>
</v-drag>

<v-drag pos="725,296,55,_">
<div v-click="1"  class="text-3 text-left">
$$
\varepsilon_r = 20
$$
</div>
</v-drag>

---

# Sphere (3D)


<div class="grid grid-cols-2 gap-3 mt-3">
  <figure class="text-center mt-5">
    <img src="/figures/sphere.png" alt="Image 1" class="w-auto h-auto">
  </figure>
  
  <figure class="flex flex-col text-center item-center mt-30">
    <img src="/figures/RCS_PEC_sphere.svg" alt="Image 1" class="w-auto h-auto">
  </figure>
</div>


<v-drag pos="539,61,186,_">
<div  class="text-4 text-left">
$$
\sigma = \lim_{r \to \infty} 4 \pi r^2 \frac{| \vec{E}^S|^2}{| \vec{E}^I|^2}
$$
</div>
</v-drag>


<div class="abs-bl m-1 text-2">
  C.A. Balanis (2012)
</div>

---
layout: two-cols-header
---

# Composite cylinder

Scattering width

::left::



<figure class="text-center item-center my-5">
  <img src="/figures/Janus/JanusHalf_schematic.svg" alt="Image 1" class="w-auto h-auto">
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


<v-drag pos="593,341,224,_">
<div v-click="1" class="mt-3">
  <figure class="text-center">
    <img src="/figures/Janus/RCS_5.svg" alt="Image 1" class="w-auto h-auto">
  </figure>
</div>
</v-drag>


<v-drag pos="607,94,168,_">
  <div text-center text-3 border border-main rounded>
    Hurd and Sachdeva (1975)
  </div>
</v-drag>

---

Radiation force and torque



<div v-click="1" class="text-center">
Analytical solution (Hurd and Sachdeva 1975)
</div>


<div v-click="1" class="grid grid-cols-3 gap-3 mt-3">
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


<div v-click="2" class="grid grid-cols-3 gap-3 mt-3">
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

---

Dielectric-dielectric

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


<v-drag pos="230,48,53,_">
<div v-click="1"  class="text-3 text-left">
$$
\langle \vec{F}_x \rangle
$$
</div>
</v-drag>


<v-drag pos="471,46,53,_">
<div v-click="1"  class="text-3 text-left">
$$
\langle \vec{F}_y \rangle
$$
</div>
</v-drag>


<v-drag pos="760,48,53,_">
<div v-click="1"  class="text-3 text-left">
$$
\langle \vec{T}_z \rangle
$$
</div>
</v-drag>


<v-drag pos="17,127,53,_">
<div v-click="1"  class="text-3 text-left">
$$
\varepsilon_{r_1} = 1
$$
</div>
</v-drag>


<v-drag pos="19,280,53,_">
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



---
layout: center
class: text-center
---

# Thank you!
