<section>

### Inside of a Category 4 hurricane

<video
  width=800
  controls
  data-autoplay
  loop
  src="assets/movies/saildrone_hurricane_fiona.mp4"
  type="video/mp4">
</video>

<br>

<div class="reference">Video credit: Saildrone Inc.</div>
</section>


<section>

## Air-sea momentum exchange in coupled models

* Air-sea momentum exchange governed by surface waves.
* But, most coupled models do not resolve waves!
* Even with waves, coupled models lack momentum closure.

<div class="fragment" style="font-style: italic;">
$\Rightarrow$

Can we achieve momentum closure in a coupled atmosphere-wave-ocean system?
</div>

</section>

<section>

## Momentum balance in a coupled atmosphere-ocean system

$$
\dfrac{\partial (\rho_a \mathbf{U})}{\partial t} + \nabla \left( \rho_a \mathbf{U} \right)
 = - \nabla p_a - \rho_a \mathbf{f} \times \mathbf{U} + SGS_a + \dfrac{\partial \tau_a}{\partial z}
$$

$$
\dfrac{\partial (\rho_w \mathbf{u})}{\partial t} + \nabla \left( \rho_w \mathbf{u} \right)
 = - \nabla p_w - \rho_w \mathbf{f} \times \mathbf{u} + SGS_w + \dfrac{\partial \tau_w}{\partial z}
$$

<div class="fragment">
$
\dfrac{\partial \tau_a}{\partial z} =
\dfrac{\partial \tau_w}{\partial z}
$, at $z = 0$
</div>

<div class="fragment">
$
\tau_a = \tau_w
$, at $z = 0$
</div>

<div class="fragment">
$\rightarrow$ Obviously and mathematically correct!
</div>
</section>

<section>

## How about ocean waves? 🌊🤔
</section>

<section>

## Atmosphere-ocean momentum closure with waves

<img class="r-stretch" src="assets/momentum-coupling-diagram.png">

<div class="reference">Curcic (2015)</div>
</section>

<section>

## Waves are responsible for quite a few important processes in the Earth System...

<ul>
  <li class="fragment">Wave growth $\rightarrow$ wind stress $\rightarrow$ atm. boundary layer mixing</li>
  <li class="fragment">Wave breaking $\rightarrow$ upper-ocean mixing $\rightarrow$ vertical transport of gases and nutrients</li>
  <li class="fragment">Stokes drift $\rightarrow$ Langmuir circulation $\rightarrow$ even more mixing</li>
</ul>

<div class="fragment">...to name a few.</div>
</section>


<section>

## Enter wave energy balance equation 🤓

$$
\dfrac{\partial E}{\partial t} +
\dfrac{\partial (\mathbf{\dot{x}} E)}{\partial \mathbf{x}} +
\dfrac{\partial (\dot{k} E)}{\partial k} +
\dfrac{\partial (\dot{\theta} E)}{\partial \theta} =
S_{in} + S_{ds} + S_{nl}
$$
</section>


<section>

## Atmosphere-ocean momentum closure with waves 💡

$$
\dfrac{\partial (\rho_a \mathbf{U})}{\partial t} + \nabla \left( \rho_a \mathbf{U} \right)
 = - \nabla p_a - \rho_a \mathbf{f} \times \mathbf{U} + SGS_a + \color{red}{\dfrac{\partial \tau_a}{\partial z}}
$$

$$
\dfrac{\partial E}{\partial t} +
\dfrac{\partial (\mathbf{\dot{x}} E)}{\partial \mathbf{x}} +
\dfrac{\partial (\dot{k} E)}{\partial k} +
\dfrac{\partial (\dot{\theta} E)}{\partial \theta} =
\color{red}{S_{in}}\color{black}{} +
\color{blue}{S_{ds}}\color{black}{} +
S_{nl}
$$

$$
\dfrac{\partial (\rho_w \mathbf{u})}{\partial t} + \nabla \left( \rho_w \mathbf{u} \right)
 = - \nabla p_w - \rho_w \mathbf{f} \times \mathbf{u} + SGS_w + \color{blue}{\dfrac{\partial \tau_w}{\partial z}}
$$

<br>

<div class="reference">Curcic (2015)</div>
</section>


<section>

### Waves induce a mean sub-surface velocity: Stokes drift

