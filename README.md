# Capítulo V: Introducción

## 5.1. Software Configuration Management.
### 5.1.1. Software Development Environment Configuration.
El entorno de desarrollo fue configurado utilizando herramientas ampliamente adoptadas en proyectos open source.

### Herramientas por tipo de actividad

| Actividad                         | Herramienta(s) utilizada(s)                    | Tipo     | Enlace de referencia                                                                 |
|-----------------------------------|------------------------------------------------|----------|----------------------------------------------------------------------------------------|
| Project Management                | Trello, GitHub Projects                        | SaaS     | [Trello](https://trello.com) / [GitHub Projects](https://github.com)                 |
| Requirements Management           | Google Docs, Google Sheets                     | SaaS     | [Google Docs](https://docs.google.com)                                               |
| Product UX/UI Design              | Figma                                          | SaaS     | [Figma](https://figma.com)                                                           |
| Software Development              | WebStorm, Visual Studio Code, Node.js, Git, Angular    | Local    | [WebStorm](https://www.jetbrains.com/webstorm/) / [VS Code](https://code.visualstudio.com) / [Node.js](https://nodejs.org) / [Git](https://git-scm.com) / [Angular](https://angular.dev)|
| Software Deployment               | Vercel, Netlify, Railway, Render               | SaaS     | [Vercel](https://vercel.com) / [Netlify](https://www.netlify.com) / [Railway](https://railway.app) |
| Software Documentation            | Google Docs, Markdown, Swagger, Structurizer   | SaaS/Local| [Google Docs](https://docs.google.com) / [Swagger](https://swagger.io)               |

### 5.1.2. Source Code Management.
Se utilizó Git como sistema de control de versiones y GitHub como plataforma de hospedaje. El proyecto fue dividido en múltiples repositorios:

Landing Page: https://github.com/flow-sense/landing

Web Services: https://github.com/flow-sense/api

Frontend Web App: https://github.com/flow-sense/frontend

Se adoptó el workflow GitFlow, basado en el modelo de Vincent Driessen (“A successful Git branching model”), para organizar las ramas de trabajo. Este flujo permite una separación clara entre las versiones estables, los desarrollos activos y las correcciones urgentes. Las ramas empleadas son:

- main: contiene la versión estable y liberada del producto. Cada merge a esta rama representa una versión deployada.

- develop: rama principal de desarrollo donde se integran los feature branches.

- feature/<nombre>: para cada nueva funcionalidad, se crea una rama individual. Ejemplo: feature/login-auth, feature/task-tracking.

- release/<version>: rama temporal que permite realizar pruebas y ajustes antes de pasar a producción. Ejemplo: release/v1.1.0.

- hotfix/<descripcion>: ramas para corregir errores críticos encontrados en producción. Ejemplo: hotfix/fix-null-user.

Cada release se nombra siguiendo Semantic Versioning 2.0.0, utilizando el formato MAJOR.MINOR.PATCH:

- Cambios incompatibles: 2.0.0

- Nuevas funcionalidades compatibles: 2.1.0

- Correcciones de bugs: 2.1.1

Se usaron etiquetas (tags) en Git para marcar los releases formales: v1.0.0, v1.1.0-beta, etc.

Además, para mantener un historial claro y legible en el repositorio, se aplicó la convención [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/), con el siguiente formato:

| **<'tipo'>(alcance): descripcion breve** |
|------------------------------------------|

Donde el <"tipo"> puede ser: feat, fix, docs, style, refactor, test, chore, entre otros.

**Ejemplos de commits:**

- feat(auth): implement Google login integration

- fix(api): prevent crash on empty request body

- refactor(ui): simplify dashboard component hierarchy

### 5.1.3. Source Code Style Guide & Conventions

Para mantener la consistencia del código fuente se adoptaron las siguientes guías y convenciones:

- **HTML/CSS**: [W3 HTML Style Guide](https://www.w3schools.com/html/html5_syntax.asp), [Google HTML/CSS Guide](https://google.github.io/styleguide/htmlcssguide.html)
- **JavaScript/TypeScript**: [Google TypeScript Style Guide](https://google.github.io/styleguide/tsguide.html), ESLint + Prettier
- **Java**: [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html), aplicado si se emplea Spring Boot
- **Especificaciones BDD (si aplica)**: [Gherkin Syntax](https://cucumber.io/docs/gherkin/)

Además, se adoptaron las siguientes prácticas:
- Uso del idioma inglés para nombrar funciones, variables, clases y archivos.
- Aplicación de principios SOLID y clean code.
- Separación modular del código, fomentando la reutilización de componentes y funciones puras.
 
### 5.1.4. Software Deployment Configuration

El proceso de despliegue fue automatizado usando plataformas como **Vercel**, **Netlify** o **Railway**. El frontend y la landing page fueron desplegados directamente desde los repositorios de GitHub mediante integración continua (CI). Para el backend se configuró un entorno en Railway o Render.

#### Pasos generales de despliegue:

1. Un push a las ramas `main` o `release/*` activa un proceso de despliegue automático.
2. Se incluyeron archivos de configuración según la plataforma:
   - `vercel.json` para Vercel
   - `netlify.toml` para Netlify
   - `Dockerfile` en caso de uso de contenedores
3. Las variables de entorno fueron configuradas directamente en la plataforma correspondiente (por ejemplo, claves de API, bases de datos, credenciales).
4. Las APIs fueron desplegadas y expuestas mediante HTTPS, y documentadas utilizando herramientas como **Swagger** o **Postman**.

## 5.2. Landing Page, Services & Applications Implementation.
### 5.2.1. Sprint 1
#### 5.2.1.1. Sprint Planning 1.
#### 5.2.1.2. Aspect Leaders and Collaborators.
#### 5.2.1.3. Sprint Backlog 1.
#### 5.2.1.4. Development Evidence for Sprint Review.
#### 5.2.1.5. Execution Evidence for Sprint Review.
#### 5.2.1.6. Services Documentation Evidence for Sprint Review.
#### 5.2.1.7. Software Deployment Evidence for Sprint Review.
#### 5.2.1.8. Team Collaboration Insights during Sprint.
