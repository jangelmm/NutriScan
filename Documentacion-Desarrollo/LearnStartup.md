# **Lean Startup aplicado a NutriScan** 

## **1. Hipótesis**

* **Hipótesis de problema**:
  Personas con diabetes y sus familiares necesitan una herramienta sencilla que interprete el etiquetado nutricional y brinde recomendaciones claras sobre si un producto es apto para su consumo, ya que las tablas de valor nutrimental suelen ser confusas o poco legibles.

* **Hipótesis de solución**:
  Una aplicación que use **OCR** para leer etiquetas, **IA** para procesar la información y un **motor de reglas nutricionales** para dar una recomendación rápida (“Apto”, “Con moderación” o “No apto”) será adoptada por personas con diabetes y cuidadores, siempre que sea fácil de usar y explique el porqué de la recomendación.

---

## **2. Producto Mínimo Viable (MVP)**

* **Funcionalidad mínima**:

  1. Capturar imagen de la tabla nutrimental (foto o subida desde galería).
  2. Procesar imagen con OCR para extraer texto.
  3. Analizar texto con API de IA (Gemini o ChatGPT) para estructurar datos.
  4. Evaluar nutrientes contra tabla estándar para diabetes.
  5. Mostrar recomendación con explicación simple.

* **Experiencia mínima**:

  * Interfaz simple tipo:

    ```
    [📸 Escanear etiqueta] → Resultado: "Con moderación"  
    Razón: Azúcar por porción excede 15 g.
    Porción recomendada: 1/2 paquete.
    ```
  * Respuesta rápida (<3 segundos).
  * Opción de guardar historial del producto.

---

## **3. Métricas de Éxito (MVP)**

* **Cuantitativas**:

  * Número de descargas o usuarios registrados.
  * Cantidad de productos escaneados por día.
  * Tiempo promedio entre apertura de app y entrega de resultado.
  * Porcentaje de usuarios recurrentes.

* **Cualitativas**:

  * Feedback de familiares y personas con diabetes sobre claridad y utilidad.
  * Opiniones de nutriólogos sobre precisión del análisis.
  * Solicitudes para ampliar a otros perfiles de salud (hipertensión, colesterol).

---

## **4. Ciclo de Validación**

1. **Construir** → Crear versión mínima con OCR + IA + motor de reglas básico para diabetes.
2. **Medir** → Probar con familiares, grupos de apoyo para diabetes y profesionales de la salud.
3. **Aprender** → Ajustar umbrales nutricionales, interfaz y mensajes según feedback real.

