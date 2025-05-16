# Parcial 3-He2AI
# Generador de Justificaciones de Gasto🚀

¡Bienvenido al repositorio de nuestro proyecto, en este, introduciras una partida de gasto público (ej. “700 mil millones para tren elevado”) y el modelo genera:

•Una justificación económica (costos-beneficio)

•Una narrativa política (generación de empleo, justicia territorial)

•Una crítica desde la oposición (“elefante blanco”, “gasto innecesario”)

•Útil para clases de economía pública o política

---
## Tabla de Contenidos
- [Autores](#autores)
- [Descripción](#descripción)
- [Planteamiento del modelo](#planteamiento-del-modelo)
- [Contenido del repositorio](#contenido-del-repositorio)
- [Modelos implementados](#modelos-implementados)
- [Evaluación de Modelos](#evaluación-de-modelos)
- [Requerimientos](#requerimientos)
- [Licencia](#licencia)
- [Propuestas de mejora](#propuesta-de-mejora)

---
## Autores

[*Juan Diego Barrios Esteban*](https://www.linkedin.com/in/juandiegobarriosesteban)
Estudiante de economía Universidad de los Andes 

[*Marcelo Yepes*](https://www.linkedin.com/in/marceloyepesa)
Estudiante de economía Universidad de Los Andes

[*Loek Kleyn*]()
Estudiante de economía Universidad de Los Andes

[*David sandino*]()
Estudiante de economía Universidad de Los Andes

---
## Descripción

Este proyecto tiene como objetivo entrenar un modelo de lenguaje adaptado para generar automáticamente justificaciones estructuradas ante partidas de gasto público. Al recibir como entrada una cifra presupuestaria y su destino (por ejemplo, “700 mil millones para tren elevado en la costa Caribe”), el modelo devuelve tres secciones de texto:

ECONOMÍA: Justificación desde el impacto económico.
POLÍTICA: Argumento narrativo desde la postura del gobierno o actores afines.
CRÍTICA: Observación, objeción o contraargumento desde la oposición.

Este tipo de generación puede usarse en clases de economía pública, debates fiscales, talleres de argumentación o como insumo en simuladores de política pública.

---
## Planteamiento del Problema

Modelo base: microsoft/phi-2, un modelo de lenguaje causal preentrenado.
Adaptación: LoRA (Low-Rank Adaptation) para ajuste fino eficiente.
Tipo de fine-tuning: Entrenamiento causal con etiquetas construidas a partir de un prompt instructivo.
Formato del prompt: Tipo instructivo con secciones fijas, iniciando con "<s>" y terminando con "</s>".
Ejemplo de prompt:
<s>Genera una justificación para la siguiente partida de gasto:

700 mil millones para tren elevado en la costa Caribe

---
## Contenido del Repositorio
	
 •	main.ipynb – Cuaderno principal con la implementación de modelos y análisis de resultados.
	
 •	README.md – Este archivo con la descripción del proyecto
 
---
## Modelos Implementados

Modelo base: microsoft/phi-2
2.8B parámetros
Tokenización tipo causal

Adaptación LoRA:
R = 16, alpha = 32

Target modules: proyecciones y capas lineales internas

Cuantización:
8-bit NF4 con bitsandbytes para reducir uso de memoria

---
## Evaluación de Modelos

Dado el carácter instructivo y bajo volumen de datos (~30 ejemplos), se evaluó la calidad de las salidas de forma cualitativa:
Las salidas fueron gramaticales, temáticamente relevantes y estructuradas.
El modelo aprendió a completar las secciones “ECONOMÍA / POLÍTICA / CRÍTICA” en forma coherente.
Se evidencian variaciones y creatividad, pero sin alejarse del dominio semántico del gasto público.
(Para evaluación cuantitativa, puede usarse ROUGE, BLEU o evaluación humana posterior.)

---
## Requerimientos
Google Colab (GPU)
Python ≥ 3.10

Paquetes:
pip install transformers peft datasets gradio bitsandbytes accelerate
Opcional: Guardar el modelo en Hugging Face Hub o montar localmente en HuggingFace Spaces.

---
## Licencia

Este proyecto puede ser licenciado bajo MIT 

---
**Propuestas de mejora**

 •	Ampliar el dataset con +200 ejemplos con mayor diversidad semántica y geográfica.
 •	Ajustar hiperparámetros de LoRA y aumentar épocas si se entrena con más datos.
 •	Añadir validación humana o por expertos para evaluar factualidad.
 •	Implementar interface en español neutro y/o lenguas indígenas.
 •	Conectar con bases reales de presupuestos públicos para generar argumentos contextuales.
