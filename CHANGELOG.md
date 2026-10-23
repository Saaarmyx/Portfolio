# Changelog

Todos los cambios relevantes de Portfolio se anotan aquí.

El formato sigue [Keep a Changelog 1.1.0](https://keepachangelog.com/es-ES/1.1.0/) y el proyecto usa [Versionado Semántico](https://semver.org/lang/es/).

## [Sin publicar]

La versión declarada en `package.json` es `0.0.1`. El repositorio no tiene tags.

### Añadido

- Póster editorial responsive en `index.html`, con tipografías Oswald, Caveat y Montserrat.
- Menú superior, retrato central, bloque de redes y pie de página.
- Proyecto SvelteKit 3 con Svelte 5 en modo runes.
- TypeScript estricto mediante `jsconfig.json` y alias `#lib`.
- Prettier con `prettier-plugin-svelte` y `.prettierignore`.
- Scripts `dev`, `build`, `preview`, `check`, `check:watch`, `lint` y `format`.
- Assets base en `static/`: favicon, imágenes y logotipo.

### Cambiado

- La página principal de SvelteKit quedó como esqueleto con navegación y el título `SAAARMYX`.
- El favicon del layout se importa desde `static/`.

### Corregido

- `svelte-check` pasa con 0 errores; quedan advertencias de selectores CSS no usados en la página principal.

[Sin publicar]: https://github.com/Saaarmyx/PortfolioS/commits/main

<!-- TODO: añadir enlaces de comparación entre versiones cuando el repositorio tenga tags. -->
