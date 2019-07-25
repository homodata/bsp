---
title: "Issues MSE 2019"
author: "A M Sajo Castelli"
date: "25 July 2019"
output: html_document
---

# Issues and descriptions

  1. no layer of source file has reference to `un_regions` found in
     `ICO(layers)` a @ `functions.R`:1241
 
  2. need to update layers `layers/rgn_area.csv` and others
     see warning('AndresS: CSV layers/rgn_area.csv no tiene las superficies correctas en km**2') in `config.R`

  1. `cw_trash_trend` missing rgn_id
     `cw_pathogen_trend` missing rgn_id SCRIPT that check for the intersection of years in
     LAYER, scenario_data_year.csv, layers.cs

# Capas verificadas

[ ] AO
[ ] CW
[ ] ECO
[ ] LIV
[ ] ICO
[ ] SPP
[ ] HAB
[ ] ICO Commented las part where unknown object are referenced.

# CheckLayers

Unused fields...
    ico_spp_iucn_status: iucn_sid,eval_yr
    mar_harvest_tonnes: taxa_group
    uninhabited: southern_island,est_population
    
Rows duplicated...
    ico_spp_iucn_status: 162
    
Layers missing data, ie all NA ...
    element_wts_cp_km2_x_protection: element_wts_cp_km2_x_protection_gl2018.csv
    element_wts_cs_km2_x_storage: element_wts_cs_km2_x_storage_gl2018.csv
    element_wts_hab_pres_abs: element_wts_hab_pres_abs_gl2018.csv
    
Layer element_wts_cp_km2_x_protection has no rows of data.
Layer element_wts_cs_km2_x_storage has no rows of data.
Layer element_wts_hab_pres_abs has no rows of data.

