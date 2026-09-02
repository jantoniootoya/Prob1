# Proyecto Final de Inferencia Estadística

## Distance Sampling para estimación de densidad y abundancia

**Autor:** José Antonio Otoya Barrenechea  
**Programa:** Maestría en Ciencias e Ingeniería Estadística — Universidad Nacional de Ingeniería  
**ORCID:** 0009-0007-0702-6958

[![Abrir en Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jantoniootoya/Prob1/blob/main/ProyectoFinalOtoya.ipynb)

Este repositorio contiene el proyecto final de Probabilidades e Inferencia Estadística desarrollado íntegramente en **Python** y preparado para ejecutarse en **Google Colab**.

## Cuaderno principal

`ProyectoFinalOtoya.ipynb`

El notebook descarga automáticamente:

- `wren_5min.csv`
- `wren_lt.csv`

desde este mismo repositorio, por lo que no es necesario cargar manualmente los archivos en Colab.

## Metodología

La secuencia inferencial es:

```text
distancias observadas
→ modelo probabilístico de detección
→ máxima verosimilitud
→ probabilidad de detección
→ densidad
→ abundancia
→ cuantificación de incertidumbre
```

La función de detección utilizada es half-normal:

$$
g(d;\sigma)
=
\exp\left(-\frac{d^2}{2\sigma^2}\right).
$$

Se comparan dos diseños:

- Point transect.
- Line transect.

La inferencia del parámetro de detección se realiza mediante máxima verosimilitud. Para cuantificar conjuntamente la incertidumbre de densidad y detección se explicita un supuesto adicional de proceso espacial homogéneo de Poisson y se utiliza la información observada derivada del Hessiano.

No se utiliza bootstrap.

## Abrir en Google Colab

Una vez que `Proyecto_Final_Distance_Sampling_Colab.ipynb` esté en la rama `main`, usar:

https://colab.research.google.com/github/jantoniootoya/Prob1/blob/main/ProyectoFinalOtoya.ipynb

También puede abrirse desde Colab seleccionando:

```text
Archivo
→ Abrir cuaderno
→ GitHub
→ jantoniootoya/Prob1
```

## Datos

`wren_5min.csv`

- Point transect.
- 134 detecciones.
- Distancia radial.

`wren_lt.csv`

- Line transect.
- 156 detecciones.
- Distancia perpendicular.

## Librerías

El notebook utiliza únicamente librerías disponibles habitualmente en Google Colab:

```python
numpy
pandas
matplotlib
scipy
```

## Repositorio

https://github.com/jantoniootoya/Prob1

## Autor

**José Antonio Otoya Barrenechea**  
Maestría en Ciencias e Ingeniería Estadística — Universidad Nacional de Ingeniería  
**ORCID:** https://orcid.org/0009-0007-0702-6958
