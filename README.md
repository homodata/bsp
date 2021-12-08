---
title: "OHI for BSP"
author: "HomoData"
date: "8 Dec 2021"
output: html_document
---
# Ocean Health Index for Bahia de Sechura (Peru) [bsp]

This is the Ocean Health Index repository for Bahia de Sechura (Peru)

# Region ID and names

 Id|Name                       | Alias
 --|---------------------------|------
0  | `Bahia de Sechura (Peru)` | 
1  | `Sechura`                 | `Sur BSP`
2  | `Vice`                    | `Norte BSP`

# Score Tables BSP
Score tables are generated using
`> scores %>% filter(dimension %in% c("status","trend", "score"))`

Available tables

 * 2021/04/26 [Reference (last from mse) `scores_reference.tbl`](scores_reference.tbl)
 * 2021/04/27 [Score table with region ID change (`6` to `1` and `7` to `2`) `scores_bsp_rgns.tbl`](scores_bsp_rgns.tbl)

# Goals Progress Report

goal|region|layer issues | action  | Completion 
----|------|-------------|---------|-------------
FIS | BSP  | <span style="color:green">  </span> | local data | 100%
MAR | BSP  | <span style="color:green">  </span> | local data | 100%
FP  | BSP  | <span style="color:green">  </span> | local data | 100%
AO  | BSP  | <span style="color:green">  </span> | local data | 100%
NP  | BSP  | <span style="color:green">  </span> | local data | 100%
CS  | BSP  | <span style="color:green">  </span> | local data | 100%
CP  | BSP  | <span style="color:green">  </span> | local data | 100%
TR  | BSP  | <span style="color:green">  </span> | local data | 100%
LIV | BSP  | <span style="color:green">  </span> | local data | 100%
ECO | BSP  | <span style="color:green">  </span> | local data | 100%
LE  | BSP  | <span style="color:green">  </span> | local data | 100%
ICO | BSP  | <span style="color:green">  </span> | local data | 100%
LSP | BSP  | <span style="color:green">  </span> | local data | 100%
SP  | BSP  | <span style="color:green">  </span> | local data | 100%
CW  | BSP  | <span style="color:green">  </span> | local data | 100%
HAB | BSP  | <span style="color:green">  </span> | local data | 100%
SPP | BSP  | <span style="color:green">  </span> | local data | 100%
BD  | BSP  | <span style="color:green">  </span> | local data | 100%
**rgn**|BSP| Complete                            | local data | 100%

# Plots

<table><tr>
<td><img src="./region2020/reports/figures/flower_BahiadeSechura(Peru).png" width="375px" alt="Bahia de Sechura (Peru)"/></td>
<td><img src="./region2020/reports/figures/flower_Sechura.png" width="375px" alt="Sechura (Sur BSP)"/></td>
<td><img src="./region2020/reports/figures/flower_Vice.png" width="375px" alt="Vice (Norte BSP)"/></td>
</tr></table>

# To Do list
  * Plot flower
```
Using layers/fp_wildcaught_weight_gl2018.csv to plot FIS and MAR with unequal weighting
```

## FIXME in `functions.R`
  - [x] Fixme L313
```
313:  # FIXME MSE UPDATE: Filter to return only regions of interest 1:2 !
314-  # All uninhabited regions 1:250 are forced to zero (i.e. this edition
315-  # does not include island data)
```
  - [ ] Fixme L1068
```
1068:  # FIXME NOTE: scripts and related files for calculating these subgoals is located:
1069-  # mse/archive
1070-  # These data are no longer available and status/trend have not been updated since 2013
```
  - [ ] Fixme L1102
```
1102:  # FIXME NOTE: scripts and related files for calculating these subgoals is located:
1103-  # mse/archive
1104-  # These data are no longer available and status/trend have not been updated since 2013
```
