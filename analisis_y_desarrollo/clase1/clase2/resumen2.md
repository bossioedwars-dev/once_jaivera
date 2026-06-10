# 🧠 Resumen Ejecutivo: Ingeniería de Requerimientos y Caso "SchoolEats"

## 1. Profundización del Concepto

### 📜 Definición Formal (IEEE 830)
Un **requerimiento** es una propiedad documentada que un sistema debe poseer para resolver un problema o lograr un objetivo. Es una declaración **verificable** de una funcionalidad, restricción o característica de calidad.
* **Clave:** Si no es *documentable* y *verificable*, NO es un requerimiento.

### 🪜 Niveles de Abstracción
1.  **Necesidad del Usuario (Piso 1 - Informal/Emocional):** *"Quiero saber qué hay de comida para no perder el viaje a la cafetería."*
2.  **Requerimiento del Sistema (Piso 2 - Formal/Traducido):** *"El sistema debe mostrar el menú del día actualizado a todos los estudiantes autenticados."*
3.  **Especificación Técnica (Piso 3 - Detalle Técnico):** *"La API `/menu/dia` debe retornar un JSON con los platos del día, en menos de 300 ms, usando HTTPS."*

### 🌐 Fuentes de Requerimientos (Stakeholders)
* **Usuarios finales:** Detalle operativo del día a día (estudiantes, cocineros).
* **Clientes / Patrocinadores:** Objetivos de negocio y presupuesto (rector, administración).
* **Leyes y normas:** Regulaciones obligatorias (protección de datos, accesibilidad).
* **Sistemas externos:** Integraciones requeridas (bancos, pasarelas de pago).

### ✅ Las 7 Cualidades de un Buen Requerimiento
* **Necesario:** Esencial para el propósito del sistema.
* **No ambiguo:** Una sola interpretación posible.
* **Verificable:** Se puede probar su cumplimiento.
* **Consistente:** No contradice a otros requerimientos.
* **Completo:** Contiene toda la información necesaria.
* **Atómico:** Describe una sola idea o función.
* **Trazable:** Se conoce su origen y su impacto.

---

## 2. 🔧 Requerimientos Funcionales (RF)
Definen **QUÉ hace** el sistema (acciones, tareas, cálculos y respuestas).

* **Identificación:** Verbos de acción (*registrar, calcular, mostrar, validar*), flujos de entrada/salida y roles de usuario.
* **Plantilla Estándar:** `El sistema [deberá] + [acción/verbo] + [objeto] + [condiciones/restricciones]`.

### 🗂️ Categorías de RF
* **Autenticación:** Gestión de accesos y seguridad (Login con correo y contraseña).
* **Cálculo:** Operaciones matemáticas (Calcular promedio aritmético con 2 decimales).
* **Persistencia (CRUD):** Almacenamiento de datos (Guardar historial de pedidos por 6 meses).
* **Comunicación:** Notificaciones y alertas (Enviar SMS cuando el pedido esté listo).
* **Reporte:** Exportación de información (Generar reporte mensual en PDF y Excel).
* **Validación:** Reglas del negocio (Rechazar contraseñas de menos de 8 caracteres).

---

## 3. ⚙️ Requerimientos No Funcionales (RNF)
Definen **CÓMO es** o **CON QUÉ CALIDAD** se comporta el sistema. Un RNF sin métrica es solo un deseo.

### 🎚️ Categorías Principales de RNF
* **⚡ Rendimiento:** Tiempos de respuesta (ej: responder consultas en < 2 segundos).
* **🔒 Seguridad:** Cifrado y protección (ej: contraseñas cifradas con `bcrypt` factor 12).
* **👍 Usabilidad:** Facilidad de uso (ej: completar un pedido en menos de 3 minutos sin tutorial).
* **🛡️ Confiabilidad:** Disponibilidad ante fallos (ej: disponibilidad del 99.5% en horario escolar).
* **📈 Escalabilidad:** Carga concurrente (ej: soportar 5,000 usuarios concurrentes).
* **🔧 Mantenibilidad:** Facilidad de mejora (ej: cobertura de pruebas unitarias mínima del 80%).
* **📱 Portabilidad/Compatibilidad:** Multiplataforma (ej: funcionar en Chrome, Firefox, Safari y Edge).
* **📜 Legales/Regulatorios:** Cumplimiento legal (ej: cumplir con la Ley de protección de datos personales).

