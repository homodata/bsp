---
title: "Scores IdSO MSE"
author: "Lelys"
date: "8/31/2019"
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
BD| MSE | Requires final scores | Revision required



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
  region_id goal dimension       score
1         6   CW    status 72.29151383
2         7   CW    status 79.40565609
3         6   CW     trend -0.09486703
4         7   CW     trend -0.25114921
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

#Latest Scores after Lelys's revision (Oct 10 2019)

```
> scores %>% filter(dimension %in% c("status","trend", "score"))
     goal dimension region_id  score
1      AO     score         0  88.21
2      AO     score         6  86.68
3      AO     score         7  89.73
4      AO    status         0  81.53
5      AO    status         6  80.72
6      AO    status         7  82.34
7      AO     trend         6   0.03
8      AO     trend         7   0.07
9      BD     score         0  71.95
10     BD     score         6  70.92
11     BD     score         7  72.98
12     BD    status         0  76.71
13     BD    status         6  76.72
14     BD    status         7  76.71
15     BD     trend         6  -0.44
16     BD     trend         7  -0.34
17     CP     score         0  75.91
18     CP     score         6  72.17
19     CP     score         7  79.64
20     CP    status         0  96.59
21     CP    status         6  99.96
22     CP    status         7  93.22
23     CP     trend         6  -1.00
24     CP     trend         7  -0.62
25     CS     score         0  15.83
26     CS     score         6  15.09
27     CS     score         7  16.57
28     CS    status         0  20.26
29     CS    status         6  20.99
30     CS    status         7  19.53
31     CS     trend         6  -1.00
32     CS     trend         7  -0.62
33     CW     score         0  69.79
34     CW     score         6  68.82
35     CW     score         7  70.76
36     CW    status         0  69.92
37     CW    status         6  63.62
38     CW    status         7  76.22
39     CW     trend         6   0.22
40     CW     trend         7  -0.26
41    ECO     score         0  84.02
42    ECO     score         6  98.68
43    ECO     score         7  69.37
44    ECO    status         0  98.68
45    ECO    status         6  97.36
46    ECO    status         7 100.00
47    ECO     trend         6   0.45
48    ECO     trend         7  -1.00
49    FIS     score         0  57.94
50    FIS     score         6  57.94
51    FIS     score         7  57.94
52    FIS    status         0  55.50
53    FIS    status         6  55.50
54    FIS    status         7  55.50
55    FIS     trend         6   0.00
56    FIS     trend         7   0.00
57     FP     score         0  78.25
58     FP     score         6  78.25
59     FP     score         7  78.25
60     FP    status         0  76.99
61     FP    status         6  76.99
62     FP    status         7  76.99
63     FP     trend         6   0.22
64     FP     trend         7   0.22
65    HAB     score         0  46.48
66    HAB     score         6  44.42
67    HAB     score         7  48.54
68    HAB    status         0  58.60
69    HAB    status         6  58.61
70    HAB    status         7  58.59
71    HAB     trend         6  -0.88
72    HAB     trend         7  -0.67
73    ICO     score         0  69.36
74    ICO     score         6  68.88
75    ICO     score         7  69.84
76    ICO    status         0  64.12
77    ICO    status         6  64.12
78    ICO    status         7  64.12
79    ICO     trend         6   0.11
80    ICO     trend         7   0.14
81  Index     score         0  71.89
82  Index     score         6  73.23
83  Index     score         7  70.55
84     LE     score         0  91.76
85     LE     score         6  99.09
86     LE     score         7  84.43
87     LE    status         0  98.84
88     LE    status         6  98.18
89     LE    status         7  99.50
90     LE     trend         6   0.70
91     LE     trend         7  -0.03
92    LIV     score         0  99.50
93    LIV     score         6  99.50
94    LIV     score         7  99.50
95    LIV    status         0  98.99
96    LIV    status         6  98.99
97    LIV    status         7  98.99
98    LIV     trend         6   0.95
99    LIV     trend         7   0.93
100   LSP     score         0 100.00
101   LSP     score         6 100.00
102   LSP     score         7 100.00
103   LSP    status         0 100.00
104   LSP    status         6 100.00
105   LSP    status         7 100.00
106   LSP     trend         6   0.00
107   LSP     trend         7   0.00
108   MAR     score         0 100.00
109   MAR     score         6 100.00
110   MAR     score         7 100.00
111   MAR    status         0 100.00
112   MAR    status         6 100.00
113   MAR    status         7 100.00
114   MAR     trend         6   0.46
115   MAR     trend         7   0.46
116    NP     score         0  58.45
117    NP     score         6  58.45
118    NP     score         7  58.45
119    NP    status         0  54.62
120    NP    status         6  54.62
121    NP    status         7  54.62
122    NP     trend         6   0.01
123    NP     trend         7   0.01
124    SP     score         0  84.68
125    SP     score         6  84.44
126    SP     score         7  84.92
127    SP    status         0  82.06
128    SP    status         6  82.06
129    SP    status         7  82.06
130    SP     trend         6   0.06
131    SP     trend         7   0.07
132   SPP     score         0  97.41
133   SPP     score         6  97.41
134   SPP     score         7  97.41
135   SPP    status         0  94.82
136   SPP    status         6  94.82
137   SPP    status         7  94.82
138   SPP     trend         6   0.00
139   SPP     trend         7   0.00
140    TR     score         0  84.11
141    TR     score         6  98.41
142    TR     score         7  69.81
143    TR    status         0  82.55
144    TR    status         6  96.82
145    TR    status         7  68.28
146    TR     trend         6  -0.03
147    TR     trend         7  -0.06
```

