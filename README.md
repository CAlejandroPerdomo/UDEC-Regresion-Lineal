# Prediccion de la produccion de frutales en el Valle del Cauca

Proyecto sencillo de **regresion lineal** en Python 3.10+ que estima la produccion de frutales
(en toneladas) a partir del año, el municipio y las caracteristicas del cultivo.

## Descripcion del problema

El objetivo es predecir la variable continua `produccion_toneladas` para el cultivo de Plátano
(el que tiene mas datos) usando como predictores el año, el identificador numerico del municipio
(`id_municipio`) y la variable categorica `subregion` (codificada con `pd.get_dummies` en el
notebook 03).

## Estructura del proyecto

```
├── data/
│   ├── raw/            # archivo original, sin modificar
│   └── processed/      # dataset limpio
├── notebooks/
│   ├── 01_recoleccion.ipynb
│   ├── 02_eda.ipynb
│   ├── 03_modelo.ipynb
│   └── 04_evaluacion.ipynb
├── figures/            # graficos en PNG
├── requirements.txt
└── README.md
```

## Instalacion

```bash
pip install -r requirements.txt
```

## Orden de ejecucion

Ejecutar los notebooks en orden (cada uno es autocontenido):

1. `notebooks/01_recoleccion.ipynb` — copia el archivo a `data/raw/` y revisa la calidad.
2. `notebooks/02_eda.ipynb` — limpieza, EDA y guardado del dataset en `data/processed/`.
3. `notebooks/03_modelo.ipynb` — codifica categoricas, ajusta la regresion y valida supuestos.
4. `notebooks/04_evaluacion.ipynb` — metricas y graficos de evaluacion.

## Notas

- El archivo fuente original se encuentra en `./files/`.
- Las rutas son relativas y se resuelven automaticamente con `pathlib`.
- Las librerias usadas son: `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn` y `scipy`
  (esta ultima solo para el Q-Q plot del notebook 03).
