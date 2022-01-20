---
title: "R Markdown Test File"
author: "Kyle Hatch"
date: "1/19/2022"
output: 
  html_document: 
    keep_md: yes
---


```r
#### insert your brilliant WORKING code here
library(tidyverse)
```

```
## -- Attaching packages --------------------------------------- tidyverse 1.3.1 --
```

```
## v ggplot2 3.3.5     v purrr   0.3.4
## v tibble  3.1.6     v dplyr   1.0.7
## v tidyr   1.1.4     v stringr 1.4.0
## v readr   2.1.1     v forcats 0.5.1
```

```
## -- Conflicts ------------------------------------------ tidyverse_conflicts() --
## x dplyr::filter() masks stats::filter()
## x dplyr::lag()    masks stats::lag()
```

```r
set.seed(123)
df <- as_tibble(data.frame(x = 1:500, y = rnorm(500, mean = 1000, sd = 10000), z = rnorm(500, mean = 1000, sd = 1000000)))
library(ggplot2)
nonsense <- ggplot(df, aes(x=x, y=y, color = z)) +
  geom_point() +
  theme_bw()
nonsense
```

![](markdowntest_files/figure-html/unnamed-chunk-1-1.png)<!-- -->

