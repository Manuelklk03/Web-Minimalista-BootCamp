## Descripción

Proyecto realizado como práctica de HTML y CSS a partir de un diseño de Figma.

La web replica un portfolio minimalista y está compuesta por varias páginas conectadas entre sí:

- Página principal con proyectos.
- Página About.
- Página de detalle del proyecto "Echoes of Italy".

Durante el desarrollo se han aplicado conceptos como:

- HTML semántico.
- CSS.
- Metodología BEM.
- Flexbox.
- CSS Grid.
- Media queries.
- Diseño responsive para móvil, tablet y escritorio.
## Integración continua y plantilla de releases

El workflow `ci.yml` ejecuta lint, el comando de tests y SonarCloud en las PR hacia `main`.

`.github/workflows/release.yml.example` conserva la propuesta de releases y despliegues como plantilla inactiva. GitHub Actions no la ejecuta mientras tenga la extensión `.example`.

Antes de renombrarla a `release.yml`, hay que añadir el `Dockerfile` y el workflow reutilizable `.github/workflows/deploy.yml`, configurar los entornos `test` y `production` (con la aprobación de producción), las variables `DOCKERHUB_USERNAME` y `TEST_URL` y los secretos de Docker Hub y del método de despliegue elegido. Después se deben validar la publicación y los despliegues. La web actual continúa desplegándose mediante su integración de Netlify.
