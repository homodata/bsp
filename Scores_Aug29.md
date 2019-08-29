---
title: "Scores IdSO MSE"
author: "Lelys"
date: "8/29/2019"
output: html_document
---

# Notes:
These are the score results after Sajo's review of the file `scen_data_year.csv` and other issues reported in <https://github.com/OHI-Science/mse/blob/master/ISSUES.md>. Trend files were corrected for values between [-1,1]. AO layers were corrected to convert unsatisfied basic needs to AO_needs.

# Table of progress
goal|status|layer issues | action
----|------|-------------|---------
FIS | GL | Global data| Use local data
MAR| GL | Global data | Use local data
FP| GL | Global data | Use local data
AO| MSE | <span style="color:orange">**Ok**</span> | Revision required 
NP| GL | Global data | Use local data
CS| MSE  | <span style="color:orange">**Ok**</span> | Revision required
CP| MSE  | <span style="color:orange">**Ok**</span> | Revision required
TR| MSE | <span style="color:red">**Ok**</span>| Revision required
LIV|MSE  | <span style="color:green">**Ok**</span>| Final revision
ECO | MSE | <span style="color:green">**Ok**</span>| Final revision
LE |MSE |Requires final layers | Final revision
ICO| MSE | R Code problems| Fix problem
LSP| GL | Global data | Use local data
SP| GL | Global data | Use local data + Fix R code problem
CW | MSE | <span style="color:green">**Ok**</span> | Final revision
HAB| MSE  | <span style="color:orange">**Ok**</span> | Revision required
SPP| MSE | <span style="color:orange">**Ok**</span>| Revision required
BD| MSE | Requires final layers | Revision required



## Scores
```
> AO(layers)
  region_id   score dimension goal
1         6 80.7150    status   AO
2         7 82.3390    status   AO
3         6  0.0298     trend   AO
4         7  0.0741     trend   AO

```
```
> CS(layers)
# A tibble: 4 x 4
  goal  dimension region_id  score
  <chr> <chr>         <int>  <dbl>
1 CS    status            6 21.0  
2 CS    status            7 19.5  
3 CS    trend             6 -1    
4 CS    trend             7 -0.619
```
```
> CP(layers)
# A tibble: 4 x 4
  region_id goal  dimension  score
      <int> <chr> <chr>      <dbl>
1         6 CP    status    21.0  
2         7 CP    status    19.5  
3         6 CP    trend     -1    
4         7 CP    trend     -0.619
> 
```
### TR: revision required

```
> TR(layers)
  region_id goal dimension    score
1         6   TR    status 97.96545
2         7   TR    status 69.08675
3         6   TR     trend -0.02480
4         7   TR     trend -0.05590
```
```
> LIV(layers)
  region_id goal dimension      score
1         6  LIV    status 98.9924668
2         7  LIV    status 98.9924668
3         6  LIV     trend  0.9519295
4         7  LIV     trend  0.9342872
```
```
> ECO(layers)
  region_id goal dimension       score
1         6  ECO    status  97.3600000
2         7  ECO    status 100.0000000
3         6  ECO     trend   0.4523954
4         7  ECO     trend  -1.0000000
```
```
> CW(layers)
  region_id goal dimension      score
1         6   CW    status 72.2915138
2         7   CW    status 79.4056561
3         6   CW     trend -0.5103900
4         7   CW     trend -0.7276086
```



```
> SPP(layers)
  region_id goal dimension        score
1         6  SPP    status 94.824902700
2         7  SPP    status 94.824902700
3         6  SPP     trend -0.004867257
4         7  SPP     trend -0.004867257
```


### ICO: gives R code error
```
> ICO(layers)
Error in tbl_vars(y) : object 'un_regions' not found
Called from: tbl_varsy)
```

```
> HAB(layers)
# A tibble: 4 x 4
  region_id goal  dimension  score
      <int> <chr> <chr>      <dbl>
1         6 HAB   status    37.9  
2         7 HAB   status    37.9  
3         6 HAB   trend     -0.876
4         7 HAB   trend     -0.674
```

```
> SPP(layers)
  region_id goal dimension        score
1         6  SPP    status 94.824902700
2         7  SPP    status 94.824902700
3         6  SPP     trend -0.004867257
4         7  SPP     trend -0.004867257
```