#Latest Scores  (Oct 24 2019)

```
> scores %>% filter(dimension %in% c("status","trend", "score"))
     goal dimension region_id  score
1      AO     score         0  88.21
2      AO     score         6  86.68
3      AO     score         7  89.73
4      AO    status         0  81.53
5      AO    status         6  80.72
6      AO    status         7  82.34
7      AO     trend         6   0.03
8      AO     trend         7   0.07
9      BD     score         0  71.95
10     BD     score         6  70.92
11     BD     score         7  72.98
12     BD    status         0  76.71
13     BD    status         6  76.72
14     BD    status         7  76.71
15     BD     trend         6  -0.44
16     BD     trend         7  -0.34
17     CP     score         0  75.91
18     CP     score         6  72.17
19     CP     score         7  79.64
20     CP    status         0  96.59
21     CP    status         6  99.96
22     CP    status         7  93.22
23     CP     trend         6  -1.00
24     CP     trend         7  -0.62
25     CS     score         0  15.83
26     CS     score         6  15.09
27     CS     score         7  16.57
28     CS    status         0  20.26
29     CS    status         6  20.99
30     CS    status         7  19.53
31     CS     trend         6  -1.00
32     CS     trend         7  -0.62
33     CW     score         0  68.70
34     CW     score         6  63.38
35     CW     score         7  74.01
36     CW    status         0  69.92
37     CW    status         6  63.62
38     CW    status         7  76.22
39     CW     trend         6  -0.03
40     CW     trend         7  -0.13
41    ECO     score         0  84.02
42    ECO     score         6  98.68
43    ECO     score         7  69.37
44    ECO    status         0  98.68
45    ECO    status         6  97.36
46    ECO    status         7 100.00
47    ECO     trend         6   0.45
48    ECO     trend         7  -1.00
49    FIS     score         0  57.94
50    FIS     score         6  57.94
51    FIS     score         7  57.94
52    FIS    status         0  55.50
53    FIS    status         6  55.50
54    FIS    status         7  55.50
55    FIS     trend         6   0.00
56    FIS     trend         7   0.00
57     FP     score         0  78.25
58     FP     score         6  78.25
59     FP     score         7  78.25
60     FP    status         0  76.99
61     FP    status         6  76.99
62     FP    status         7  76.99
63     FP     trend         6   0.22
64     FP     trend         7   0.22
65    HAB     score         0  46.48
66    HAB     score         6  44.42
67    HAB     score         7  48.54
68    HAB    status         0  58.60
69    HAB    status         6  58.61
70    HAB    status         7  58.59
71    HAB     trend         6  -0.88
72    HAB     trend         7  -0.67
73    ICO     score         0  69.36
74    ICO     score         6  68.88
75    ICO     score         7  69.84
76    ICO    status         0  64.12
77    ICO    status         6  64.12
78    ICO    status         7  64.12
79    ICO     trend         6   0.11
80    ICO     trend         7   0.14
81  Index     score         0  71.78
82  Index     score         6  72.69
83  Index     score         7  70.88
84     LE     score         0  91.76
85     LE     score         6  99.09
86     LE     score         7  84.43
87     LE    status         0  98.84
88     LE    status         6  98.18
89     LE    status         7  99.50
90     LE     trend         6   0.70
91     LE     trend         7  -0.03
92    LIV     score         0  99.50
93    LIV     score         6  99.50
94    LIV     score         7  99.50
95    LIV    status         0  98.99
96    LIV    status         6  98.99
97    LIV    status         7  98.99
98    LIV     trend         6   0.95
99    LIV     trend         7   0.93
100   LSP     score         0 100.00
101   LSP     score         6 100.00
102   LSP     score         7 100.00
103   LSP    status         0 100.00
104   LSP    status         6 100.00
105   LSP    status         7 100.00
106   LSP     trend         6   0.00
107   LSP     trend         7   0.00
108   MAR     score         0 100.00
109   MAR     score         6 100.00
110   MAR     score         7 100.00
111   MAR    status         0 100.00
112   MAR    status         6 100.00
113   MAR    status         7 100.00
114   MAR     trend         6   0.46
115   MAR     trend         7   0.46
116    NP     score         0  58.45
117    NP     score         6  58.45
118    NP     score         7  58.45
119    NP    status         0  54.62
120    NP    status         6  54.62
121    NP    status         7  54.62
122    NP     trend         6   0.01
123    NP     trend         7   0.01
124    SP     score         0  84.68
125    SP     score         6  84.44
126    SP     score         7  84.92
127    SP    status         0  82.06
128    SP    status         6  82.06
129    SP    status         7  82.06
130    SP     trend         6   0.06
131    SP     trend         7   0.07
132   SPP     score         0  97.41
133   SPP     score         6  97.41
134   SPP     score         7  97.41
135   SPP    status         0  94.82
136   SPP    status         6  94.82
137   SPP    status         7  94.82
138   SPP     trend         6   0.00
139   SPP     trend         7   0.00
140    TR     score         0  84.11
141    TR     score         6  98.41
142    TR     score         7  69.81
143    TR    status         0  82.55
144    TR    status         6  96.82
145    TR    status         7  68.28
146    TR     trend         6  -0.03
147    TR     trend         7  -0.06
```