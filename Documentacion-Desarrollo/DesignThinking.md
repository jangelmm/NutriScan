# **Design Thinking aplicado a NutriScan**

## **1. Descubrimiento / Empatía / Investigación (Divergencia)**

**Contexto detectado**:

* Las personas con **diabetes** (y otras condiciones como hipertensión u obesidad) deben controlar su consumo de ciertos nutrientes como azúcar, sodio y grasas saturadas.
* El etiquetado nutricional, aunque obligatorio, suele ser **confuso, poco legible o con términos técnicos** que dificultan la decisión rápida en el supermercado.
* Aplicaciones existentes suelen estar enfocadas a contar calorías o dietas generales, pero **no siempre personalizan la recomendación según la condición médica del usuario**.
* Hay una oportunidad en **combinar IA con análisis nutricional estándar** para dar una respuesta directa: *"Apto"*, *"Con moderación"*, o *"No apto"*, con explicación clara.

**Necesidades de los usuarios**:

* Personas con diabetes o familiares que les ayudan en sus compras.
* Profesionales de la salud que quieren una herramienta rápida para evaluar productos.
* Usuarios que desean información clara sin leer párrafos técnicos.
* Comunidad interesada en etiquetado saludable y recomendaciones personalizadas.

**Hallazgos clave**:

* Necesidad de una **interfaz simple**: cámara → escaneo → respuesta.
* Posibilidad de ampliar a **otros perfiles de salud** (hipertensión, colesterol alto, alergias alimentarias).
* Integrar **porciones recomendadas** para casos en que el producto sea “consumible con moderación”.

---

## **2. Definición / Síntesis (Convergencia)**

**Problema a resolver**:
*"Las personas con diabetes no cuentan con una herramienta rápida, confiable y accesible que interprete el etiquetado nutricional de un producto y dé una recomendación clara sobre su consumo, adaptada a sus necesidades específicas."*

**Oportunidad de mercado**:

* Crear una aplicación que use **IA para interpretar y analizar datos nutricionales**.
* Posibilidad de integrar **OCR** para lectura de etiquetas y **motor de reglas** para decisiones basadas en estándares médicos.
* Extensión futura para perfiles personalizados (ej. personas con hipertensión).

---

## **3. Ideación (Divergencia y Convergencia)**

**Lluvia de ideas de funciones iniciales**:

* Escaneo de tabla nutricional desde foto (OCR).
* Análisis con IA (Gemini o ChatGPT API) para estructurar datos.
* Motor de reglas basado en estándares para diabetes.
* Respuesta en tiempo real con clasificación:

  * 🟢 **Apto**
  * 🟡 **Con moderación**
  * 🔴 **No apto**
* Explicación en lenguaje simple.
* Sugerencia de porciones recomendadas.
* Historial de productos escaneados.

**Selección para primera versión (MVP)**:

* Módulo de OCR → Procesamiento IA → Motor de decisión.
* Base de datos interna de umbrales recomendados para diabetes.
* Interfaz simple (app móvil o web).
* Historial básico.

---

## **4. Implementación / Construcción (Divergencia y Convergencia)**

**Primera iteración (v0.1)**:

* Integrar OCR para leer etiquetas.
* Procesar texto con API de IA (Gemini o ChatGPT).
* Motor de reglas en base a parámetros fijos para diabetes.
* Interfaz mínima para prueba (puede ser web responsiva).

**Pruebas y feedback**:

* Test con familiares y personas con diabetes.
* Ajuste de umbrales y mensajes.
* Validación con un nutriólogo.

**Iteraciones siguientes**:

* Perfiles para diferentes condiciones médicas.
* Recomendaciones de porciones.
* Escaneo offline con modelo IA ligero.
* Integración con base de datos pública de productos.

