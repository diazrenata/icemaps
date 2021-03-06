# icemaps

Working from subsets of the tutorial at https://github.com/eleanorlutz/earth_atlas_of_space/ (by Eleanor Lutz - shared under GPL-3.0) to produce .png images from NASA Earth Observations' Blue Marble and Sea Ice Concentration datasets. 


## File structure

- [`replicate.ipynb`](https://github.com/diazrenata/icemaps/blob/main/replicate.ipynb) contains instructions for replicating this process.
- [`process_maps.ipynb`](https://github.com/diazrenata/icemaps/blob/main/process_maps.ipynb) contains code to produce the files in `processed_maps` from the raw files in `csv_maps` and `jpg_maps`. 
- [`processed_maps/blue_marble`](https://github.com/diazrenata/icemaps/blob/main/processed_maps/blue_marble) contains processed .png maps from the Blue Marble dataset. 
    - `1_earth.png`, etc: Large side view. The numbers correspond to calendar months.
    - `N_1_earth.png`, `S_1_earth.png`, etc: Small views looking down on the north or south poles. Numbers correspond to calendar months.
- [`processed_maps/sea_ice`](https://github.com/diazrenata/icemaps/blob/main/processed_maps/sea_ice) contains processed .pngs from the Sea Ice dataset, named according to the same conventions as the Blue Marble data. 
- [`csv_maps/sea_ice`](https://github.com/diazrenata/icemaps/blob/main/csv_maps/sea_ice) contains [NASA Earth Observations' Sea Ice Concentration data](https://neo.gsfc.nasa.gov/view.php?datasetId=NISE_D&date=2021-12-31), downloaded as .CSV files with 0.1 degree resolution for the 1st of each month in 2021 (January 1st, Feburary 1st, etc).
- [`jpg_maps/blue_marble`](https://github.com/diazrenata/icemaps/blob/main/blue_marble) contains [NASA Earth Observations' Blue Marble: Next Generation data](https://neo.gsfc.nasa.gov/view.php?datasetId=BlueMarbleNG-TB&date=2004-12-01), downloaded as .jpg files with 0.1 degree resolution for each month in 2004.




## Credits

The code in `process_maps.ipynb` is modified from portions of Eleanor Lutz's code at: https://github.com/eleanorlutz/earth_atlas_of_space/blob/main/raster_data.ipynb. Specifically, I changed the paths and simplified the `set_save_img` function to remove toggles that aren't needed for these maps.

Per https://neo.gsfc.nasa.gov/about/:

NASA Earth Observations Blue Marble: Blue Marble: Next Generation was produced by Reto St??ckli, NASA Earth Observatory (NASA Goddard Space Flight Center). When using or republishing Blue Marble: Next Generation please credit ???NASA Earth Observatory.??? Accessed at at https://neo.gsfc.nasa.gov/view.php?datasetId=BlueMarbleNG-TB&date=2004-12-01 for each month in 2004.

NASA Earth Observations Sea Ice Concentration - Global 1 Day: Images by National Snow and Ice Data Center (NSIDC) in Boulder, Colorado, using satellite passive microwave data from the Special Sensor Microwave/Imager (SSM/I). Accessed from  https://neo.gsfc.nasa.gov/view.php?datasetId=NISE_D&date=2021-12-31 for the 1st of each month in 2021 (January 1 2021, February 1 2021, etc).
