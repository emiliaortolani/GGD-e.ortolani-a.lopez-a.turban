
# Proyecto: Predicción de Churn

Este proyecto tiene como objetivo preparar los datos de clientes, analizarlos y entrenar modelos de Machine Learning para predecir churn (si un cliente deja de comprar).  
El trabajo se divide en tres notebooks principales: limpieza, modelado y registro de experimentos.

---

## Estructura del proyecto

- **DATA/** → Archivo original (`client_full.csv`)
- **notebooks/**
  - `limpieza.ipynb` → limpieza del dataset y creación de variables
  - `modelado.ipynb` → entrenamiento y comparación de modelos
  - `mlflow.ipynb` → registro de modelos y métricas con MLflow
- **models/** → modelos guardados
- **mlruns/** → carpeta generada automáticamente por MLflow
- `requirements.txt`

---

## Resumen del proceso

### 1. Limpieza de datos  
En esta parte se:
- corrigen tipos de datos  
- manejan valores faltantes  
- generan variables nuevas  
- codifican las columnas categóricas  

### 2. Modelado  
Se entrenaron varios modelos para comparar rendimiento:
- Logistic Regression  
- Decision Tree  
- Random Forest  
- Gradient Boosting  

Las métricas utilizadas fueron **AUC**, **F1** y **accuracy**.  
Random Forest y Gradient Boosting fueron los que mejor funcionaron en general.

### 3. MLflow  
MLflow se utilizó para:
- registrar parámetros  
- guardar las métricas  
- comparar runs  
- almacenar los modelos  

Para abrir MLflow:
```bash
mlflow ui
````

Luego entrar a: [http://127.0.0.1:5000](http://127.0.0.1:5000)

---

## Requisitos

Instalar dependencias:

```bash
pip install -r requirements.txt
```

---

## Notas

El proyecto fue realizado para la materia de Gobierno y Gestión de Datos, siguiendo el flujo completo desde la limpieza hasta la comparación de modelos.

