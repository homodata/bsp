---
title: "Progress Report for MSE 2019"
author: "A M Sajo Castelli"
date: "29 September 2019"
output:
  pdf_document: default
  html_document: default
---

ASSESSMENT AREA (region_id=0) + regions 6 and 7.

# Table of progress

goal|pr|layer|status | action
----|--|----|------------------------------------|---------
AO  |  | <span style="color:green">**Ok**</span> |  | 
$\,$|AO| <span style="color:red">GL</span> | Global data |
$\,$|BD| <span style="color:red">GL</span> | Global data |
CP  |  | <span style="color:green">**Ok**</span> | Mix GL and LL |
$\,$|CP| <span style="color:red">GL</span> | Global data |
CS  |  | <span style="color:green">**Ok**</span> | Mix GL and LL |
CW  |  | <span style="color:green">**Ok**</span> |  |
$\,$|CW| <span style="color:green">**Ok**</span> |  | 
ECO |  | <span style="color:green">**Ok**</span> | | 
$\,$|ECO|<span style="color:red">GL</span> | Global data |
FIS |  | <span style="color:red">**GL**</span> | Layer `fis_meancatch_mse2019` empty data column| 
$\,$|FIS|<span style="color:red">GL</span> | Global data |
$\,$|FP| <span style="color:red">GL</span> | Global data |
HAB |  | <span style="color:green">**Ok**</span> |  |
$\,$|HAB| <span style="color:red">GL</span> | Global data |
ICO |  | <span style="color:green">**Ok**</span> | |
$\,$|ICO| <span style="color:red">GL</span> | Global data |
LIV |  | <span style="color:green">**Ok**</span>  |
$\,$|LIV| <span style="color:red">GL</span> | Global data |
LSP |  | <span style="color:red">GL</span> | Global data |
MAR |  | <span style="color:red">GL</span> | Global data |
NP  |  | <span style="color:red">GL</span> | Global data |
SPP |  |<span style="color:green">**Ok**</span> |
TR  |  |<span style="color:green">**Ok**</span> |   |  

# Latest scores (29 September 2019)
```
> scores %>% filter(dimension %in% c("status", "score"))
     goal dimension region_id  score
1      AO     score         0  88.27
2      AO     score         6  86.77
3      AO     score         7  89.77
4      AO    status         0  81.53
5      AO    status         6  80.72
6      AO    status         7  82.34
7      BD     score         0  72.00
8      BD     score         6  70.99
9      BD     score         7  73.00
10     BD    status         0  76.71
11     BD    status         6  76.72
12     BD    status         7  76.71
13     CP     score         0  76.09
14     CP     score         6  72.52
15     CP     score         7  79.66
16     CP    status         0  96.59
17     CP    status         6  99.96
18     CP    status         7  93.22
19     CS     score         0  15.85
20     CS     score         6  15.12
21     CS     score         7  16.58
22     CS    status         0  20.26
23     CS    status         6  20.99
24     CS    status         7  19.53
25     CW     score         0  72.63
26     CW     score         6  70.57
27     CW     score         7  74.70
28     CW    status         0  75.85
29     CW    status         6  72.29
30     CW    status         7  79.41
31    ECO     score         0  84.11
32    ECO     score         6  98.68
33    ECO     score         7  69.55
34    ECO    status         0  98.68
35    ECO    status         6  97.36
36    ECO    status         7 100.00
37    FIS     score         0  54.56
38    FIS     score         6  54.56
39    FIS     score         7  54.56
40    FIS    status         0  53.20
41    FIS    status         6  53.20
42    FIS    status         7  53.20
43     FP     score         0  76.50
44     FP     score         6  76.50
45     FP     score         7  76.50
46     FP    status         0  75.80
47     FP    status         6  75.80
48     FP    status         7  75.80
49    HAB     score         0  46.58
50    HAB     score         6  44.57
51    HAB     score         7  48.59
52    HAB    status         0  58.60
53    HAB    status         6  58.61
54    HAB    status         7  58.59
55    ICO     score         0  69.50
56    ICO     score         6  69.08
57    ICO     score         7  69.92
58    ICO    status         0  64.12
59    ICO    status         6  64.12
60    ICO    status         7  64.12
61  Index     score         0  71.90
62  Index     score         6  73.11
63  Index     score         7  70.68
64     LE     score         0  91.81
65     LE     score         6  99.09
66     LE     score         7  84.52
67     LE    status         0  98.84
68     LE    status         6  98.18
69     LE    status         7  99.50
70    LIV     score         0  99.50
71    LIV     score         6  99.50
72    LIV     score         7  99.50
73    LIV    status         0  98.99
74    LIV    status         6  98.99
75    LIV    status         7  98.99
76    LSP     score         0 100.00
77    LSP     score         6 100.00
78    LSP     score         7 100.00
79    LSP    status         0 100.00
80    LSP    status         6 100.00
81    LSP    status         7 100.00
82    MAR     score         0 100.00
83    MAR     score         6 100.00
84    MAR     score         7 100.00
85    MAR    status         0 100.00
86    MAR    status         6 100.00
87    MAR    status         7 100.00
88     NP     score         0  56.06
89     NP     score         6  56.06
90     NP     score         7  56.06
91     NP    status         0  52.38
92     NP    status         6  52.38
93     NP    status         7  52.38
94     SP     score         0  84.75
95     SP     score         6  84.54
96     SP     score         7  84.96
97     SP    status         0  82.06
98     SP    status         6  82.06
99     SP    status         7  82.06
100   SPP     score         0  97.41
101   SPP     score         6  97.41
102   SPP     score         7  97.41
103   SPP    status         0  94.82
104   SPP    status         6  94.82
105   SPP    status         7  94.82
106    TR     score         0  85.01
107    TR     score         6  98.98
108    TR     score         7  71.03
109    TR    status         0  83.53
110    TR    status         6  97.97
111    TR    status         7  69.09
```

