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



<div class="flex items-center justify-center mt-30">
  <img src="/figures/IITM_Logo.png" alt="" class="h-20 w-20">
</div>

<div class="text-3 mt-10">
  Fluid mechanics division, Department of Applied Mechanics and Biomedical Engineering <br>
  Indian Institute of Technology Madras, Chennai, India, 600036
</div>


<div class="abs-bl m-1.5 text-2">
  Background image: https://pixabay.com
</div>



---

## Scattering of EM waves in Climate Studies



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
    <img src="/figures/radiation.jpg" alt="Image 1" class="w-full h-auto">
    <figcaption class="text-3 mt-2">
      Radiation budget
      <div class="text-2">(Source: betterup.com)</div>
    </figcaption>
  </figure>
  
  <figure class="text-center">
    <img src="/figures/aerosol.jpg" alt="Image 2" class="w-full h-auto">
    <figcaption class="text-3 mt-2">
      Aerosol
      <div class="text-2">(Source: wikipedia.com)</div>
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


## Solution Methods



<table class="w-full border-collapse border text-center text-3.5 mt-10">
  

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

## Normal incidence at a plane wall






<div v-click="1" class="text-center text-4 mb-1 mt-5">
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




<v-drag pos="781,44,131,_">
<div v-click="1"  class="text-3 text-left">
$$
\min \{ \lambda / \Delta x \}  = 20
$$
</div>
</v-drag>




<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>


---

## Normal Incidence Plane Wave Scattering by Circular Cylinder


<div v-click="1" class="text-center text-4 mb-1 mt-5">
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


<div v-click="1" class="text-center text-4 mb-1 mt-5">
  Perfect electric conductor
</div>

<div v-click="1" class="grid grid-cols-3 gap-0 place-items-center mb-1">
  <figure class="text-center">
    <img src="/figures/JCP/EzTot_er_1_Real_0.02.png" alt="Image 1" class="w-5/6 h-auto">
  </figure>
  
  <figure class="text-center">
    <img src="/figures/JCP/EzTot_er_1_Real_1.0.png" alt="Image 2" class="w-5/6 h-auto">
  </figure>

  <figure class="text-center">
    <img src="/figures/JCP/EzTot_er_1_Real_50.0.png" alt="Image 3" class="w-5/6 h-auto">
  </figure>
</div>



<div v-click="2" class="text-center text-4 mt-1 mb-1">
  Dielectric constant
</div>

<div v-click="2" class="grid grid-cols-3 gap-0 place-items-center mb-1">
  <figure class="text-center">
    <img src="/figures/JCP/EzTot_er_2_Real_0.02.png" alt="Image 4" class="w-5/6 h-auto">
  </figure>
  
  <figure class="text-center">
    <img src="/figures/JCP/EzTot_er_2_Real_1.0.png" alt="Image 5" class="w-5/6 h-auto">
  </figure>

  <figure class="text-center">
    <img src="/figures/JCP/EzTot_er_2_Real_50.0.png" alt="Image 6" class="w-5/6 h-auto">
  </figure>
</div>


<v-drag pos="564,305,55,_">
<div v-click="2"  class="text-4 text-left">
$$
\varepsilon_r = 2
$$
</div>
</v-drag>



<v-drag pos="8,290,55,_">
<div v-click="1"  class="text-2.5 text-left">
$$
\frac{a}{\lambda} = \frac{1}{50}
$$
</div>
</v-drag>

<v-drag pos="311,294,55,_">
<div v-click="1"  class="text-2.5 text-left">
$$
\frac{a}{\lambda} = 1
$$
</div>
</v-drag>


<v-drag pos="877,295,55,_">
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


<v-drag pos="406,90,228,_">
<div v-click="1"  class="text-3 text-left">
$$
\min \{\lambda / \Delta x \} = 50, \hspace{10pt} L/a = 10
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




<figure class="flex flex-col text-center item-center mt-18">
    <img src="/figures/RCS_PEC_sphere.svg" alt="Image 1" class="w-auto h-auto">
</figure>



<v-drag pos="656,79,186,_">
<div  class="text-4 text-left">
$$
\sigma = \lim_{r \to \infty} 4 \pi r^2 \frac{| \vec{E}^S|^2}{| \vec{E}^I|^2}
$$
</div>
</v-drag>


<v-drag pos="479,455,72,_">
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

## Sharp edged scatterer




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


## Multiple scatterers




<div class="grid grid-cols-3 gap-1 place-items-center text-center mt-20">

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

## Composite cylinder

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
\min \{\lambda / \Delta x \} = 50, \hspace{10pt} L/a = 10
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


<v-drag pos="617,97,168,_">
  <div text-center text-3 border border-main rounded>
    Hurd and Sachdeva (1975)
  </div>
</v-drag>


<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---

## Radiation force and torque



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
a / \Delta x = 40,  \hspace{10pt} L/a = 4
$$
</div>
</v-drag>


<div class="abs-br m-2 text-3">
  <SlideCurrentNo />
</div>

---

## Conclusion



<div class="mt-10">

- Benchmarked the LBM for

</div>


---
layout: center
class: text-center
---

## Thank you!

<div class="m-5 text-center">
  <a href="https://github.com/mohd-meraj-khan/LBM-for-scattering" target=_blank>https://github.com/mohd-meraj-khan/LBM-for-scattering</a> 
</div>
