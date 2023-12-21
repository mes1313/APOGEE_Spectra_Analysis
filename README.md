# APOGEE Spectrum Analysis Tools (in Python)
This repository is a list of tools I worked on during my time pursuing investigations into the radial velocity variations in APOGEE visit spectrum. Please feel free to share and use this code to your hearts content!

A quick overview of the project's scope and current timeline. The original motivation for this project was the apparent "mass gap" in compact object remnants between about 2-5 solar masses. Currently, it is unknown whether this gap is due to observation bias or a real phenomena in the mass distribution of these objects. 

In the field of binary steller astronomy, one method of detecting binary systems with significant unseen companions attached to a star is to detect radial velocity variations in the stellar component's spectra (per https://upload.wikimedia.org/wikipedia/commons/c/c8/Exoplanet_radial_velocity_doppler_spectroscopy_dark.gif, licensed under https://creativecommons.org/licenses/by-sa/4.0/deed.en) 

Spurred on by some recent discoveries in the field of mass-gap compact object-stellar binaries, such as Thompson et al. 2019 (https://ui.adsabs.harvard.edu/abs/2019Sci...366..637T/abstract) and their discovery of a relevant black hole candidate, or Jayasinghe et al. 2022 and the discovery of "The Giraffe" (https://ui.adsabs.harvard.edu/abs/2022MNRAS.516.5945J/abstract), I was motivated to analyze APOGEE spectrum of candidate objects to more accurately quantify the phenomena we are seeing in these object's spectra. Additionally, we of course were interested to search for further interesting candidate systems that might potentiallly be hosts of the relevant mass compact objects

The motivating factors behind the candidate systems that  we were interested in performing initial analysis on are as follows:
  1. Registered as an SB1 by APOGEE (since we expect these systems to only have one stellar companion, and so if the system registered multiple spectral lines, we'd expect it not to be an interesting system)
  2. Specific ranges of effective temperature (between about 3500-6000 K) and surface gravity (log(g) between about 3-4 dex). This factor was motivated by the fact that compact object-stellar binaries have been discovered in this range of Red Giants/Main Sequence stars. We decided to focus on these regions since it's already been shown that objects can be detected here
  3. Noted to have a high v_scatter parameter in their APOGEE combined object file (this is the parameter that tracks uncertainty in the object's radial velocity scatter between visits. SDSS notes that objects with v_scatter > 1 [km/s] are likely binaries, so we included this cut as well

With that all in mind, I encourage anyone who is interested in analyzing APOGEE radial velocities to perhaps take a look at the files in this repository, and as always feel free to reach out with any concerns or questions.

- M
