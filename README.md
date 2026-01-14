# GHOST_ApRES_archiving
Code for preparation of Autonomous phase-sensitive radio-echo sounder data collected by the ITGC GHOST project for archiving.

The data is archived at the US Antarctic Program Data Center (USAP-DC) at [inert DOI when availible]

In this repositiory are four jupyter notebooks which prepare data and metadata for archiving at USAP-DC as well as save some fo the unattended data to a cloud optimized zarr format in a google cloud storage bucket.

dats_to_zarr_unattended.ipynb:
this notebook loads the raw data files from the unattended ApRES deployments and collates them into netcdfs including location information. This is the level 1 product described in the UPDC page. 

dats_to_NCs_attended.ipynb:
this does the same as above but for the attended ApRES deployments.

metadata_preparation.ipynb:
prepares the metadata files for archiving at USAP-DC, including gelocation information.

NCs_to_zarrs.ipynb:
loads the unattended netcdf files and saves them as cloud optimized zarrs in a google cloud storage bucket.


## Install dependencies
To run the notebooks in this repo, you can install the exact packages used for producing the archived data by running the following commands in the terminal 

```
mamba env create -f environment.yaml
```

```
mamba activate apres_archiving
```



