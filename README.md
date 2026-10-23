<div align="center">

# Portfolio

Mi portafolio personal: un póster editorial y una base en SvelteKit para seguir construyéndolo.

[![Licencia](https://img.shields.io/badge/Licencia-MIT-8B5CF6)](LICENSE)
![Estado](https://img.shields.io/badge/Estado-En%20desarrollo-F59E0B)
![Versión](https://img.shields.io/badge/Versión-0.0.1-8B5CF6)
![Svelte](https://img.shields.io/badge/Svelte-5-FF3E00?logo=svelte&logoColor=white)
![SvelteKit](https://img.shields.io/badge/SvelteKit-3-FF3E00?logo=sveltekit&logoColor=white)

</div>

## Estado del proyecto

**En desarrollo.** La base de SvelteKit funciona y el póster está maquetado, pero las secciones de contenido todavía son un esqueleto. `check` y `build` pasan; `lint` todavía marca el formato de `index.html`. Faltan los textos, los proyectos y el despliegue.

## Descripción

Portfolio es mi tarjeta de presentación técnica. La idea es tener un sitio rápido, sin ruido y fácil de mantener, donde quepan quién soy, qué hago, algunos proyectos y cómo contactarme.

El repositorio tiene dos piezas: un `index.html` autónomo con el diseño de póster (tipografías, retrato y redes) y una aplicación SvelteKit 3 con Svelte 5 en modo runes, que es la base sobre la que quiero construir el sitio final.

## Características principales

- Póster editorial responsive con tipografías Oswald, Caveat y Montserrat.
- Menú superior, retrato central y bloque de redes sociales.
- Aplicación SvelteKit con Svelte 5 en modo runes.
- TypeScript estricto mediante `jsconfig.json`.
- Prettier con `prettier-plugin-svelte` para `.svelte`.
- `svelte-check` para tipos y plantillas.
- Build estático listo para cualquier hosting.
- Assets en `static/` (favicon, imágenes y logotipo).

## Requisitos

- Node.js ≥ 20.19 (requisito de Vite 8).
- npm.

## Instalación

```bash
git clone https://github.com/Saaarmyx/PortfolioS.git
cd Portfolio
npm install
```

## Uso

```bash
npm run dev          # desarrollo en http://localhost:5173
npm run build        # build de producción
npm run preview      # previsualiza el build
npm run check        # svelte-check
npm run check:watch  # svelte-check en modo watch
npm run lint         # prettier --check
npm run format       # prettier --write
```

Para ver solo el póster, abre `index.html` en el navegador. No necesita build.

### Verificación

```bash
npm run check
npm run build
```

El build termina correctamente y `svelte-check` no reporta errores (sí advertencias de CSS no usado). `npm run lint` todavía falla porque Prettier marca `index.html`; formatearlo está en la hoja de ruta. `@sveltejs/adapter-auto` avisa de que no detecta una plataforma de producción; para desplegar hay que elegir un adapter concreto (`adapter-vercel`, `adapter-netlify`, etc.).

## Estructura del proyecto

```text
Portfolio/
├── index.html              # Póster autónomo con estilos embebidos
├── src/
│   ├── app.html            # Documento base de SvelteKit
│   ├── app.d.ts            # Tipos globales de la app
│   ├── lib/
│   │   └── index.js        # Alias #lib
│   └── routes/
│       ├── +layout.svelte  # Layout raíz y favicon
│       └── +page.svelte    # Página principal (esqueleto)
├── static/
│   ├── favicon.svg
│   ├── image.png
│   ├── image2.png
│   ├── saaarmyx.png
│   ├── saaarmyx.svg
│   └── saaarmyx/hero_uno.jpg
├── jsconfig.json
├── prettier.config.js
├── vite.config.js          # SvelteKit + adapter-auto + runes
├── package.json
├── LICENSE
└── README.md
```

> El proyecto no tiene `svelte.config.js`: la integración de SvelteKit se declara directamente en `vite.config.js`.

## Hoja de ruta

- [x] Póster editorial responsive.
- [x] Base de SvelteKit con Svelte 5, TypeScript y Prettier.
- [x] `svelte-check` y build funcionando.
- [ ] Formatear `index.html` para que `npm run lint` pase.
- [ ] Completar las secciones de Sobre mí, Proyectos, Testimonios y Contacto.
- [ ] Reemplazar el retrato de ejemplo por una imagen propia.
- [ ] Convertir el póster en la portada real de la app de SvelteKit.
- [ ] Elegir un adapter de despliegue y publicar el sitio.
- [ ] Añadir pruebas de componentes y una integración continua.
- [ ] Revisar los avisos de CSS no usado que reporta `svelte-check`.

## Contribuir

Es un portafolio personal, así que no espero contribuciones de código. Si encuentras un error o quieres sugerir una mejora, abre un issue. Si aun así quieres enviar un cambio, lee [CONTRIBUTING.md](CONTRIBUTING.md).

## Seguridad

El sitio no tiene backend ni formularios conectados. Si encuentras un problema, sigue [SECURITY.md](SECURITY.md).

## Licencia

Este proyecto se distribuye bajo **MIT License** (`MIT`). Consulta el archivo [LICENSE](LICENSE).

MIT permite usar, copiar, modificar, fusionar, publicar, distribuir, sublicenciar y vender copias del software, siempre que se conserve el aviso de copyright y el texto de la licencia. El software se entrega sin garantías.

Es un proyecto personal de Santiago Sarmiento. No está afiliado a Nexora ni utiliza su marca.

---

Hecho por Santiago Sarmiento
