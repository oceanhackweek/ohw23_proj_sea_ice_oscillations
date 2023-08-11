# ohw23_proj_sea_ice_oscillations

# Sea Ice Oscillations
This repo is for the OHW23 marginal ice zone inertial oscillations project

## Background

# Motivation
Storms can generate energetic currents in the ocean mixed later that oscillate at the local inertial frequency. These inertial oscillations can futher generate internal waves in the stratified ocean interior, contributing to ocean mixing. Therefore, inertial oscillations are an important link between the atmosphere and the deep ocean. 

In the data-sparse Arctic, collecting ocean velocity measurements is difficult and expensive. In the marginal ice zone, sea ice can act as a tracer of the underlying ocean currents. Thus, by tracking ice floes through multiple satellite images, we can potentially measure ocean currents from space. 

# Datasets

## Satellite Data
We use data from the [VIIRS instruments](https://lpdaac.usgs.gov/data/get-started-data/collection-overview/missions/s-npp-nasa-viirs-overview/) installed on the [Joint Polar Satellite System](https://www.nesdis.noaa.gov/our-satellites/currently-flying/joint-polar-satellite-system). These satelllites' pole-to-pole orbits result in multiple images per day in the Arctic. This dense temporal sampling is neecssary to resolve inertial currents, which have periods of just over 12 hours in this region.

Cloud-based data from the Suomi-NPP and JPSS-1/NOAA-20 satellites was accessed from [EarthDataSearch](https://search.earthdata.nasa.gov/search). We use the Imaging and Moderate Resolution Level 1b (VNP02IMG, VNP02MOD, VJ102IMG, VJ102MOD) data to create true color images as well as Day-Night Band Level 1b data (VNP02DNB, VJ102DNB) to visualize ice during moonlit nights. 

## Floe Tracking

## Demonstration Event
We focused our project on a storm that occured in the Beaufort Sea, north of Alaska, in autumn 2022. Concurrent ship ADCP data from the R/V Sikuliaq showed the storm generated strong inertial oscillations. We were motivated to test our method on an event with in situ data that could be used to validate our results. Specifically, we focused on satellite imagery from 7-10 Occtober 2022 near the sea ice edge, in a region bounded by 73&deg;N to 77&deg;N, -130&deg;W to -160&deg;W.

In the future, this method could be extended from this prototype event to study interannual changes in inertial osccilation strength. [Results](https://agupubs.onlinelibrary.wiley.com/doi/full/10.1029/2011JC007633) from drifting buoys suggest that inertial osccillations are becoming stronger, a trend that may relate to sea ice thinning and weakening with climate change. A satellite-based method for measuring inertial oscillation strength would greatly increase the amount of data available to study this trend. 

### Project Planning
- [Jam Board](https://jamboard.google.com/d/1lOgVwnqQLvNRPAOEVEGnWXm8FSTuPYQWbteptKrslTM/viewer?f=4)
- [Slide deck](https://docs.google.com/presentation/d/1eQKSdFHNGMDqGJMY4d-yGnNm4UrUj5kIS2mLQGPMZC8/edit#slide=id.g239da66eda5_18_7)

### Packages and Tutorials
- [Satpy](https://satpy.readthedocs.io/en/latest/overview.html)
- [OpenCV and Optical Flow](https://docs.opencv.org/3.4/d4/dee/tutorial_optical_flow.html)
- [Scikit-image and Optical Flow](https://scikit-image.org/docs/stable/auto_examples/registration/plot_opticalflow.html)
 

## Workflow/Roadmap

1. General protocol for accessing data
2. Create an optimal “image” for tracking
3. Reproject all images from swath coordinates to a common lat/lon grid
4. Import images to OpenCV
5. Track ice floes

## Contributing
To contribute to this project, create a fork, make your changes, and submit a pull request

## Team Members
Laura Crews
Colin Sauze
Dalton KS
Alex Kearney
Myranda Shirk
Aditya Sharma
Michael Cappola

## References 
