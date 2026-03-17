# Documentación técnica de mi tarjeta personal

## Decisiones semánticas

- **`<!DOCTYPE html>`**: se usa para indicar que el archivo está en HTML5.
- **`<html lang="es">`**: se usa para indicar que la página está en español.
- **`<head>`**: contiene la información importante del documento, como el título y los metadatos.
- **`<meta charset="UTF-8">`**: permite que se vean bien las tildes y la ñ.
- **`<meta name="viewport">`**: ayuda a que la página se vea bien en celular y computadora.
- **`<header>`**: lo usé para poner mi nombre y mi frase.
- **`<main>`**: contiene el contenido principal de la página.
- **`<section>`**: lo usé para separar la información en partes, como “Sobre mí” y “Habilidades y pasatiempos”.
- **`<h1>`**: es el título principal con mi nombre.
- **`<h2>`**: son los títulos de cada sección.
- **`<p>`**: se usa para escribir los textos.
- **`<time>`**: lo usé para mostrar mi cumpleaños de forma semántica.
- **`<strong>`**: lo usé para resaltar información importante.
- **`<em>`**: lo usé para dar énfasis a una palabra importante.
- **`<footer>`**: lo usé para la parte final de la página.
- **`<address>`**: lo usé para mostrar mi información de contacto.
- **`<a>`**: lo usé para que el correo se pueda abrir al hacer clic.

## Árbol DOM (visual)

```text
html
├── head
│   ├── meta
│   ├── meta
│   └── title
└── body
    ├── header
    │   ├── h1
    │   └── p
    ├── main
    │   ├── section
    │   │   ├── h2
    │   │   ├── p
    │   │   └── time
    │   └── section
    │       ├── h2
    │       ├── p
    │       ├── strong
    │       └── em
    └── footer
        └── address