# Updates 28 September 2019
  1. Local `fis_meancatch` layer does not contain data column and is using illegal characters e.g. "ñ".
  3. MAR goal has fixed URL file for layer data! this should point to a local layer!
```
uninhabited <- read.csv("https://raw.githubusercontent.com/OHI-Science/ohiprep/master/globalprep/spatial/v2017/output/rgn_uninhabited_islands.csv")
```
    is replaced by empty data frame, i.e., we don't include island data.
    It also filters scores to only include `region_id`s 6 and 7.
  4. Notes from `CalculateAll()`
  
```
  Some regions/habitats have extent data, but no trend data. Consider estimating these values. 

Calculating Status and Trend for each region for SPP...
Calculating Pressures for each region...
There are 6 pressures subcategories: 
  pollution, 
  alien_species, 
  habitat_destruction, 
  fishing_pressure, 
  climate_change, 
  social
  
These goal-elements are in the weighting data layers, but not included in the pressure_matrix.csv:
  LIV-tra, 
  ECO-tra
  
These goal-elements are in the pressure_matrix.csv, but not included in the weighting data layers:
  ECO-aqf, 
  ECO-mar, 
  LIV-mar, 
  CP-saltmarsh, 
  CP-seagrass, 
  CS-saltmarsh, 
  CS-seagrass, 
  HAB-saltmarsh, 
  HAB-seagrass, 
  NP-shells, 
  NP-sponges, 
  ECO-mmw, 
  LIV-mmw, 
  LIV-ph, 
  LIV-tran, 
  CP-seaice_shoreline, 
  HAB-seaice_edge, 
  ECO-wte, 
  LIV-wte, 
  LIV-sb
  
Calculating Resilience for each region...
There are 7 Resilience subcategories: 
  ecological, 
  alien_species, 
  goal, 
  fishing_pressure, 
  habitat_destruction, 
  pollution, 
  social 

These goal-elements are in the resilience_matrix.csv, but not included in the weighting data layers:
  CP-saltmarsh, 
  CP-seagrass, 
  CS-saltmarsh, 
  CS-seagrass, 
  HAB-saltmarsh, 
  HAB-seagrass, 
  NP-shells, 
  NP-sponges, 
  HAB-seaice_edge, 
  CP-seaice_shoreline
```

# Updates 31 August 2019
  1. Incorrectly named layer `cw_nutrients_trend_mse2019.csv` renamed to `cw_nutrient_trend_mse2019.csv`
  2. Removed unknown file layer `region2019/layers/hab_softbottom_mse2019.csv`
  3. `LAYERS.CSV` was not fully updated, following entries where corrected
      `hab_coral_extent_mse2019.csv` and `element_wts_hab_pres_abs_mse2019.csv`

