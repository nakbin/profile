---
permalink: /
title: "Welcome"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<p>
  <strong>Nakbin Choi</strong><br />
  Research Assistant Professor<br />
  Department of Civil Urban Earth and Environmental Engineering<br />
  Ulsan National Institute of Science and Technology<br />
  <a href="mailto:nbchoi21@unist.ac.kr">nbchoi21@unist.ac.kr</a>
</p>


I am a postdoctoral research fellow in the Department of Atmospheric, Oceanic, and Earth Sciences (AOES) at George Mason University (GMU). My research focuses on subseasonal-to-seasonal (S2S) prediction using NOAA’s fully coupled global climate model, particularly the Unified Forecast System Version 8 (UFS P8).

I obtained my Ph.D. in Atmospheric Science from the Department of Urban and Environmental Engineering at Ulsan National Institute of Science and Technology (UNIST) in February 2021. My Ph.D. thesis is “Development of a Coupled Data Assimilation System in the Fully Coupled Model and Its Implications for Seamless Prediction” under the advisement of Professor Myong-In Lee.

Recent research interests are as follows:

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

<h2>Coupled Data Assimilation</h2>

<h3>GloSea5</h3>

<p>The GloSea5-GC2.0 is a fully coupled seasonal forecasting system developed by the Met Office, which is based on the Hadley Centre Global Environmental Model, version 3 (HadGEM3). The atmosphere–land component is based on the Met Office Unified Model (UM) and the Joint UK Land Environment Simulator (JULES), along with the ocean–sea ice component based on the Nucleus for European Modelling of the Ocean (NEMO) and the Los Alamos Sea Ice Model (CICE). Each component realizes the interactions with other components through the Ocean Atmosphere Sea Ice Soil (OASIS3) coupler. This study follows the KMA operational configuration (GloSea5-GC2.0). The spatial resolution of the atmospheric model is N216 (0.838 longitude and 0.568 latitude with 85 vertical levels). The top level of the atmosphere is ~85 km in height. The ocean model uses the ORCA025 tripolar grid with 75 vertical levels.</p>

<p>Initialization of atmosphere and land components of GloSea5-GC2.0 uses the global analysis obtained from the KMA Global Data Assimilation and Prediction System (GDAPS), which is based on the Met Office UM model and a hybrid four-dimensional variational data assimilation (4DVAR) scheme. It uses various observations from surface in situ, sonde, aircraft, and satellite sources. KMA produces a 6-hourly atmosphere analysis field at 0000, 0600, 1200, and 1800 UTC. It has a horizontal resolution of N1280 (~10 km) with 70 vertical levels, so the GDAPS analysis fields are regridded to match the GloSea5 grids.</p>

<p>The KMA GloSea5 system uses ocean initial states from the Met Office Forecast Ocean Assimilation Model (FOAM), which is based on the variational data assimilation scheme of NEMO (NEMOVAR). The FOAM also has the ORCA025 tripolar grid.</p>

<h3>Improvement of MJO Prediction</h3>

<p style="font-family: 'Times New Roman', Times, serif; line-height: 1.6;">
  <img src="/profile/images/Figure1.png" alt="Figure 3" width="90%" /><br />
  <strong>Figure 3.</strong> Schematic diagram of the CDA system. (1) Initialization and the free coupled model run from the coupled analysis to obtain the coupled background (“predictor” steps), (2) increment development (analysis to background) from atmospheric analysis every 6 h and from ocean analysis every 24 h, (3) rewinding of the time step by 3 h, and (4) the coupled model run with IAU forcing terms (“corrector” steps) to produce the coupled analysis. Steps 1–4 outline the sequence of the WCDA process. (5) The GloSea5 ensemble forecasts from the coupled initialization can start at 0000, 0600, 1200, and 1800 UTC.
</p>

