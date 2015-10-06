---
title       : Data Visualization
subtitle    : Week 1
author      : Kieran Healy
job         : Duke University
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : solarized_light      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---



## What Data Values are Displayed in this Figure?

![A 3-D Column Chart created in Excel for Mac](../assets/wk-01-excel-3d-column-chart.png)

---

## 

![Excel 3-D Column Chart with Values shown](../assets/wk-01-excel-3d-column-chart-values.png)

---



## What about this one?

![A 3-D Pie Chart created in Excel for Mac](../assets/wk-01-excel-3d-pie-chart.png)

---

## 

![A 3-D Pie Chart created in Excel for Mac](../assets/wk-01-excel-3d-pie-chart-values.png)

---



## Let's get some Data ...


```r
library(ggplot2)
library(devtools)

gapminder.url <- "https://raw.githubusercontent.com/socviz/soc880/master/data/gapminder.csv"
data <- read.csv(url(gapminder.url))
head(data)
```

```
##   country continent year lifeExp      pop gdpPercap
## 1 Algeria    Africa 1952  43.077  9279525  2449.008
## 2 Algeria    Africa 1957  45.685 10270856  3013.976
## 3 Algeria    Africa 1962  48.303 11000948  2550.817
## 4 Algeria    Africa 1967  51.407 12760499  3246.992
## 5 Algeria    Africa 1972  54.518 14760787  4182.664
## 6 Algeria    Africa 1977  58.014 17152804  4910.417
```

---

## ... and Plot it


```r
p <- ggplot(data, aes(x=gdpPercap, y=lifeExp))
p + geom_point()
```

<img src="assets/fig/FirstPlot-2-1.png" title="plot of chunk FirstPlot-2" alt="plot of chunk FirstPlot-2" style="display: block; margin: auto;" />

---