# Scores 31 August 2019
```
AO(layers = layers)
  region_id   score dimension goal
1         6 80.7150    status   AO
2         7 82.3390    status   AO
3         6  0.0298     trend   AO
4         7  0.0741     trend   AO
```
```
CW(layers)
  region_id goal dimension       score
1         6   CW    status 72.29151383
2         7   CW    status 79.40565609
3         6   CW     trend -0.09486703
4         7   CW     trend -0.25114921
```
```
ECO(layers)
  region_id goal dimension       score
1         6  ECO    status  97.3600000
2         7  ECO    status 100.0000000
3         6  ECO     trend   0.4523954
4         7  ECO     trend  -1.0000000
```
```
LIV(layers)
  region_id goal dimension      score
1         6  LIV    status 98.9924668
2         7  LIV    status 98.9924668
3         6  LIV     trend  0.9519295
4         7  LIV     trend  0.9342872
```
```
SPP(layers)
  region_id goal dimension        score
1         6  SPP    status 94.824902700
2         7  SPP    status 94.824902700
3         6  SPP     trend -0.004867257
4         7  SPP     trend -0.004867257
```
```
TR(layers)
  region_id goal dimension    score
1         6   TR    status 97.96545
2         7   TR    status 69.08675
3         6   TR     trend -0.02480
4         7   TR     trend -0.05590
```

# Updates from 20 July 2019 - NOTES