<p>Figure 3 illustrates the developed WCDA process. Initialization begins with the existing analysis of independent atmosphere and ocean data assimilations. After initialization, the first guess (step 1 in Fig. 3) is obtained from a 6-h coupled model forecast, which serves as the coupled model background (referred to as the “predictor” steps). The second step (step 2) calculates the increment from the KMA GDAPS atmosphere analysis (from a hybrid 4DVAR scheme) and then rewinds the time step by 3 h (step 3). This is followed by a 6-h integration with incremental forcing based on IAU (step 4, called the “corrector” steps). Instead of applying the entire increment at once, IAU divides the total increment by the number of time steps and applies an equal portion uniformly throughout the 6-h corrector step. Finally, an additional 3-h integration (step 1) generates a new coupled background. Updated atmospheric prognostic variables include potential temperature, wind, and specific humidity. In this study, the prognostic mass field is not included due to technical issues, but this system well reproduces the geopotential height. It presumably comes from the well-corrected temperature and wind fields affecting the mass field. This cycle repeats during the WCDA process (steps 1–4), with the ocean analysis from the NEMOVAR scheme updating oceanic prognostic variables (temperature, salinity, wind, sea surface height) every day at 0000 UTC (2). Note that ocean increments are applied within a 6-h time window only at 0000 UTC when the ocean analysis is available daily. During IAU, the atmosphere and ocean components are balanced through flux exchanges via the coupler.</p>

<p style="font-family: 'Times New Roman', Times, serif; line-height: 1.6;">
  <img src="/profile/images/Figure9.png" alt="Figure 4" width="50%" /><br />
  <strong>Figure 4.</strong> (a) Correlation coefficient and (b) RMSE of the RMM index by forecasting time for UFcst (blue) and CFcst (red). Shading indicates the minimum–maximum range of bootstrapping with 10,000 random samplings.
</p>

<p>Figure 4 compares the bivariate correlation and RMSE of MJO RMM index forecasts between UFcst and CFcst during the boreal cold season (October–March). With a predictable correlation threshold of 0.5 for the MJO, UFcst can predict the MJO up to 11 days, while CFcst extends this to 17 days and remains the correlation of 0.5 up to 25 days. The skill difference becomes indistinguishable after 26 days. Note that this forecasting skill, verified over a single year, appears lower than that of other current S2S models, including the same model, when tested over much longer hindcast periods. Due to the small sample size, the correlation and RMSE do not show a gradual degradation of forecast skills as the forecast lead time increases. Nonetheless, compared to UFcst, using WCDA clearly improves MJO prediction. The improvement in MJO forecasting appears to result from enhanced eastward propagation of the MJO from the Indian Ocean to the Maritime Continent.</p>

<p style="font-family: 'Times New Roman', Times, serif; line-height: 1.6;">
  <img src="/profile/images/daFigure10.png" alt="Figure 5" width="70%" /><br />
  <strong>Figure 5.</strong> Lag regression of averaged OLR (shading) and 850-hPa zonal wind (contours) from 10S to 10N onto the averaged OLR over the Indian Ocean (5S–5N, 65–75E) for (a) the GloSea5 coupled reanalysis, (c) UFcst, and (e) CFcst. Gray dashed lines indicate the forecast lead time at day 10 (horizontal) and the Maritime Continent centered at 120E (vertical). Dotted areas indicate the 95% confidence level. (b),(d),(f) Differences (UFcst–CFcst, UFcst–GloSea5, and CFcst–GloSea5, respectively).
</p>

<p>Figure 5 presents the lag regression of OLR and 850-hPa zonal wind, averaged over 10S–10N, relative to the area-averaged OLR in the Indian Ocean (5S–5N, 65–75E). This illustrates the cases where the MJO convection is initially located in the Indian Ocean. In the GloSea5 coupled reanalysis, clear eastward propagation is observed over 15 days, extending from the Indian Ocean to the western Pacific. In comparison, neither forecast accurately captures the eastward propagation over the Maritime Continent (~120E), a phenomenon known as the Maritime Continent barrier effect. However, CFcst demonstrates a better representation of eastward propagation for up to 10 days with a significant signal (Figs. 5b,e), which aligns with the increase in the forecasting skill of the RMM index (Fig. 4a). In contrast, forecasting skill in UFcst rapidly diminishes after 6 days, coinciding with a weakened signal of eastward propagation (Fig. 5c). </p>
