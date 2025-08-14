# **Product Backlog – NutriScan AI**

---

## **HU1 – Subida de texto nutricional**

**Historia de Usuario:**
Como usuario, quiero subir manualmente el texto con la información nutricional de un producto para que el sistema pueda analizarlo.

**Criterios de aceptación:**

* Formulario web que acepte texto plano.
* Validación de que el texto no esté vacío.
* Mensaje de error claro si el formato es inválido.

**Tareas técnicas:**

* Implementar formulario en Reflex.
* Validar entrada antes de enviarla a la API.
* Integrar validaciones en el frontend y backend.

---

## **HU2 – Subida de imagen con datos nutricionales**

**Historia de Usuario:**
Como usuario, quiero subir una foto del empaque con la información nutricional para que el sistema la lea automáticamente.

**Criterios de aceptación:**

* Soporta formato JPG y PNG.
* Si la imagen es ilegible, mostrar mensaje de advertencia.
* Procesar imagen con OCR (ej. Tesseract).

**Tareas técnicas:**

* Implementar carga de imágenes en Reflex.
* Integrar OCR para extracción de texto.
* Manejar errores por imágenes corruptas o muy grandes.

---

## **HU3 – Extracción estructurada de datos nutricionales**

**Historia de Usuario:**
Como usuario, quiero que el sistema extraiga y organice los datos nutricionales (calorías, carbohidratos, azúcares, etc.) para poder analizarlos.

**Criterios de aceptación:**

* Detecta y separa nutrientes con sus valores y unidades.
* Maneja diferentes formatos (tablas, listas, texto corrido).
* Valida que los datos sean coherentes.

**Tareas técnicas:**

* Implementar `NutritionParser`.
* Crear expresiones regulares para detectar valores.
* Pruebas unitarias con distintos formatos.

---

## **HU4 – Análisis con IA**

**Historia de Usuario:**
Como usuario, quiero que el sistema use IA para analizar los datos nutricionales junto con mi perfil de salud y determinar si es recomendable consumir el producto.

**Criterios de aceptación:**

* API de IA recibe datos estructurados y perfil de usuario.
* Devuelve evaluación (Apto / No apto).
* Considera tablas nutricionales estándar (ej. OMS).

**Tareas técnicas:**

* Integrar API de IA (Gemini o ChatGPT).
* Diseñar prompt estructurado.
* Implementar capa de conexión con manejo de errores.

---

## **HU5 – Generación de recomendación explicativa**

**Historia de Usuario:**
Como usuario, quiero que el sistema me explique en lenguaje sencillo por qué recomienda o no consumir el producto.

**Criterios de aceptación:**

* Texto claro y breve (máx. 150 palabras).
* Destacar nutrientes clave que motivan la decisión.
* Lenguaje comprensible para personas sin formación técnica.

**Tareas técnicas:**

* Procesar respuesta de IA y simplificar el lenguaje.
* Integrar módulo `Recommender`.
* Pruebas con ejemplos reales.

---

## **HU6 – Optimización para móviles**

**Historia de Usuario:**
Como usuario, quiero que la aplicación sea fácil de usar desde el móvil para poder analizar productos en el supermercado.

**Criterios de aceptación:**

* Diseño responsive.
* Botones grandes y formularios adaptados.
* Carga rápida en redes móviles.

**Tareas técnicas:**

* Aplicar estilos adaptativos en Reflex.
* Probar en navegadores móviles.
* Optimizar imágenes y scripts.

---

## **HU7 – Privacidad y seguridad de datos**

**Historia de Usuario:**
Como usuario, quiero que mis datos (texto o imágenes) no se almacenen permanentemente para proteger mi privacidad.

**Criterios de aceptación:**

* Borrar archivos e información tras el análisis.
* Política de privacidad visible.
* No registrar datos sensibles en logs.

**Tareas técnicas:**

* Implementar borrado automático en backend.
* Configurar logs para no almacenar datos del usuario.
* Pruebas de seguridad.

---

## **HU8 – Pruebas unitarias y de integración**

**Historia de Usuario:**
Como desarrollador, quiero contar con pruebas para garantizar que la extracción, análisis y recomendaciones funcionen correctamente.

**Criterios de aceptación:**

* Pruebas de OCR, parser, API y recomendación.
* Integración en CI/CD de GitHub Actions.
* Reportes de cobertura.

**Tareas técnicas:**

* Implementar pruebas con `pytest`.
* Configurar workflow en GitHub Actions.
* Dataset de ejemplos.

---

## **HU9 – Documentación inicial**

**Historia de Usuario:**
Como usuario, quiero una guía rápida para entender cómo usar NutriScan AI.

**Criterios de aceptación:**

* README con instrucciones y capturas.
* Ejemplos de entrada/salida.
* Explicación breve de cómo se procesan los datos.

**Tareas técnicas:**

* Escribir README.md.
* Crear carpeta `/examples`.
* Añadir imágenes demostrativas.

---

```
Título,Descripción,Etiqueta,Prioridad
HU1 – Subida de texto nutricional,"Como usuario, quiero subir manualmente el texto con la información nutricional de un producto para que el sistema pueda analizarlo.",Sprint 1,Alta
HU2 – Subida de imagen con datos nutricionales,"Como usuario, quiero subir una foto del empaque con la información nutricional para que el sistema la lea automáticamente.",Sprint 2,Alta
HU3 – Extracción estructurada de datos nutricionales,"Como usuario, quiero que el sistema extraiga y organice los datos nutricionales para poder analizarlos.",Sprint 1,Alta
HU4 – Análisis con IA,"Como usuario, quiero que el sistema use IA para analizar los datos y determinar si es recomendable consumir el producto.",Sprint 1,Alta
HU5 – Generación de recomendación explicativa,"Como usuario, quiero que el sistema me explique de forma sencilla la recomendación.",Sprint 1,Media
HU6 – Optimización para móviles,"Como usuario, quiero que la aplicación sea fácil de usar desde el móvil.",Sprint 3,Media
HU7 – Privacidad y seguridad de datos,"Como usuario, quiero que mis datos no se almacenen permanentemente.",Sprint 3,Alta
HU8 – Pruebas unitarias y de integración,"Como desarrollador, quiero contar con pruebas para garantizar que el sistema funciona correctamente.",Sprint 2,Alta
HU9 – Documentación inicial,"Como usuario, quiero una guía rápida para entender cómo usar NutriScan AI.",Sprint 1,Media
```

---

## **Historias Épicas**

### **E1 – Captura y análisis de datos**

Como usuario, quiero poder ingresar información nutricional desde texto o imagen y que el sistema la analice para darme una recomendación clara.

**Incluye:** HU1, HU2, HU3, HU4, HU5.

---

### **E2 – Experiencia de uso y seguridad**

Como usuario, quiero una interfaz optimizada para móviles y garantías de privacidad para usar la aplicación en cualquier lugar sin riesgo.

**Incluye:** HU6, HU7.

---

### **E3 – Calidad y documentación**

Como desarrollador y usuario, quiero que la aplicación tenga pruebas que aseguren su correcto funcionamiento y documentación clara para entender cómo usarla.

**Incluye:** HU8, HU9.