Most of the problems are solved by updating the mistical `scen_data_year.csv` sheet. In fact, almost all the NA rows
are generated by data provided in this sheet. Some common problems where

  1. Incorrectly reported available data
  2. layers generally have TWO groups where they report available scenario/data years, only the first group was updated.
  3. Some of the updates in group 1 has missaligned years. As the documente for alignments states:
      (see http://ohi-science.org/ohicore/reference/AlignDataYears.html)
      Data should be aligned per available year of closes match.
      
> AlignDataYears
> Source: R/AlignDataYears.R
> 
> Used in conf/functions.R to link the year data was collected to the 
> appropriate scenario year for a data layer. A dataframe is returned 
> with both the **data year and the corresponding scenario year**. 
> The scenario year is used to join data layers with different data 
> years for use in models.




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
Working domain

  *  Status 0-100
  *  Trend -100 to +100

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

Problem in data layer `liv_trend_mse2019.csv`
```
rgn_id,year,trend
6,2017,0.452395374
7,2017,-1.503209681                       <- OUT OF RANGE per layers.csv: -1 to +1
```

Working domain

  *  Status 0 to 100
  *  Trend -1 to +1

# LIV [OK]

Fixed and scores don't change.

Initial scores
```
  region_id goal dimension      score
1         6  LIV    status 98.9924668
2         7  LIV    status 98.9924668
3        NA  LIV    status         NA
4         6  LIV     trend  0.9519295
5         7  LIV     trend  0.9342872
6        NA  LIV     trend         NA
```

Working domain

  *  Status 0 to 100
  *  Trend -1 to +1

Final fixed scores
```
  region_id goal dimension      score
1         6  LIV    status 98.9924668
2         7  LIV    status 98.9924668
3         6  LIV     trend  0.9519295
4         7  LIV     trend  0.9342872
```

Updated `scenario_data_years.csv` `diff -u`
```diff
»  git diff scenario_data_years.csv
diff --git a/region2019/conf/scenario_data_years.csv b/region2019/conf/scenario_data_years.csv
index 27e4626..67367ff 100644
--- a/region2019/conf/scenario_data_years.csv
+++ b/region2019/conf/scenario_data_years.csv
@@ -676,12 +676,10 @@
 liv_status,2015,2015
 liv_status,2016,2016
 liv_status,2017,2017
 liv_status,2018,2018
-liv_status,2019,2018
 liv_trend,2015,2018
 liv_trend,2016,2018
 liv_trend,2017,2018
 liv_trend,2018,2018
-liv_trend,2019,2019
 eco_status,2013,2013
 eco_status,2014,2014
 eco_status,2015,2015
@@ -760,8 +758,8 @@
 tr_jobs_pct_tourism,2019,2017
 tr_sustainability,2019,2017
 tr_travelwarnings,2019,2018
 wgi_all,2019,2016
-liv_status,2019,2013
-liv_trend,2019,2013
+liv_status,2019,2018
+liv_trend,2019,2019
 eco_status,2019,2017
 eco_trend,2019,2017
 species_diversity_3nm,2019,2018
```
# SPP [OK]
This layer only does a simple linear transform on layer data.
```
  region_id goal dimension        score
1         6  SPP    status 94.824902700
2         7  SPP    status 94.824902700
3         6  SPP     trend -0.004867257
4         7  SPP     trend -0.004867257
```

Working domain

  *  Status 0 to 100
  *  Trend -1 to +1

Note: `scen_data_year.csv` does not report on available data from TREND component.
Assumes it matches with STATUS layer data (!).

# TR [NO-OK] SCORES CHANGED
Problem with data layer `tr_sustainability_mse2019.csv` variable `S_score` out of range (0 to 1)
```
rgn_id,year,S_score
6,2017,3.91
7,2017,3.91
```
Reading `TR` funtion, potential fix it to scale with respect to max TTCI index of 7.0, so new scores could be
3.91 / 7.0 for both regions.

Initial score table
```
> TR(layers)
  region_id goal dimension     score
1         6   TR    status 100.00000
2         7   TR    status  70.52154
3         6   TR     trend   0.21380
4         7   TR     trend   0.21380
```
Temporary updated scores **SCORES CHANGED** revision required
```
  region_id goal dimension    score
1         6   TR    status 97.96545
2         7   TR    status 69.08675
3         6   TR     trend -0.02480
4         7   TR     trend -0.05590
```
Additional fixes to `scenario_data_year.csv`
```
»  git diff ../conf/scenario_data_years.csv
diff --git a/region2019/conf/scenario_data_years.csv b/region2019/conf/scenario_data_years.csv
index 67367ff..74cb609 100644
--- a/region2019/conf/scenario_data_years.csv
+++ b/region2019/conf/scenario_data_years.csv
@@ -638,15 +638,15 @@ ss_wgi,2015,2013
 ss_wgi,2016,2014
 ss_wgi,2017,2015
 ss_wgi,2018,2016
-tr_jobs_pct_tourism,2010,2009
-tr_jobs_pct_tourism,2011,2010
-tr_jobs_pct_tourism,2012,2011
-tr_jobs_pct_tourism,2013,2012
-tr_jobs_pct_tourism,2014,2013
-tr_jobs_pct_tourism,2015,2014
-tr_jobs_pct_tourism,2016,2015
-tr_jobs_pct_tourism,2017,2016
-tr_jobs_pct_tourism,2018,2017
+tr_jobs_pct_tourism,2010,2010
+tr_jobs_pct_tourism,2011,2011
+tr_jobs_pct_tourism,2012,2012
+tr_jobs_pct_tourism,2013,2013
+tr_jobs_pct_tourism,2014,2014
+tr_jobs_pct_tourism,2015,2015
+tr_jobs_pct_tourism,2016,2016
+tr_jobs_pct_tourism,2017,2017
+tr_jobs_pct_tourism,2018,2018
 tr_sustainability,2010,2017
 tr_sustainability,2011,2017
 tr_sustainability,2012,2017
@@ -754,7 +754,7 @@ res_spi,2019,2018
 sp_genetic,2019,2016
 ss_spi,2019,2018
 ss_wgi,2019,2016
-tr_jobs_pct_tourism,2019,2017
+tr_jobs_pct_tourism,2019,2018^M
 tr_sustainability,2019,2017
 tr_travelwarnings,2019,2018
 wgi_all,2019,2016
```

Working domain

  *  Status 0-100
  *  Trend 0-1
  

# HAB [] GL2018
```
> HAB(layers)
# A tibble: 0 x 4
# … with 4 variables: region_id <int>, goal <chr>, dimension <chr>, score <dbl>
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


  *  `[D]`  LIV
  *  `[D]`  SPP
  *  `[ ]`  HAB
  *  `[ ]`  ICO Commented last part where unknown object are referenced.

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

