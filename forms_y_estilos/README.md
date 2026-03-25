# 📝 Explicación: Flow bosque 🏕

En este trabajo lo que hice fue cambiar ese color muerto que habia por uno bien coolero que llena de vida ese formulario:

### 1. Cambio de "Color" 
* **Color:** Edite la variable `--primario` en el archivo CSS. Cambie el azul por un **verde bosque** (`#37cf58`). Ahora, todos los botones y bordes resaltados usan este nuevo tono automáticamente.
* **Redondeo:** Subi el valor de `--radio` de 8px a **20px**. Esto hace que los botones y las cajas de texto se vean mucho más circulares y amigables.

### 2. El Nuevo Campo de "Edad"
* En el HTML, justo antes del mensaje, cree un nuevo `div` con la clase `.campo`.
* Use un `<label>` para el título y un `<input>`.
* **Restricciones:** Le pusimos `type="number"`, `min="15"` y `max="99"`. Esto lo hice porque el navegador no dejará que nadie mienta o ponga números locos; el formulario se "protege" solo.

### 3. El Botón con Superpoderes
* En el CSS, busque la clase `.btn-primario`. 
* Modifice el `box-shadow` para que tenga una sombra negra muy densa. 
* Al pasar el mouse (`:hover`), la sombra crece muchísimo, dando la sensación de que el botón tiene una gravedad brutal y se separa de la pantalla.
