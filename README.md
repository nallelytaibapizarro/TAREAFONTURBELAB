# Caracterización morfométrica y sensorial de antenas en Euborellia annulipes

Análisis estadístico comparativo de la morfometría antenomérica y el equipamiento 
sensorial entre machos y hembras adultos de *Euborellia annulipes* (Dermaptera: 
Anisolabididae), mediante microscopía electrónica de barrido (SEM) e imágenes 
procesadas en Fiji/ImageJ.

**Autora:** Nallely Taiba Pizarro  
**Curso:** Diseño Experimental y Bioestadística — Magíster en Ciencias Biológicas, PUCV (2026)

---

## Requisitos

R 4.5 o superior con los siguientes paquetes:

```r
install.packages(c("tidyverse", "rstatix", "ggpubr", "car", 
                   "coin", "glmmTMB", "DHARMa", "emmeans",
                   "FactoMineR", "factoextra"))
```

---

## Datos

Los archivos `sens_data.csv` y `anten_data.csv` deben estar en la misma 
carpeta que los scripts `.Rmd`. En RStudio, establecer el directorio de 
trabajo con:

```r
Session → Set Working Directory → To Source File Location
```

---

## Cómo reproducir el análisis

Abrir cada archivo `.Rmd` en RStudio y hacer click en **Knit**, 
en el siguiente orden:

1. `ANTEN.Rmd` — análisis exploratorio de morfometría
2. `PCA_morfometria.Rmd` — análisis multivariado de morfometría
3. `SENS__1_.Rmd` — análisis exploratorio de sensillas + GLMM inicial
4. `SENS_con_DHARMa.Rmd` — diagnóstico de supuestos con DHARMa
5. `SENS_binomial_negativa.Rmd` — modelos finales con reajuste por sobredispersión

Alternativamente, abrir `TAREAFONTURBELAB.Rproj` para cargar 
el proyecto completo en RStudio.

---

## Contenido del repositorio

### Scripts R

| Archivo | Descripción |
|---|---|
| `ANTEN.Rmd` | Morfometría antenomérica: Shapiro-Wilk, Levene, Wilcoxon-BH, modelos lineales (AIC/BIC) |
| `PCA_morfometria.Rmd` | PCA de morfometría: varianza explicada por componente, biplots por sexo, superficie e interacción |
| `SENS__1_.Rmd` | Sensillas: Shapiro-Wilk, Wilcoxon-Bonferroni, GLMM Poisson inicial |
| `SENS_con_DHARMa.Rmd` | Diagnóstico de residuos con DHARMa (uniformidad, sobredispersión, outliers) |
| `SENS_binomial_negativa.Rmd` | Modelos finales: Poisson (TR) y Binomial Negativa (BS, CH, TOTAL); Wald tipo III; post hoc emmeans |

### Outputs HTML

| Archivo | Descripción |
|---|---|
| `ANTEN.html` | Output del análisis exploratorio de morfometría |
| `PCA_morfometria.html` | Output del PCA con resultados numéricos y biplots |
| `SENS__1_.html` | Output del análisis exploratorio de sensillas |
| `SENS_con_DHARMa.html` | Output del diagnóstico DHARMa |
| `SENS_binomial_negativa.html` | Output de los modelos finales con binomial negativa |

### Datos y proyecto

| Archivo | Descripción |
|---|---|
| `sens_data.csv` | Conteo de sensillas por flagelómero e individuo |
| `anten_data.csv` | Mediciones morfométricas por flagelómero e individuo |
| `TAREAFONTURBELAB.Rproj` | Proyecto RStudio |
| `README.md` | Este archivo |

