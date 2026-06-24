# TAREAFONTURBELAB
# Análisis de sensillas y antenomeros antenales en Euborellia annullipes

Comparación de sensillas entre machos y hembras de Euborellia annullipes mediante pruebas no paramétricas y GLMM.

## Requisitos

R 4.0 o superior con los siguientes paquetes:

install.packages(c("tidyverse", "rstatix", "ggpubr", "car", "coin", "glmmTMB"))

## Datos

El archivo `sens_data.csv`  y `anten_data.csv` deben estar en el directorio de trabajo.

## Reproducir el análisis

Abrir `SENS.Rmd` y `ANTEN.Rmd`en RStudio y ejecutar todos los chunks en orden, o abrir el archivo `TAREAFONTURBELAB.Rproj` para abrir los dos archivos a la vez.

## Contenido del repositorio

- `SENS.Rmd` — código completo del análisis
- `ANTEN.Rmd` — código completo del análisis
- `sens_data.csv` — datos de sensillas
- `anten_data.csv` — datos de sensillas
- `TAREAFONTURBELAB.Rproj` — Archivo del proyecto en R
- `ANTEN.html` y `SENS.html` - archivos de visualizacion del codigo en HTML.
- `README.md` — este archivo
