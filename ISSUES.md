---
title: "Issues MSE 2019"
author: "A M Sajo Castelli"
date: "25 July 2019"
output:
  pdf_document: default
  html_document: default
---


# Capas verificadas

## AO [OK]
`AO` was verified and changes were made.

### Correcciones: Archivo `scenario_data_years.csv`
```
  1 layer_name,scenario_year,data_year
  2 ao_access,2015,2019
  3 ao_access,2016,2019
  4 ao_access,2017,2019
  5 ao_access,2018,2019
  6 ao_access,2019,2019
  7 ao_need,2010,2010
  8 ao_need,2011,2011
  9 ao_need,2012,2012
 10 ao_need,2013,2013
 11 ao_need,2014,2014
 12 ao_need,2015,2015
 13 ao_need,2016,2016
 14 ao_need,2017,2016
 15 ao_need,2018,2016 
...
714 ao_need,2019,2016
```
Notar que **AO_NEED** tiene entradas entre las líneas
7:15 y adicionalmente 714 donde se especifica el último año de dato disponible e.g. 2016.

### Scores
Dado los cambios, los scores se actualizaron a
```
> AO(layers)
  region_id   score dimension goal
1         6 49.2850    status   AO
2         7 47.6610    status   AO
3         6 -0.0452     trend   AO
4         7 -0.1065     trend   AO
```



## CW [OK]
`CW` was verified and changes were made. Scores do not change.

Removed empty and wrong named layer `cw_nutrients_trend_mse2019.csv`.

Table of scores
```
> CW(layers)
  region_id goal dimension     score
1         6   CW    status 72.291514
2         7   CW    status 79.405656
3         6   CW     trend -0.882890
4         7   CW     trend -1.622609
```

## ECO [NO-OK]

**PROBLEMA**

Los datos en el archivo `eco_trend_mse2019.csv` requieren revisión: hay datos fuera del 
fuera del rango [-1.0, +1.0]. Revisar `layers.csv` Renglón 50 `ECO,eco_trend`

### Correciones
Score is being estimated twice. This is because in `scenario_data_years.csv`
has mis-aligned years and duplicate of last scenario/data years. Currently it
looks like
```
685 eco_status,2013,2013
686 eco_status,2014,2014
687 eco_status,2015,2015
688 eco_status,2016,2016
689 eco_status,2017,2017
690 eco_status,2018,2017
691 eco_trend,2015,2017
692 eco_trend,2016,2017
693 eco_trend,2017,2017
694 eco_trend,2018,2017
...
765 eco_status,2019,2017
766 eco_trend,2019,2017
```
Note: last data year for `eco_status` is 2017 and not 2013.

Tabla temporal
```
  region_id goal dimension       score
1         6  ECO    status  97.3600000
2         7  ECO    status 100.0000000
3         6  ECO     trend   0.4523954
4         7  ECO     trend  -1.5032097   <------ ! ERROR not in [-1, +1]
```

# Ignore rest of report

# [IGNORE this section] Issues and descriptions

  1. no layer of source file has reference to `un_regions` found in
     `ICO(layers)` a @ `functions.R`:1241
 
  2. need to update layers `layers/rgn_area.csv` and others
     see warning('AndresS: CSV layers/rgn_area.csv no tiene las superficies correctas en km**2') in `config.R`

  1. `cw_trash_trend` missing rgn_id
     `cw_pathogen_trend` missing rgn_id SCRIPT that check for the intersection of years in
     LAYER, scenario_data_year.csv, layers.cs


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

