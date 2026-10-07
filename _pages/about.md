---
permalink: /
title: "Nakbin Choi"
seo_title: "Nakbin Choi | Climate Scientist at UNIST"
description: "Nakbin Choi is a climate scientist and Research Assistant Professor at Ulsan National Institute of Science and Technology (UNIST), specializing in climate dynamics, subseasonal-to-seasonal prediction, and coupled data assimilation."
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<p>
  <strong>Research Assistant Professor</strong><br />
  Department of Civil, Urban, Earth, and Environmental Engineering<br />
  Ulsan National Institute of Science and Technology<br />
  <a href="mailto:nbchoi21@unist.ac.kr">nbchoi21@unist.ac.kr</a>
</p>


I am a Research Assistant Professor in the Department of Civil, Urban, Earth, and Environmental Engineering at Ulsan National Institute of Science and Technology (UNIST). My research focuses on subseasonal-to-seasonal (S2S) prediction and Coupled Data Assimilation. I'm involved in developing the Next-Generation Climate Model.

I obtained my Ph.D. in Atmospheric Science from the Department of Urban and Environmental Engineering at Ulsan National Institute of Science and Technology (UNIST) in February 2021. My Ph.D. thesis is “Development of a Coupled Data Assimilation System in the Fully Coupled Model and Its Implications for Seamless Prediction” under the advisement of Professor Myong-In Lee.

Recent research interests are as follows:

Atmospheric controls on ITCZ biases
We investigate why climate models misrepresent the north–south distribution of tropical rainfall. Across models, ITCZ asymmetry is more strongly associated with the vertical structure of atmospheric moisture and virtual temperature than with sea surface temperature alone. Single-column experiments show that moisture-profile changes produce consistent responses in both convective and large-scale precipitation, whereas SST perturbations primarily affect convective precipitation. These results highlight the importance of atmospheric thermodynamic structure, alongside SST, in understanding and reducing ITCZ biases.
![Precipitation responses]({{ "/images/itcz_fig4.png" | relative_url }})
Precipitation responses to SST and moisture-profile perturbations in single-column simulations. Panels show changes in total, convective, and large-scale precipitation relative to the control. Source: Choi, Quan, and Stan (2026), Fig. 4.

<h2>Diagnostic Climate Models</h2>

<h3>UFS P8</h3>

<p >
  The UFS prototype 8 (UFS P8) is a fully coupled global model. The atmospheric component uses the Geophysical Fluid Dynamics Laboratory (GFDL) finite-volume cubedsphere dynamical core, which has c384 (~0.25°) horizontal resolution and 127 vertical levels. The atmospheric physics package is the candidate for the Global Forecast System version 17 (GFSv17). The ocean model is GFDL Modular Ocean Model 6 (MOM6). The spatial resolution of MOM6 is a 0.25° tripolar grid with 75 hybrid vertical levels. The Los Alamos Sea Ice Model, version 6 (CICE6), WAVEWATCH III, and Goddard Chemistry Aerosol Radiation and Transport model (GOCART) are used for sea ice, waves, and aerosol components, respectively.
</p>

<p >
  The reforecasts of UFS P8 are initialized on the first and 15th of each month from April 2011 to March 2018. The atmospheric initial conditions come from the Global Ensemble Forecast System, version 12 (GEFSv12). The land is initialized by the Noah-MP land model with a combination of Global Soil Wetness Project and GDAS atmospheric forcing, while snow is initialized from Noah-MP with NASA-GLDAS forcing. The ocean and sea ice are initialized by the CPC-3DVAR ocean data assimilation product and CPC Sea Ice Initialization System (CPC-CSIS), respectively. Each reforecast extends to 35 days. In UFS P8, there is only a deterministic run for each initialization.
</p>

<p >
  <strong>See More:</strong> <a href="https://vlab.noaa.gov/web/ufs-r2o/dataproducts" target="_blank">https://vlab.noaa.gov/web/ufs-r2o/dataproducts</a>
</p>

<h3>Temperature Bias over CONUS</h3>

<p>The large-scale bias pattern in UFS P8 explains 31.6% of total bias variability and is strongly related to upper-level atmospheric circulation originating from the tropical central Pacific (Figure 1).</p>

<p style="font-family: 'Times New Roman', Times, serif; line-height: 1.6;">
  <img src="/profile/images/figure2a.png" alt="Figure 1" width="70%" /><br />
  <strong>Figure 1.</strong> The leading EOF from all weekly surface air temperature biases over the CONUS (24–50N, 60–130W)
</p>

<p>The OLR bias over the tropical central Pacific generates a wave-like bias pattern in the upper atmosphere and affects the surface air temperature in the extratropics.</p>

<p>UFS P8 also shows weak propagation of the Rossby wave from the tropical central Pacific to the CONUS, indicating that even if the model produces perfect convective activity in the tropics, there can be biases in the midlatitudes affecting the propagation of the Rossby wave.</p>

<p style="font-family: 'Times New Roman', Times, serif; line-height: 1.6;">
  <img src="/profile/images/Figure10.png" alt="Figure 2" width="70%" /><br />
  <strong>Figure 2.</strong> The schematic diagram for the three error sources of surface air temperature bias pattern in UFS P8. Thick arrows indicate teleconnection paths in ERA5 (black) and UFS P8 (blue), respectively.
</p>

<p>The surface air temperature bias is strongly related to the upper-level Rossby wave from the tropics. 1) This Rossby wave appears as excited by the OLR bias in the central tropical Pacific. In addition, even if convection in the tropics is well represented, 2) the weak zonal wind at 500 hPa or upper-level atmosphere reduces eastward propagation of the Rossby wave, and 3) the strong vertical wind shear bias can suppress the amplitude of the Rossby wave (Figure 2).</p>


<hr />

Previous Research
[Coupled Data Assimilation and MJO Prediction — Choi et al. (2025)]({{ "/previous-research/" | relative_url }})
