<section>

## What is machine learning?

### A 20-second explanation

<p class="fragment">
  In traditional modeling, we prescribe a model that takes an input and produces an output.
</p>

<p class="fragment">
  In contrast, machine learning generates a model based on sets of inputs and outputs.
</p>

</section>

<section>

## What are neural networks all about?

<img src="assets/neural_network.png">

<div class="reference">Image credit: Michael Nielsen</div>
</section>

<section>

## Why machine learning for Earth Science?

1. Discover patterns in complex data $\rightarrow$ *new scientific understanding*
2. Build predictive models from data $\rightarrow$ *unbiased and more accurate parametric models*
3. Emulate and accelerate explicit and costly models $\rightarrow$ *faster and more general models*

</section>


<section>

### FourCastNet ([Pathak et al. 2022](https://arxiv.org/abs/2202.11214))

<img height=600 src="assets/fourcastnet.png">
</section>


<section>

## Limitations of FourCastNet-like models and alternative ways forward

* FourCastNet-like models are intrinsically limited to the variables (20),
  grid-resoluion (0.25 degree), and output time step (6-hourly) of the training data.
* Useful as a quick and limited forecasting tool, but not a replacement for
  traditional models.
* Alternatives approaches:
  - physics-informed neural networks e.g. [Raissi et al. (2019)](https://arxiv.org/abs/1711.10561)
  - emulating subgrid-scale processes e.g. [Rasp et al. (2018)](https://doi.org/10.1073/pnas.1810286115)
</section>


<section>

## Integrating machine learning in Earth System models

### A two-language problem

* Machine learning training is predominantly done using Python frameworks (TensorFlow, PyTorch, etc.).
* However, virtually every weather, ocean, wave, and climate model is written in Fortran.
* Not only a legacy/technical debt thing! NOAA and the weather enterprise are doubling-down on Fortran
  for their next generation stack of community models.

<p class="fragment" style="font-style: italic;">$\rightarrow$ Significant point of friction for integrating ML into ES models!</p>
</section>


<section>

## Possible solutions to the two-language problem

<ul>
  <li class="fragment">Re-write ES modeling capability in another language (difficult, expensive)</li>
  <li class="fragment">Interface Python ML frameworks directly from ES models (maintenance and performance nightmare)</li>
  <li class="fragment">Glue Python ML and ES models with data files (easy but ad hoc and clumsy)</li>
  <li class="fragment">Implement ML in Fortran for easy integration into ES models (easy but needs work)</li>
</ul>
</section>


<section style="display: flex; flex-direction: column;">

<div style="flex: 8">

## neural-fortran: A parallel deep learning framework for Fortran applications

* Created to solve the two-language problem of machine learning in Earth System models
* Training and inference of arbitrarily deep dense and convolutional neural networks 
* Used in over a dozen published studies from chemistry and combustion to weather and climate
* A registered invention with the U. Miami's Office of Technology Transfer
* https://github.com/modern-fortran/neural-fortran


<div class="reference"><a href="https://doi.org/10.1145/3323057.3323059">Curcic (2019)</a></div>
</div>

<div style="flex: 2">
  <img height=90 src="assets/logos/nasa.png"></img>
  <img height=90 src="assets/logos/gsoc.png"></img>
</div>

</section>


<section style="display: flex; flex-direction: column;">

<div style="flex: 8">

## DOE EarthShots: Deep Learning to Emulate, Improve, and Accelerate Earth System Models

* An organized effort to evaluate the feasibility of deep learning emulators
  for subgrid-scale processes in Earth System models
* Toward more general and efficient Earth System model components
* Led by the University of Miami, in collaboration with the Berkeley Lab, NCAR, and industry partners
* Still at LOI stage, but we are hopeful! Stay tuned. 
</div>

<div style="flex: 2">
  <img height=90 src="assets/logos/doe.png"></img>
</div>

</section>