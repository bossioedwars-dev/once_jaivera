# 🕵️‍♂️ Resumen Ejecutivo: El Arte de Elicitar y Análisis de Viabilidad

## 1. El Arte de Elicitar: Concepto y Mentalidad

### 📖 Definición
**Elicitar** significa *"sacar, extraer, hacer salir"*. En ingeniería de software, es el proceso **activo** de descubrir las necesidades reales de los clientes y usuarios para traducirlas en requerimientos formales. 
* ⚠️ **No es "recolectar":** El cliente rara vez sabe con exactitud lo que necesita. El analista no es un transcriptor pasivo, es un detective.

> 💡 *"Si hubiera preguntado a la gente qué quería, me habrían dicho: caballos más rápidos."* — Henry Ford. Los usuarios suelen describir soluciones basadas en lo que conocen, no el problema de raíz.

### 🛠️ Habilidades Blandas del Analista
* **Escucha activa:** Concentración total en el emisor, sin preparar la respuesta de antemano.
* **Curiosidad genuina:** Preguntar el porqué de las cosas de forma iterativa.
* **Saber callar:** Tolerar los silencios; a menudo preceden a las revelaciones más importantes.
* **Empatía:** Comprender la posición y frustraciones del cliente sin juzgar.
* **No asumir:** Evitar dar por sentado "lo obvio". Todo debe ser validado.

### ⚠️ El Problema del Iceberg
* **La Punta (Lo que dice):** *"Quiero una app rápida y bonita."*
* **El Medio (Lo que piensa pero no dice):** *"Mi competencia directa tiene una y me estoy quedando atrás."*
* **La Base (Lo que NO sabe que piensa):** Rutinas automatizadas, miedos al cambio tecnológico, procesos culturales implícitos.

---

## 2. 💬 La Técnica Reina: Entrevistas
Es una conversación guiada con un propósito claro. No es un interrogatorio ni un checklist.

### 🎨 Tipos de Entrevistas
* **Estructurada:** Lista cerrada de preguntas en orden fijo. Útil para comparar respuestas de grupos grandes. (Rígida).
* **No estructurada:** Conversación libre sin guion. Ideal en etapas muy tempranas para explorar el panorama. (Difícil de analizar).
* **Semi-estructurada:** Balance ideal. Cuenta con una guía de preguntas pero permite desviaciones si surge un dato de valor.

### 🕒 Las 3 Etapas Críticas
1.  **ANTES (Preparación):** Investigar al stakeholder, definir objetivos y estructurar de 5 a 10 preguntas guía.
2.  **DURANTE (Ejecución):** Romper el hielo, usar preguntas abiertas, repreguntar sobre las pausas, documentar o grabar (con autorización).
3.  **DESPUÉS (Consolidación):** Pasar notas a limpio en menos de 24 horas, extraer requerimientos y enviar correo de agradecimiento.

### ❓ Tipos de Preguntas
* **Abiertas:** Exploran contexto (*"¿Cómo es un día típico en su trabajo?"*).
* **Cerradas:** Confirman datos específicos (*"¿Cuántos empleados nocturnos hay?"*).
* **De sondeo:** Profundizan en respuestas previas (*"¿Me podría dar un ejemplo de ese fallo?"*).

---

## 3. 📊 Encuestas: Elicitación Masiva
Cuestionarios asincrónicos diseñados para recopilar información cuantitativa de grandes volúmenes de personas.

* **¿Cuándo usar?:** Grupos masivos (cientos/miles), usuarios dispersos, búsqueda de métricas/porcentajes o validación anónima de hipótesis.
* **¿Cuándo NO usar?:** Temas complejos que requieran explicación técnica o cuando se busca profundidad y matices.

### 📐 Reglas de Oro en el Diseño
1.  **Brevedad:** Máximo 10-15 preguntas para evitar el abandono.
2.  **Foco:** Una sola idea por pregunta (Evitar: *"¿Es rápido y fácil?"*).
3.  **Lenguaje neutro:** Cero jerga técnica (`API`, `JWT`, `Database`).
4.  **Escala Likert:** Herramienta estrella para medir actitudes de 1 a 5 (Muy en desacuerdo a Muy de acuerdo).

---

## 4. 👀 Observación: Descubrir lo Invisible
Consiste en acudir al entorno real de trabajo para registrar la ejecución de los procesos sin interrumpir el flujo. Revela los atajos, trucos y errores que el usuario omite en las entrevistas porque los considera "normales".

### 🎭 Variantes de Observación
* **Directa (Pasiva):** El analista actúa como una "mosca en la pared" sin intervenir.
* **Participante:** El analista se integra al equipo y ejecuta las tareas operativas para vivir los dolores del usuario.
* **Etnográfica / Shadowing:** Estudio prolongado y profundo del entorno o seguimiento estricto a un rol específico.

> ⚠️ **Efecto Hawthorne:** Fenómeno psicológico donde las personas modifican o mejoran su comportamiento habitual por el simple hecho de saber que están siendo observadas. Para mitigar esto, se recomienda extender las jornadas de observación hasta que la presencia del analista se vuelva cotidiana.

---

## 5. 🧩 Caso Práctico: "Biblioteca del Colegio" (Triangulación de Técnicas)

El éxito del levantamiento radica en alternar y complementar las herramientas según el volumen y criticidad de los actores:

* **Entrevistas (3 Bibliotecarios):** Revelan la saturación de los cuadernos físicos y el desconocimiento de la demanda de libros.
* **Observación (Hora Pico de Préstamos):** Permite medir que cada registro manual tarda de 4 a 5 minutos y que el 30% de los estudiantes desiste por las largas filas.
* **Encuestas (800 Estudiantes / 40 Profesores):** Cuantifican la necesidad (82% exige acceso móvil, 91% quiere catálogo online antes de asistir).

### 🔄 Traducción de Hallazgos a Requerimientos Formales
* *De Encuesta:* El **82%** quiere pedir desde el celular $\rightarrow$ **RF:** El sistema deberá permitir a los estudiantes solicitar préstamos desde una aplicación móvil.
* *De Observación:* El registro a mano toma **5 minutos** $\rightarrow$ **RNF:** El tiempo total de registro de un préstamo no deberá superar los 60 segundos.

---

## 6. ⚖️ Análisis de Viabilidad del Requerimiento
Filtro profesional y ético donde el analista evalúa si lo solicitado puede implementarse de manera realista en el mundo real.

### 📊 Las 5 Dimensiones Dimensionales
1.  **🛠️ Técnica:** ¿Existe la tecnología y el equipo cuenta con el conocimiento técnico para desarrollarlo?
2.  **💰 Económica:** ¿El presupuesto asignado cubre el costo de las herramientas, infraestructura y licencias?
3.  **👥 Operativa:** ¿La solución se adapta a la cultura organizacional y las capacidades del usuario final?
4.  **📜 Legal:** ¿El requerimiento infringe normativas de derechos de autor, accesibilidad o leyes de protección de datos personales?
5.  **⏱️ Temporal:** ¿El cronograma propuesto es realista para el nivel de complejidad del software?