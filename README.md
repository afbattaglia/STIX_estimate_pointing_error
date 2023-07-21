# Estimate the pointing error of the SAS

This repository is designed to build an automatic pipeline that can improve the estimation of the STIX (https://github.com/i4Ds/STIX-GSW) pointing error.

The automatic pipeline (status as of 21-Jul-2023) includes the following three scripts:

1. `download_STIX-cpd-aux_stixpy.ipynb`: This script automatically downloads cpd and aux data starting from a list of externally provided events in which the flare UID has to be provided.
2. `automatic_STIX_imaging.pro`: This script performs automatic MEM_GE images for all files downloaded automatically in STEP 1. The time range and energy range of the images are taken from the externally provided list.
3. `automatic_STIX-AIA_comparison.ipynb`: This script automatically downloads, does the cutout and reprojects the AIA 1600 maps to the STIX view for all maps generated in STEP 2. At present, the result is a png figure with the STIX map plot on top of the AIA 1600 map.
