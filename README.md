# Análisis exploratorio del mercado de autos usados en Colombia

Análisis de la Guía de valores de Fasecolda (12.433 referencias de vehículos) para entender qué factores influyen en el precio de un vehículo usado: marca, cilindraje, peso, potencia y año-modelo.

## Contenido

| Archivo | Descripción |
|---|---|
| `proyecto_fasecolda.ipynb` | Notebook con el análisis completo (ya ejecutado, con gráficas y resultados) |
| `guia_fasecolda.csv` | Datos de Fasecolda. Precios en miles de pesos; `0` significa sin precio |
| `requirements.txt` | Librerías necesarias |

## Qué se hace en el notebook

1. Carga y revisión inicial de los datos (faltantes y ceros).
2. Análisis univariado: distribución del precio, valores atípicos, marcas más frecuentes.
3. Análisis bivariado: cilindraje vs. precio, precio y peso por marca, correlaciones.
4. Enriquecimiento de datos (SOAT, TRM e inflación, DANE).
5. Regresión (Random Forest) para predecir el precio.
6. Clustering (KMeans) para encontrar segmentos de vehículos.

## Cómo ejecutarlo

**En Google Colab:** abre el notebook desde GitHub (Colab → Archivo → Abrir cuaderno → pestaña GitHub). Cuando la primera celda pida un archivo, sube `guia_fasecolda.csv`.

**En local:**

```bash
pip install -r requirements.txt
jupyter notebook proyecto_fasecolda.ipynb
```

Deja `guia_fasecolda.csv` en la misma carpeta que el notebook.
