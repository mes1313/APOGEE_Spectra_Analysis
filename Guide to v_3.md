This file is the current version of the plotter code. What this code does is by taking in the APOGEE telescope (APO or LCO), the 2MASS ID, and the
object's field, it then prints out an image of two graphs. On top is the first 5 visits stacked on a graph, downloaded from the apVisit files
(https://data.sdss.org/datamodel/files/APOGEE_REDUX/APRED_VERS/visit/TELESCOPE/FIELD/PLATE_ID/MJD5/apVisit.html), while the bottom graph has the
first 5 visits stacked on a graph, but downloaded from the apStar files
(https://data.sdss.org/datamodel/files/APOGEE_REDUX/APRED_VERS/stars/TELESCOPE/FIELD/apStar.html). Essentially, if the top image shows radial
velocity shifts, but the bottom image shows the visits to be stacked uniformly, we can confirm that the APOGEE reduction pipeline worked well for
the object (since the apStar files come later—and after the RV reductions—compared to the apVisit files in the pipeline). Disregularities between
the images (i.e., significantly shifted apVisit plots, broadened lines, or significantly dirty spectra) points to other possible contaminants which
should be considered for that object.

Addiitionally, at the bottom of this file we print out the Radial Velocity measurements from the object. I recommend that after the initial plot,
one should check this print to see exactly which 5 visits show "the most significant shifts in RV values." The reason for this is that perhaps a few
of the visits back to back did not have significant shifts in their RV measurements, which can lead to a spectra which does not look like an
interesting candidate system. However, if there are later visits with more significant differences in their values, then it would be more pertinent
to focus on those visits in particular.

If one needs to change the visits that are plotted, for the apVisit files, one will edit the block of code in which the files are called forth
[SFILE1/SFILE2/etc/]. These count up sequentially, so SFILE1 refers to the first visit, SFILE2 to the second, and etc. Meanwhile if one needs to
change the visits from the apStar file, one will edit the block of code which calls for a specific row of the spectra_data array [spectra_data[2,: /
3,:/ 4,:/ etc.]. These ones also count up sequentially, however, do note that the first two rows of the array (spectra_data[1,:] and
spectra_data[0,:]) call for combined spectra with different weightings. Since these are averages and not discrete visits, they aren't necessary for
analyzing whether or not the reduction pipeline worked well between the apVisit and apStar files.