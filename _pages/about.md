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

<img src="/images/figure2a.png" alt="Figure1" width="70%" />
<br />
Figure 1. The leading EOF from all weekly surface air temperature biases over the CONUS (24–50N, 60–130W)


<img src="/images/Figure10.png" alt="Figure2" width="70%" />


Coupled Data Assimilation
======
1. Register a GitHub account if you don't have one and confirm your e-mail (required!)
1. Fork [this template](https://github.com/academicpages/academicpages.github.io) by clicking the "Use this template" button in the top right. 
1. Go to the repository's settings (rightmost item in the tabs that start with "Code", should be below "Unwatch"). Rename the repository "[your GitHub username].github.io", which will also be your website's URL.
1. Set site-wide configuration and create content & metadata (see below -- also see [this set of diffs](http://archive.is/3TPas) showing what files were changed to set up [an example site](https://getorg-testacct.github.io) for a user with the username "getorg-testacct")
1. Upload any files (like PDFs, .zip files, etc.) to the files/ directory. They will appear at https://[your GitHub username].github.io/files/example.pdf.  
1. Check status by going to the repository settings, in the "GitHub pages" section

Extreme Heat Events
======
The main configuration file for the site is in the base directory in [_config.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_config.yml), which defines the content in the sidebars and other site-wide features. You will need to replace the default variables with ones about yourself and your site's github repository. The configuration file for the top menu is in [_data/navigation.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_data/navigation.yml). For example, if you don't have a portfolio or blog posts, you can remove those items from that navigation.yml file to remove them from the header. 

References
------
For site 

Example: editing a markdown file for a talk
![Editing a markdown file for a talk](/images/editing-talk.png)
