# Parcial 3-He2AI
# Generador de Justificaciones de Gasto🚀

¡Bienvenido al repositorio de nuestro proyecto, en este, introduciras una partida de gasto público (ej. “700 mil millones para tren elevado”) y el modelo genera:
	•	Una justificación económica (costos-beneficio)
	•	Una narrativa política (generación de empleo, justicia territorial)
	•	Una crítica desde la oposición (“elefante blanco”, “gasto innecesario”)
	•	Útil para clases de economía pública o política.

---

## Tabla de Contenidos
- [Descripción del Proyecto](#descripción-del-proyecto)
- [Dataset Utilizado](#dataset-utilizado)
- [Modelos Implementados](#modelos-implementados)
- [Preprocesamiento de Datos](#preprocesamiento-de-datos)
- [Resultados](#resultados)
- [Ejecución del Código](#ejecución-del-código)
- [Limitaciones y Futuras Mejoras](#limitaciones-y-futuras-mejoras)

---

## Descripción del Proyecto 📈
**Problema:**   
**Objetivo:** 

**Aplicaciones prácticas:**
- 
- 
-  

---

## Modelos Implementados 🤖

1. **...**  
   - 
   - 
2. **...**  
   - 
   - 
3. **...**  
   

---

## Preproceso 🔧
Los pasos clave incluyeron:
1. **Limpieza de datos:**  
   - Imputación de valores faltantes mediante interpolación lineal, aplicada por Ticker para conservar la coherencia temporal.
   - Detección de valores atípicos utilizando una ventana móvil de 20 días y eliminación de aquellos que exceden 3 desviaciones estándar.
2. **Feature Engineering:**  
   - Creación de ventanas temporales: se generaron Close_denoised_lag_1 hasta Close_denoised_lag_40 (40 días históricos de precios).
   - Suavizado de los precios (Open y Close) usando una media móvil de 5 días para reducir el ruido.

---

## Resultados 📊



**Conclusión:** 


## Ejecución del Código 
1. **Requisitos:**  
  
   
2. **Pasos para ejecutar el código:**
   
 

   **2. Ejecutar el script principal:**


## Limitaciones y Futuras Mejoras 🔮
**Desafíos identificados:**

-
-
**Propuestas de mejora:**
-
-
