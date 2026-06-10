# 📜 Resumen Ejecutivo: Documentación, Estándar IEEE 830 y Casos de Uso

## 1. ¿Por qué Documentar? Poner por Escrito como Escudo Profesional

### 🧠 Mente vs. Papel
* **La trampa del analista junior:** Pensar que tener la información en la cabeza es suficiente.
* **La realidad:** La memoria olvida detalles en días, los datos no se pueden auditar, cambian con el estado de ánimo y la información se pierde si el analista se enferma o renuncia.
* **El valor del papel:** Permanece inalterable, es accesible para todo el equipo, sobrevive a la rotación de personal y sirve como **evidencia legal**.

### 💸 Consecuencias Reales de NO Documentar
1.  **Fuga de Conocimiento:** La renuncia del único desarrollador que "sabía todo" puede costar millones en consultorías externas para descifrar código antiguo.
2.  **"Eso no fue lo que dije":** Sin un documento firmado, el cliente puede rechazar el software final. Resultado: meses de retrabajo gratis.
3.  **Vacío Legal ante Auditorías:** Incapacidad de demostrar ante entes reguladores que el software cumple con las leyes vigentes, derivando en multas severas.

### 🎯 Las 5 Funciones de la Documentación
* **Acuerdo:** Contrato formal entre el cliente y el equipo sobre qué se va a construir.
* **Guía:** Hoja de ruta clara para los desarrolladores (evita que tengan que adivinar).
* **Verificación:** Base técnica para que los *testers* validen el producto.
* **Conocimiento:** Memoria histórica que sobrevive a las personas en el proyecto.
* **Legal:** Evidencia ante disputas, demandas o auditorías externas.

> 📊 **Regla de oro de la cantidad:** A mayor riesgo del proyecto, mayor exhaustividad en la documentación. (Desde historias de usuario en Trello para Startups, hasta un IEEE 830 estricto y trazable para banca o software médico).

---

## 2. 📘 El Estándar IEEE 830 (Especificación de Requerimientos - SRS)

El **IEEE 830** es una práctica recomendada internacional para la creación de la **Especificación de Requerimientos de Software (SRS)**. Es el idioma universal de los ingenieros de software.

### 🏗️ Estructura Esencial del SRS
1.  **Introducción:** Propósito, alcance del producto, definiciones, acrónimos y referencias legales/técnicas.
2.  **Descripción General:** Perspectiva del producto, funciones principales, características de los usuarios, restricciones del proyecto (presupuesto, plazos) y suposiciones.
3.  **Requisitos Específicos:** El núcleo técnico. Detalle exhaustivo de los Requerimientos Funcionales (RF), No Funcionales (RNF), interfaces externas y modelos/diagramas de comportamiento.
4.  **Apéndices:** Glosarios extendidos, bocetos de pantallas (mockups) y tablas de trazabilidad.

### ✨ Las 8 Cualidades de un SRS Profesional
* **Correcto:** Cada requerimiento responde a una necesidad real y verídica.
* **No ambiguo:** Existe una única interpretación posible por frase.
* **Completo:** No contiene secciones vacías o notas pendientes (`TODO`).
* **Consistente:** No presenta requerimientos que se contradigan entre sí.
* **Clasificado:** Prioridades de desarrollo claramente definidas (Alta, Media, Baja).
* **Verificable:** Cada línea se puede probar mediante un test métrico.
* **Modificable:** Su estructura permite cambios puntuales sin romper el documento.
* **Trazable:** Cada requerimiento posee un ID único para rastrear su origen y código asociado.

---

## 3. 🎭 Casos de Uso (CU): Contar Historias Técnicas

Un **Caso de Uso** es una descripción narrativa de cómo un actor interactúa con el sistema para lograr un objetivo específico. Es una guía paso a paso del comportamiento del software.

### 🎬 Diferencia Clave
* **Requerimiento (Qué):** *"El sistema deberá permitir al usuario iniciar sesión."* (Una sola frase declarativa).
* **Caso de Uso (Cómo):** *"1. El usuario digita el correo. 2. El sistema valida... 3. El sistema muestra..."* (Una secuencia narrativa completa).

### 🧩 Componentes del Bloque de Construcción
* **Actor:** Entidad externa (humana o sistema) que interactúa con el software.
* **Sistema:** Las fronteras del software que reacciona ante las acciones del actor.
* **Objetivo:** La meta final del actor (ej: "Reservar un libro").
* **Escenario:** Secuencia exacta de pasos que ocurren para alcanzar el objetivo.



### 🔗 Relaciones Especiales en UML
* `‹‹include››` (Incluye): El caso de uso base **siempre** requiere del flujo de otro para completarse. *(Ej: "Reservar libro" incluye obligatoriamente "Iniciar sesión")*.
* `‹‹extend››` (Extiende): El caso de uso base **puede** activar un comportamiento opcional bajo una condición específica. *(Ej: "Reservar libro" se extiende a "Pagar multa" solo si el usuario tiene deudas)*.

---

## 4. 📋 Plantilla Profesional de un Caso de Uso (CU)

Un caso de uso estándar de la industria se compone de las siguientes secciones clave:

| Campo | Descripción | Ejemplo |
| :--- | :--- | :--- |
| **ID** | Código de identificación único | `CU-001` |
| **Nombre** | Verbo + Objeto | `Reservar libro` |
| **Actor Principal** | Quién inicia la acción | `Estudiante` |
| **Descripción** | Resumen corto del objetivo | El estudiante aparta un libro para su retiro presencial. |
| **Precondiciones** | Requisitos obligatorios *antes* de empezar | El usuario está autenticado; No posee multas vigentes. |
| **Postcondiciones** | Estado final del sistema *después* del éxito | El libro cambia a estado "Reservado"; Expira en 72 horas. |
| **Flujo Principal** | Secuencia de pasos numerados del camino feliz | 1. Actor busca libro. 2. Sistema valida disponibilidad... |
| **Flujos Alternos** | Caminos secundarios válidos | El actor busca el libro por Autor en lugar de Título. |
| **Excepciones** | Manejo de errores cuando algo falla | Si el libro está agotado, el sistema ofrece lista de espera. |
| **Reglas de Negocio**| Restricciones lógicas institucionales | Un estudiante puede reservar un máximo de 3 libros a la vez. |
| **Frecuencia / Prioridad**| Uso estimado y orden de desarrollo | Frecuencia: Alta (~50 al día) / Prioridad: Alta. |

---

## 5. 🔎 Revisión Cruzada: El Control de Calidad del Analista

La **revisión cruzada** consiste en someter el documento SRS al escrutinio de otros analistas para detectar errores antes de que lleguen a la fase de desarrollo.

### 🚫 Errores Típicos a Detectar (Casos de Falla)
* **Ambigüedades:** Palabras vacías como *"rápido"*, *"seguro"*, *"bonito"*, o *"amigable"*. (Deben cambiarse por métricas).
* **Falta de Atomicidad:** Mezclar tres funciones en un solo ID. *(Ej: "El sistema permitirá cancelar, hacer reportes y enviar SMS").* Debe dividirse en tres requerimientos independientes.
* **Contradicciones Internas:** Declarar que *"todos los datos son públicos"* pero luego exigir que *"los datos estén ocultos"*.
* **Jerga Técnica Innecesaria en RF:** Incluir código de API, métodos HTTP (`GET`, `POST`) o tokens (`JWT`) dentro de requerimientos funcionales que el cliente debe firmar. Esas especificaciones pertenecen exclusivamente al diseño técnico.