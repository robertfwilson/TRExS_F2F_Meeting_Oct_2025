# File Description

Here you'll find a short description of the files in this folder. Files are located in
the `dryrun_01` folder and are organized in different directories according to data types or origin.

## Catalogs
- `dryrun_01/catalogs/TRExS_dryrun_01_MASTER_input_catalog_v1.1_cutout.csv`: Has the summary input catalog used to simulate the 256x256 image cutout. It contain source ids, positions, source type, and filter brightnesses. It has 12,570 rows.
- `dryrun_01/catalogs/TRExS_dryrun_01_MASTER_input_catalog_v1.1.db`: Is the complete summary input catalog for the 4088x4088 pixel images. It has 4,973,188 rows.
- : It has the stellar parameters of the sources in the master input catalog for the image cutout. It has 12,570 rows.

## Images
- `dryrun_01/simulated_imgs/rimtimsim_WFI_lvl02_{FILTER}_SCA02_field03_rampfitted_r1920c1920_256x256_sim.asdf`: Are the ASDF files with the time-stack of the image cutout for the three filters `F087`, `F146`, and `F213`. The simulation used the master input catalog cutout. The file shapes are `F087 = [131 ,256, 256]`,  `F146 = [6595 ,256, 256]`, and `F213 = [132 ,256, 256]`.
- `dryrun_01/simulated_imgs/rimtimsim_WFI_lvl02_{FILTER}_SCA02_field03_rampfitted_exposureno_{*}_sim.fits`: Are FITS files with the single frame full size image (488x488 pixels) for each filter. The exposure number correspond to the first observations of each filter. The file shapes are `[1, 4088, 4088]` for two header extensions, flux and flux error. 

## Light Curves
- `dryrun_01/lcs_extracted/TRExS_dryrun_01_lcs_v2.0_cutout.tar.gz`: Is the archive file with light curves extracted from the image cutout for all three filters. Files in the archive have name pattern: `roman_wfi_{sicbro_id}_{FILTER}_dryrun01_lc.fits` with `sicbro_id` the source id in the master catalog, and `FILTER` one of the three available filters.
- `dryrun_01/lcs_pivot/....`: Is the archive file with simulated light curves, aka 'pivot light curves'. This are the simulation input light curves with added noise. Files in the archive have name pattern: `....` with `sicbro_id` the source id in the master catalog, and `FILTER` one of the three available filters. 

## Support Files
- `dryrun_01/prf_models/roman_WFI_rampfitted_{FILTER}_3_SCA02_shape_model_cad0_center_v2.fits`: Are the pre-computed PRF models as shown in the [notebook tutorial](../lc_extraction/lc_extraction_build_prf.ipynb). This file are used for PRF light curve extraction. 