# Contribuir a Portfolio

Gracias por pasarte. Portfolio es mi tarjeta de presentación personal, así que el contenido y el diseño los decido yo. Dicho eso, los reportes de errores y las mejoras técnicas son bienvenidos.

## Antes de empezar

Abre un issue antes de enviar un cambio grande: una sección nueva, un rediseño o un adapter de despliegue. Para corregir una errata o un detalle de accesibilidad, puedes ir directo al Pull Request.

## Flujo de trabajo

1. Haz un fork del repositorio.
2. Crea una rama desde `main`:

   ```bash
   git checkout -b fix/favicon-ruta
   ```

   Usa prefijos `feat/`, `fix/` o `docs/` y nombres en kebab-case.

3. Haz commits atómicos con [Conventional Commits](https://www.conventionalcommits.org/es/v1.0.0/):

   ```text
   feat(routes): añade la sección de proyectos
   fix(layout): corrige la ruta del favicon
   docs(readme): documenta el adapter de despliegue
   ```

4. Abre un Pull Request contra `main` explicando qué cambia y cómo lo verificaste.

## Entorno de desarrollo

```bash
git clone https://github.com/Saaarmyx/PortfolioS.git
cd Portfolio
npm install

npm run dev
npm run check
npm run lint
npm run build
```

Para el póster no hace falta servidor: abre `index.html` directamente.

## Estándares de código

- **Svelte 5** en modo runes; no mezcles la API antigua de stores si no hace falta.
- **TypeScript** estricto según `jsconfig.json`.
- **Prettier** con tabs, comillas simples, sin comas finales y ancho de 100.
- **Estilos:** el póster usa CSS embebido; la app puede usar estilos scoped de Svelte.
- **Assets:** van en `static/` y se referencian desde la raíz (`/imagen.png`).
- **Tests:** no hay suite todavía. Como mínimo, `npm run check`, `npm run lint` y `npm run build` deben pasar.

## Checklist del Pull Request

- [ ] El cambio está explicado y respeta el carácter personal del sitio.
- [ ] `npm run check` pasa sin errores.
- [ ] `npm run lint` pasa.
- [ ] `npm run build` pasa.
- [ ] No añadí dependencias sin justificarlo.
- [ ] Actualicé `CHANGELOG.md` si el cambio es visible.
- [ ] No incluí imágenes personales sin permiso.
- [ ] El commit sigue Conventional Commits.

## Proceso de revisión

Reviso los PR cuando puedo, sin plazos fijos. Al ser un proyecto personal, puedo rechazar cambios de contenido o de diseño aunque estén bien implementados. Te explicaré el motivo.

## Acuerdo de contribución

No hay CLA. Al enviar una contribución aceptas que se incorpore al proyecto bajo **MIT License** (`MIT`), la misma licencia del repositorio.

## Código de conducta

- Respeta a las demás personas y su trabajo.
- Crítica el código, no a quien lo escribió.
- No publiques datos personales ni imágenes de terceros sin permiso.
- No reportes vulnerabilidades en issues públicos.

## Licencia

Las contribuciones quedan bajo **MIT License** (`MIT`). Consulta [LICENSE](LICENSE).
