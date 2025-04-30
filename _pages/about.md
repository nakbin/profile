---
permalink: /
title: "Welcome"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

**Greetings!**

I am a postdoctoral research fellow in the Department of Atmospheric, Oceanic, and Earth Sciences (AOES) at George Mason University (GMU). My research focuses on subseasonal-to-seasonal (S2S) prediction using NOAA’s fully coupled global climate model, particularly the Unified Forecast System Version 8 (UFS P8).

I obtained my Ph.D. in Atmosphere Science from the Department of Urban and Environmental Engineering at Ulsan National Institute of Science and Technology (UNIST) in February 2021. My Ph.D. thesis is “Development of a Coupled Data Assimilation System in the Fully Coupled Model and Its Implications for Seamless Prediction” under the advisory of Professor Myong-In Lee.


Diagnostic Climate Models
======
UFS P8
------
The UFS prototype 8 (UFS P8) is a fully coupled global model. The atmospheric component uses the Geophysical Fluid Dynamics Laboratory (GFDL) finite-volume cubedsphere dynamical core, which has c384 (;0.258) horizontal resolution and 127 vertical levels. The atmospheric physics package is the candidate for the Global Forecast System version 17 (GFSv17). The ocean model is GFDL Modular Ocean Model 6 (MOM6; Adcroft et al. 2019). The spatial resolution of MOM6 is a 0.258 tripolar grid with 75 hybrid vertical levels. The Los Alamos Sea Ice Model, version 6 (CICE6), WAVEWATCH III, and Goddard Chemistry Aerosol Radiation and Transport model (GOCART; Chin et al. 2000) are used for sea ice, waves, and aerosol components, respectively.

The reforecasts of UFS P8 are initialized on the first and 15th of each month from April 2011 to March 2018. The atmospheric initial conditions come from the Global Ensemble Forecast System, version 12 (GEFSv12), analysis (Hamill et al. 2022) and the initial conditions of waves are forced by GEFS. The land is initialized by the Noah-MP land model with a combination of Global Soil Wetness Project and GDAS atmospheric forcing, while snow is initialized from Noah-MP with NASA-GLDAS forcing. The ocean and sea ice are initialized by the CPC-3DVAR ocean data assimilation product (Adcroft et al. 2019) and CPC Sea Ice Initialization System (CPC-CSIS; Stefanova et al. 2022), respectively. Each reforecast extends to 35 days. In UFS P8, there is only a deterministic run for each initialization.

See More: https://vlab.noaa.gov/web/ufs-r2o/dataproducts

Temperature Bias over CONUS
------

The large-scale bias pattern in UFS P8 explains 31.6% of total bias variability and is strongly related to upper-level atmospheric circulation originating from the tropical central Pacific (Figure 1). 

<img src="/images/figure2a.png" alt="Figure1" width="70%" />
Figure 1. The leading EOF from all weekly surface air temperature biases over the CONUS (24–50N, 60–130W)
</p></p>

The OLR bias over the tropical central Pacific generates a wave-like bias pattern in the upper atmosphere and affects the surface air temperature in the extratropics. 

UFS P8 also shows weak propagation of the Rossby wave from the tropical central Pacific to the CONUS, indicating that even if the model produces perfect convective activity in the tropics, there can be biases in the midlatitudes affecting the propagation of the Rossby wave.



<img src="/images/Figure10.png" alt="Figure2" width="70%" />
Figure 2. The schematic diagram for the three error sources of surface air temperature bias pattern in UFS P8. Thick arrows indicate teleconnection paths in ERA5 (black) and UFS P8 (blue), respectively.
</p></p>


The surface air temperature bias is strongly related to the upper-level Rossby wave from the tropics. 1) This Rossby wave appears as excited by the OLR bias in the central tropical Pacific. In addition, even if convection in the tropics is well represented, 2) the weak zonal wind at 500 hPa or upper-level atmosphere reduces eastward propagation of the Rossby wave, and 3) the strong vertical wind shear bias can suppress the amplitude of the Rossby wave (Figure 2).

Coupled Data Assimilation
======
<img src="/images/Figure1.png" alt="Figure2" width="70%" />
Figure 3. Schematic diagram of the CDA system. (1) Initialization and the free coupled model run from the coupled analysis to obtain the coupled background (“predictor” steps), (2) increment development (analysis to background) from atmospheric analysis every 6 h and (2) from ocean analysis every 24 h, (3) rewinding of the time step by 3 h, and (4) the coupled model run with IAU forcing terms (“corrector” steps) to produce the coupled analysis. Steps 1–4 outline the sequence of the WCDA process. (5) The GloSea5 ensemble forecasts from the coupled initialization can start at 0000, 0600, 1200, and 1800 UTC.

<img src="/images/Figure9.png" alt="Figure2" width="70%" />
Figure 4. (a) Correlation coefficient and (b) RMSE of the RMM index by forecasting time for UFcst (blue) and CFcst (red). Shading indicates the minimum–maximum range of bootstrapping with 10,000 random samplings.

<img src="/images/daFigure10.png" alt="Figure2" width="70%" />
Figure 5. Lag regression of averaged OLR (shading) and 850-hPa zonal wind (contours) from 10S to 10N onto the averaged OLR over the Indian Ocean (5S–5N, 65–75E) for (a) the GloSea5 coupled reanalysis, (c) UFcst, and (e) CFcst. Gray dashed lines indicate the forecast lead time at day 10 (horizontal) and the Maritime Continent centered at 1208E (vertical). Dotted areas indicate the 95% confidence level. (b),(d),(f) Differences (UFcst–CFcst, UFcst–GloSea5, and CFcst–GloSea5, respectively).



Extreme Heat Events
======
The main configuration file for the site is in the base directory in [_config.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_config.yml), which defines the content in the sidebars and other site-wide features. You will need to replace the default variables with ones about yourself and your site's github repository. The configuration file for the top menu is in [_data/navigation.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_data/navigation.yml). For example, if you don't have a portfolio or blog posts, you can remove those items from that navigation.yml file to remove them from the header. 

References
------
For site 

Example: editing a markdown file for a talk
![Editing a markdown file for a talk](/images/editing-talk.png)
