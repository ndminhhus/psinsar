# Advanced processing of SAR interferometry time series using SNAP and StaMPS (Stanford Method for Persistent Scatterers)
This document will describe in details all the steps and releated theory.

Unlike others tutorial, this recipie will try to cover 99% of the process including installation, version fixing, upgrading, etc. If you are a Windows10 user, have no or very little experience with python, linux and want to do SAR interferometry time series analysis by the method of StaMPS (Stanford Method for Persistent Scatterers). This document is for you.

My first advice is: You don't have to install every sofware/packages at onces. We only install a software/package when it is the barrier to prevent us from moving forward. In that way, you will understand what, why and when a certain action is needed. 

1. Define study area and download SLC Sentinel 1

2. Prepare input for StaMPS PSI

3. Install StaMPS, Matlab in Window Sub system for Linux (WSL) Ubuntu

4. Analysis with StaMPS PS
# Results
Out of my curiosity, this is a preliminary investigation of land subsidence in Ho Chi Minh City (HCMC) using Sentinel 1 satellite data. Persistent Scatterer Interferometry (PSI), an advanced remote sensing technique belonging to Interferometry Synthetic Aperture Radar (InSAR), was used to derive displacement of the ground surface over time.

I analyzed 22 pairs of Sentinel 1 SLC images (from 08-06-2020 to 15-02-2021). More than 3 million stable phase pixels were detected and analyzed for deformation analysis over HCMC during this period. Software and open-source Python code were involved, including ESA-SNAP, snap2stamps, and StaMPS. StaMPS Matlab scripts were executed in the Ubuntu environment.

A large amount of satellite data, including 22 raw Sentinel 1 SLC images (4 GB each), was downloaded from The Alaska Satellite Facility (ASF) data portal (not from the Copernicus Open Access Hub because I experienced that downlinks are more stable in ASF). ESA SNAP toolbox 6.0 was used for preprocessing. Then, snap2stamp C++ software was used to prepare input for StaMPS, which eventually produced more than 3 million stable phase pixels. Each pixel contains the velocity of land deformation over HCMC. The figures below show the spatial distribution of Line of Sight (LOS) land subsidence rate

![HCMC_LS_LOS_2021](https://github.com/ndminhhus/psinsar/assets/40456844/5707ccc6-83ca-4bba-a429-a6bca2506c26)
![plot_u-dmo](https://github.com/ndminhhus/psinsar/assets/40456844/59363e13-dd38-4728-b297-50cd92a1b503)