<video
  width=600
  data-autoplay
  loop
  src="assets/movies/stokes_drift.mp4"
  type="video/mp4">
</video>

<br>

<div class="reference">Video credit: Nick Pizzo (UCSD)</div>
</section>


<section>

## Coriolis-Stokes and Vortex forces

Ocean momentum balance becomes:

$
\dfrac{\partial (\rho_w \mathbf{u})}{\partial t} + \nabla \left( \rho_w \mathbf{u} \right) = 
$

$
= - \nabla p_w - \rho_w \mathbf{f} \times (\mathbf{u} + \color{green}{\mathbf{u_{St}}}\color{black}{}) + \color{green}{\mathbf{u_{St}}}\color{black}{} \times \mathbf{\omega} + SGS_w + \color{blue}{\dfrac{\partial \tau_w}{\partial z}}
$

* Based on theory by Mcwilliams et al. (2004)
* New terms responsible for enhanced upper-ocean mixing and near-surface transport

<br>

<div class="reference">Curcic (2015)</div>
</section>


<section>

## Unified Wave INterface - Coupled Model (UWIN-CM)

* Curcic (2015) physics implemented in a fully (3-way) coupled atmosphere-wave-ocean model
  * WRF for the atmosphere
  * UMWM for ocean waves (Donelan et al., 2012); developed here at Rosenstiel
  * HYCOM for ocean circulation
  * ESMF for coupling, interpolation, and parallelism
* Deployed and ran in an "operational" setting on IDSC, NASA, and DOE supercomputers
* Later iteration of the coupled system (EarthVM) in continued development
  here at the Rosenstiel and testing on IDSC Triton

</section>

<section>

## Key findings on air-sea momentum budget in hurricanes
</section>

<section>

### Simulated 10-m winds in four Tropical Cyclones

<img class="r-stretch" src="assets/momentum_budget_wspd.png">

<div class="reference">Curcic (2015)</div>
</section>


<section>

### Hurricane winds generate large ocean waves

<img class="r-stretch" src="assets/momentum_budget_swh.png">

<div class="reference">Curcic (2015)</div>
</section>


<section>

### Wind-wave interaction is complex and difficult to generalize

<div style="display: flex; flex-direction: row;">

<div style="flex: 1">
  <ul style="margin-top: 50px">
    <li style="color: blue;">Waves aligned with wind</li>
    <li style="color: red;">Waves opposing wind</li>
    <li style="color: green;">Waves outrunning wind</li>
  </ul>

  <p class="fragment">
    $\rightarrow$ There are regions where all three regimes exist at the same time! 
  </p>

  <p class="fragment">
    $\rightarrow$ Simple heuristics won't work; need explicit modeling and/or machine learning.
  </p>

</div>

<div style="flex: 1">
  <img width=600 src="assets/momentum_budget_stress_components.png">
</div>

</div>

<div class="reference">Curcic (2015)</div>
</section>


<section>

## ~10% overall loss of momentum to waves

<img class="r-stretch" src="assets/momentum_budget_stress_deficit.png">

<div class="reference">Curcic (2015)</div>
</section>

<!--
<section>

### How about the momentum loss to waves?

<img class="r-stretch" src="assets/momentum_budget_stress_deficit_radial.png">

<div class="reference">Curcic (2015)</div>
</section>


<section>

### Momentum loss to waves as function of wind speed

<img class="r-stretch" src="assets/momentum_budget_stress_deficit_with_wspd.png">

<div class="reference">Curcic (2015)</div>
</section>
-->

<section>

## UWIN-CM and UMWM impacts on the field

* Wave impacts on ocean transport (*Curcic et al., 2016*)
* Wave impacts on drag at landfall (*Chen and Curcic, 2016*)
* Implications for storm surge prediction (*Dietrich et al., 2018*)
* Drifter drogue-loss detection and current estimation (*Haza et al., 2018; 2019*)
* Uncertainty quantification in hurricanes (*Li et al., 2020*)
* Whitecap and aerosol production in NASA's global model (GEOS, *Darmenov et al., 2018*)
* BSISO prediction (*Wang et al., 2021*)
* MJO prediction (*Savarin and Chen, 2022a; 2022b*)
* Sea-spray generation (*Barr et al., 2022*)

<p class="fragment">...and more.</p>
</section>