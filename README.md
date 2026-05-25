---
title: "Análisis de datos"
format:
  html:
    toc: true
    toc-expand: true
    toc-depth: 4
    toc-location: left
    number-sections: true
    self-contained: true
    code-fold: true
    output-file: "ESM"
editor_options: 
  chunk_output_type: console
execute: 
  warning: false
  message: false
  echo: true
---

# Project Setup

```{r}
#| label:  setup

source('https://inkaverse.com/setup.r')
```

# Data import

```{r}
gs <- "https://docs.google.com/spreadsheets/d/1DxRhmFtBscdZkNRlOHaP2ZLf2yYz6IKwg1cF9elXY84/edit?gid=1390923633#gid=1390923633" %>% 
  as_sheets_id()

fb <- gs %>% 
  range_read(ss = .,sheet = "fb")