⚠️ **Trade-offs comunes:** Más Seguridad = Menor Usabilidad; Mayor Escalabilidad = Mayor Costo de Infraestructura.

---

## 4. 💎 Atributos de Calidad (Norma ISO/IEC 25010)
Son los conceptos abstractos generales que luego se materializan de forma medible en los RNF.

1.  **Adecuación funcional:** Completitud y corrección de las funciones.
2.  **Eficiencia de desempeño:** Velocidad y uso óptimo de recursos.
3.  **Compatibilidad:** Capacidad de interactuar con otros sistemas (Interoperabilidad).
4.  **Usabilidad:** Facilidad de aprendizaje, accesibilidad y operabilidad.
5.  **Confiabilidad:** Tolerancia a fallos, madurez y recuperabilidad.
6.  **Seguridad:** Confidencialidad, integridad y autenticidad de los datos.
7.  **Mantenibilidad:** Modularidad, reusabilidad y facilidad de prueba.
8.  **Portabilidad:** Adaptabilidad e instalabilidad en diferentes entornos.

---

## 5. 🧩 Caso de Estudio: "SchoolEats" (Cafetería Colegio San Antonio)

### 👤 Stakeholders Clave
1. Estudiantes, 2. Cocineros/Cafetería, 3. Rector/Administración, 4. Padres de familia.

### 🗺️ Técnicas de Elicitación a aplicar
* **Encuestas digitales:** Para grupos grandes (Estudiantes y Padres).
* **Observación en sitio + Entrevistas:** Para procesos operativos en la cocina (Cocineros).
* **Entrevista estructurada:** Para el tomador de decisiones clave (Rector).

### 📋 Mapeo de Requerimientos (RF vs RNF)
* **RF:** Mostrar menú del día, Reservar y pagar platos con saldo digital, Generar reportes mensuales de ventas en PDF.
* **RNF:** Disponibilidad del 99.5% en horario escolar, Compatibilidad multiplataforma (iOS/Android/Web), Tiempo de respuesta inferior a 2 segundos.
* **Atributos de Calidad Críticos para la app:** **Confiabilidad** (no puede caerse al almuerzo), **Usabilidad** (debe ser rápido y fácil de usar) y **Seguridad** (gestión de dinero y saldo).

---

## 6. 🏃 Historias de Usuario (Enfoque Ágil)
Descripción corta centrada en el valor que el usuario recibe.

### 📐 Estructura Ágil
* **Como** `[tipo de usuario]`
* **Quiero** `[acción / funcionalidad]`
* **Para** `[beneficio / objetivo]`

### ⭐ Criterio de Calidad: INVEST
**I**ndependiente, **N**egociable, **V**aliosa, **E**stimable, **S**mall (Pequeña), **T**estable (Testeable).

### 📋 Ejemplo con Criterios de Aceptación (Given/When/Then)
**Historia:** Como estudiante, quiero ver el menú del día en mi celular para decidir qué comer.
* **Criterio 1:** **Dado** que soy un estudiante autenticado, **cuando** abro la app, **entonces** veo el menú del día con foto, nombre y precio de cada plato.
* **Criterio 2:** **Dado** que un plato está agotado, **cuando** se muestra el menú, **entonces** aparece como "AGOTADO" y se bloquea su selección.
* **Criterio 3:** **Dado** que no hay internet, **cuando** abro la app, **entonces** veo el último menú guardado con un aviso de "sin conexión".