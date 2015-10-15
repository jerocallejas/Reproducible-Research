---
output: html_document
---

PEER ASSESSMENT 1
=========================================================

#Reproducible research#
Jeronimo Callejas
October 14, 2015

In this fist assessment, i am going to make a simple linear regression with the ChickWeight [1] dataset in r.

[1] https://stat.ethz.ch/R-manual/R-devel/library/datasets/html/ChickWeight.html

```{r}
library(datasets)
data(ChickWeight)
summary(ChickWeight)
```

This specific data set contains information from an experiment on the effect of diet on early growth of chicks. We are going to test the effect of each diet on the growth of a chick by a simple regression model.

```{r, results='hide', echo=FALSE}
levels(ChickWeight$Diet)
```

```{r}
effect=lm(weight~Time+Diet, data=ChickWeight)
effect
```
