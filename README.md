# telecom-analysis

# 📊 ConnectaTel – Análisis de Uso de Clientes

## 🎯 Objetivo del Proyecto

El objetivo de este proyecto es analizar el comportamiento de los clientes de ConnectaTel (empresa de telecomunicaciones en Latinoamérica) para identificar patrones de uso en llamadas y mensajes, detectar valores atípicos (outliers) y segmentar a los usuarios según su nivel de consumo.

Este análisis permite generar **insights accionables** para optimizar la oferta comercial, mejorar la experiencia del cliente y apoyar la toma de decisiones estratégicas.

---

## 📂 Datasets Utilizados

Se trabajó con tres fuentes principales:

* **plans.csv**
  Contiene información de los planes disponibles:

  * precio
  * minutos incluidos
  * datos incluidos
  * costos adicionales

* **users_latam.csv**
  Información de los clientes:

  * edad
  * ciudad
  * fecha de registro
  * tipo de plan

* **usage.csv**
  Registro de uso del servicio:

  * tipo de evento (llamada o mensaje)
  * duración de llamadas
  * longitud de mensajes
  * fecha de actividad

---

## 🔄 Etapas del Análisis

El proyecto se desarrolló siguiendo un flujo estructurado:

### 1. Exploración de datos

* Revisión de estructura (`.head()`, `.info()`, `.shape`)
* Identificación de tipos de datos y granularidad

### 2. Calidad de datos

* Detección de valores nulos
* Identificación de sentinels (ej. `-999`, `"?"`)
* Validación de fechas fuera de rango

### 3. Limpieza de datos

* Reemplazo de sentinels
* Conversión de tipos de datos (fechas)
* Tratamiento de valores inválidos
* Manejo de datos no aplicables (MAR)

### 4. Transformación y agregación

* Creación de métricas por usuario:

  * número de llamadas
  * número de mensajes
  * minutos totales
* Integración de datasets (`merge`)

### 5. Análisis exploratorio (EDA)

* Estadísticas descriptivas
* Visualización de distribuciones
* Comparación por tipo de plan

### 6. Detección de outliers

* Uso de boxplots
* Método IQR
* Interpretación de heavy users

### 7. Segmentación de clientes

* Por nivel de uso (bajo, medio, alto)
* Por edad (joven, adulto, adulto mayor)

### 8. Insights de negocio

* Identificación de segmentos clave
* Detección de patrones de consumo
* Recomendaciones estratégicas

---

## ▶️ Cómo ejecutar el proyecto

### Opción 1: GitHub (visualización rápida)

1. Abre el repositorio en GitHub
2. Haz clic en el archivo `.ipynb`
3. GitHub mostrará el notebook renderizado

---

### Opción 2: Ejecución local

1. Clona el repositorio:

```bash
git clone <URL_DEL_REPOSITORIO>
```

2. Instala dependencias:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

3. Ejecuta Jupyter Notebook:

```bash
jupyter notebook
```

4. Abre el archivo `.ipynb` y ejecuta las celdas

---

## 🔁 Guía de reproducción

Para reproducir el análisis:

1. Asegúrate de tener los datasets en la carpeta `/datasets`
2. Ejecuta el notebook en orden (de arriba hacia abajo)
3. Verifica:

   * limpieza de datos
   * creación de variables
   * agregación por usuario
4. Ejecuta secciones de visualización y segmentación
5. Revisa el bloque final de **insights ejecutivos**

---

## 💡 Insights Clave

* El uso está **altamente concentrado** en un pequeño grupo de usuarios (heavy users)
* Existen segmentos claramente diferenciados por nivel de consumo
* Los planes actuales pueden no estar alineados con el comportamiento real

---

## 🚀 Recomendaciones

* Diseñar planes diferenciados por nivel de uso
* Implementar estrategias de upselling
* Identificar y retener usuarios de alto valor
* Activar usuarios de bajo consumo

---

## 👤 Autor

Proyecto desarrollado como parte de un ejercicio de análisis de datos enfocado en **Data Analytics con Python y enfoque de negocio (Lean mindset)**.

---
