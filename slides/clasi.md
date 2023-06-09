<section style="display: flex; flex-direction: column;">

<div style="flex: 8">

## Coastal Land Air-Sea Interaction (CLASI)

  <div style="display: flex; flex-direction: row;">

  <div style="flex: 5">
    <ul style="margin-top: 50px">
      <li>
        Field campaigns toward coast-aware air-sea flux parameterizations
        for operational weather prediction models
      </li>
      <li>
        Deployments:
        <ol>
          <li>Central Monterey Bay (Jun-Aug 2021)</li>
          <li>South Monterey Bay (Aug-Oct 2021)</li>
          <li>Santa Cruz (Aug-Oct 2022)</li>
          <li>Northern Gulf of Mexico (Jan-Mar 2023)</li>
        </ol>
      </li>
    </ul>
  </div>

  <div style="flex: 2">
    <img src="assets/asis.png">
  </div>

</div>

<div style="flex: 2">
  <img height=90 src="assets/logos/clasi.png"></img>
  <img height=90 src="assets/logos/onr.png"></img>
  <div class="reference"><a href="https://doi.org/10.1175/BAMS-D-20-0304.1">Haus et al. (2022, BAMS)</a></div>
</div>

</section>


<section style="display: flex; flex-direction: column;">

<div style="flex: 8">

## Air-Sea Interaction Spar (ASIS)

  <div style="display: flex; flex-direction: row;">

  <div style="flex: 2">
    <ul style="margin-top: 50px">
      <li>Designed to be a stationary spar for windsea and a pitch-and-roll buoy for swell</li>
      <li>Optimized for flux and wave measurements with minimal flow distortion</li>
      <li>Battery operated with up to 3 months life</li>
      <li>2 sonic anemometers, 3 motion sensors, 6 wave sensors, and standard meteorology package</li>
    </ul>
  </div>

  <div style="flex: 1">
    <img src="assets/asis.png">
  </div>

</div>

<div style="flex: 2">
  <img height=90 src="assets/logos/clasi.png"></img>
  <img height=90 src="assets/logos/onr.png"></img>
  <div class="reference"><a href="https://doi.org/10.1175/BAMS-D-20-0304.1">Haus et al. (2022, BAMS)</a></div>
</div>

</section>

<section>

## ASIS deployment and recovery in pictures

<img height=400 src="assets/clasi_asis_shipyard.jpg">
</section>

<section>

## ASIS deployment and recovery in pictures

<img height=400 src="assets/clasi_asis_deck.jpg">
</section>


<section>

## ASIS deployment and recovery in pictures

<img height=400 src="assets/asis_recovery.jpeg">
</section>


<section>

## ASIS deployment and recovery in pictures

<img height=400 src="assets/clasi_asis_revelle.jpg">
<p class="reference">Image credit: Jill Zwierz</p>
</section>


<section>

## ASIS deployment and recovery in pictures

<img height=400 src="assets/clasi_um_group.png">
</section>

<section>

## ASIS deployment and recovery in pictures

<img height=400 src="assets/clasi_sam_medina.jpeg">
<img height=400 src="assets/clasi_peisen_neil_armstrong.jpeg">
</section>


<section>

## ASIS deployment and recovery in pictures

<img height=400 src="assets/clasi_me_neil_armstrong.jpeg">
<img height=400 src="assets/clasi_sunset.jpg">
</section>


<section>

### Wind speed and wave heights during the Gulf of Mexico 2023 deployment

<img height=250 src="assets/clasi_phase4_wspd.png">
<img height=250 src="assets/clasi_phase4_swh.png">
</section>


<section>

### Air-sea momentum flux as function of wind speed

<img width=600 src="assets/clasi_phase4_flux_scatter.png">

<p class="fragment" style="font-style: italic;">
  $\rightarrow$ How to fit a model? Perfect candidate for machine learning!
</p>
</section>

<section>

### Neural networks allow unbiased fitting and interpretation of complex data

Fit $[U_z, H_s, T_m, \Delta T] \rightarrow \overline{-u'w'}$

<img width=45% src="assets/clasi_asis_flux_model_data.png">
<img width=45% src="assets/clasi_asis_flux_model_stability.png">

<p class="fragment" style="font-style: italic;">
  $\rightarrow$ Neural networks are universal function approximators.
</p>
</section>