---
permalink: /previous-research/
title: "Previous Research"
author_profile: true
---

[Back to Home]({{ "/" | relative_url }})

<h2>Coupled Data Assimilation</h2>

<h3>GloSea5</h3>

<p>The GloSea5-GC2.0 is a fully coupled seasonal forecasting system developed by the Met Office, which is based on the Hadley Centre Global Environmental Model, version 3 (HadGEM3). The atmosphere–land component is based on the Met Office Unified Model (UM) and the Joint UK Land Environment Simulator (JULES), along with the ocean–sea ice component based on the Nucleus for European Modelling of the Ocean (NEMO) and the Los Alamos Sea Ice Model (CICE). Each component realizes the interactions with other components through the Ocean Atmosphere Sea Ice Soil (OASIS3) coupler. This study follows the KMA operational configuration (GloSea5-GC2.0). The spatial resolution of the atmospheric model is N216 (0.838 longitude and 0.568 latitude with 85 vertical levels). The top level of the atmosphere is ~85 km in height. The ocean model uses the ORCA025 tripolar grid with 75 vertical levels.</p>

<p>Initialization of atmosphere and land components of GloSea5-GC2.0 uses the global analysis obtained from the KMA Global Data Assimilation and Prediction System (GDAPS), which is based on the Met Office UM model and a hybrid four-dimensional variational data assimilation (4DVAR) scheme. It uses various observations from surface in situ, sonde, aircraft, and satellite sources. KMA produces a 6-hourly atmosphere analysis field at 0000, 0600, 1200, and 1800 UTC. It has a horizontal resolution of N1280 (~10 km) with 70 vertical levels, so the GDAPS analysis fields are regridded to match the GloSea5 grids.</p>

<p>The KMA GloSea5 system uses ocean initial states from the Met Office Forecast Ocean Assimilation Model (FOAM), which is based on the variational data assimilation scheme of NEMO (NEMOVAR). The FOAM also has the ORCA025 tripolar grid.</p>

<h3>Improvement of MJO Prediction</h3>

<p style="font-family: 'Times New Roman', Times, serif; line-height: 1.6;">
  <img src="/profile/images/Figure1.png" alt="Figure 1" width="90%" /><br />
  <strong>Figure 1.</strong> Schematic diagram of the CDA system. (1) Initialization and the free coupled model run from the coupled analysis to obtain the coupled background (“predictor” steps), (2) increment development (analysis to background) from atmospheric analysis every 6 h and from ocean analysis every 24 h, (3) rewinding of the time step by 3 h, and (4) the coupled model run with IAU forcing terms (“corrector” steps) to produce the coupled analysis. Steps 1–4 outline the sequence of the WCDA process. (5) The GloSea5 ensemble forecasts from the coupled initialization can start at 0000, 0600, 1200, and 1800 UTC.
</p>

<p>Figure 1 illustrates the developed WCDA process. Initialization begins with the existing analysis of independent atmosphere and ocean data assimilations. After initialization, the first guess (step 1 in Fig. 1) is obtained from a 6-h coupled model forecast, which serves as the coupled model background (referred to as the “predictor” steps). The second step (step 2) calculates the increment from the KMA GDAPS atmosphere analysis (from a hybrid 4DVAR scheme) and then rewinds the time step by 3 h (step 3). This is followed by a 6-h integration with incremental forcing based on IAU (step 4, called the “corrector” steps). Instead of applying the entire increment at once, IAU divides the total increment by the number of time steps and applies an equal portion uniformly throughout the 6-h corrector step. Finally, an additional 3-h integration (step 1) generates a new coupled background. Updated atmospheric prognostic variables include potential temperature, wind, and specific humidity. In this study, the prognostic mass field is not included due to technical issues, but this system well reproduces the geopotential height. It presumably comes from the well-corrected temperature and wind fields affecting the mass field. This cycle repeats during the WCDA process (steps 1–4), with the ocean analysis from the NEMOVAR scheme updating oceanic prognostic variables (temperature, salinity, wind, sea surface height) every day at 0000 UTC (2). Note that ocean increments are applied within a 6-h time window only at 0000 UTC when the ocean analysis is available daily. During IAU, the atmosphere and ocean components are balanced through flux exchanges via the coupler.</p>

<p style="font-family: 'Times New Roman', Times, serif; line-height: 1.6;">
  <img src="/profile/images/Figure9.png" alt="Figure 2" width="50%" /><br />
  <strong>Figure 2.</strong> (a) Correlation coefficient and (b) RMSE of the RMM index by forecasting time for UFcst (blue) and CFcst (red). Shading indicates the minimum–maximum range of bootstrapping with 10,000 random samplings.
</p>

<p>Figure 2 compares the bivariate correlation and RMSE of MJO RMM index forecasts between UFcst and CFcst during the boreal cold season (October–March). With a predictable correlation threshold of 0.5 for the MJO, UFcst can predict the MJO up to 11 days, while CFcst extends this to 17 days and remains the correlation of 0.5 up to 25 days. The skill difference becomes indistinguishable after 26 days. Note that this forecasting skill, verified over a single year, appears lower than that of other current S2S models, including the same model, when tested over much longer hindcast periods. Due to the small sample size, the correlation and RMSE do not show a gradual degradation of forecast skills as the forecast lead time increases. Nonetheless, compared to UFcst, using WCDA clearly improves MJO prediction. The improvement in MJO forecasting appears to result from enhanced eastward propagation of the MJO from the Indian Ocean to the Maritime Continent.</p>

<p style="font-family: 'Times New Roman', Times, serif; line-height: 1.6;">
  <img src="/profile/images/daFigure10.png" alt="Figure 3" width="70%" /><br />
  <strong>Figure 3.</strong> Lag regression of averaged OLR (shading) and 850-hPa zonal wind (contours) from 10S to 10N onto the averaged OLR over the Indian Ocean (5S–5N, 65–75E) for (a) the GloSea5 coupled reanalysis, (c) UFcst, and (e) CFcst. Gray dashed lines indicate the forecast lead time at day 10 (horizontal) and the Maritime Continent centered at 120E (vertical). Dotted areas indicate the 95% confidence level. (b),(d),(f) Differences (UFcst–CFcst, UFcst–GloSea5, and CFcst–GloSea5, respectively).
</p>

<p>Figure 3 presents the lag regression of OLR and 850-hPa zonal wind, averaged over 10S–10N, relative to the area-averaged OLR in the Indian Ocean (5S–5N, 65–75E). This illustrates the cases where the MJO convection is initially located in the Indian Ocean. In the GloSea5 coupled reanalysis, clear eastward propagation is observed over 15 days, extending from the Indian Ocean to the western Pacific. In comparison, neither forecast accurately captures the eastward propagation over the Maritime Continent (~120E), a phenomenon known as the Maritime Continent barrier effect. However, CFcst demonstrates a better representation of eastward propagation for up to 10 days with a significant signal (Figs. 3b,e), which aligns with the increase in the forecasting skill of the RMM index (Fig. 2a). In contrast, forecasting skill in UFcst rapidly diminishes after 6 days, coinciding with a weakened signal of eastward propagation (Fig. 3c). </p>
