<section>

## Air-sea momentum exchange in coupled models

* Air-sea momentum exchange governed by surface waves.
* But, most coupled models do not resolve waves!
* Even with waves, coupled models lack momentum closure.

<div class="fragment" style="font-style: italic;">
$\rightarrow$

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
$
</div>

<div class="fragment">
$\rightarrow$ Obviously and mathematically correct!
</div>
</section>

<section>

## How about ocean waves? 🌊🤔
</section>

<section style="outline: 1px solid red;">

## Atmosphere-ocean momentum closure with waves

<img class="r-stretch" src="assets/momentum-coupling-diagram.png">
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
\dfrac{\partial (\dot{k} E)}{\partial \mathbf{x}} +
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
\dfrac{\partial (\dot{k} E)}{\partial \mathbf{x}} +
\dfrac{\partial (\dot{\theta} E)}{\partial \theta} =
\color{red}{S_{in}}\color{black}{} +
\color{blue}{S_{ds}}\color{black}{} +
S_{nl}
$$

$$
\dfrac{\partial (\rho_w \mathbf{u})}{\partial t} + \nabla \left( \rho_w \mathbf{u} \right)
 = - \nabla p_w - \rho_w \mathbf{f} \times \mathbf{u} + SGS_w + \color{blue}{\dfrac{\partial \tau_w}{\partial z}}
$$
</section>