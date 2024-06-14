# Crear un componente en Tailwind

en el archivo index.css agregamos la siguiente configuracion

```css
@tailwind base;
@tailwind components;
@tailwind utilities;


@layer components {
    .contenedor{
        @apply w-[90%] sm:w-[80%] mx-auto max-w-screen-xl;
    }
    .my-button {
        @apply bg-icd-pink text-icd-pink-suave rounded-full;
    }
}
```