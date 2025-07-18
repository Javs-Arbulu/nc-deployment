# NC Deployment

Una aplicación full-stack con backend en NestJS y frontend en React con TypeScript.

##  Descripción

Este proyecto es una aplicación full-stack que consiste en:

- **Server**: API REST desarrollada con NestJS y TypeScript
- **Client**: Aplicación web desarrollada con React, TypeScript, Vite y TailwindCSS

##  Estructura del Proyecto

`
nc-deployment/
 server/          # Backend - NestJS API
 client/          # Frontend - React App
 README.md        # Este archivo
`

##  Inicio Rápido

### Prerequisitos

- Node.js (v18 o superior)
- npm o yarn
- Docker y Docker Compose (opcional)

### Instalación Local

1. **Clonar el repositorio**
`ash
git clone <repository-url>
cd nc-deployment
`

2. **Configurar el Backend**
`ash
cd server
npm install
npm run start:dev
`
El servidor estará disponible en http://localhost:3000

3. **Configurar el Frontend**
`ash
cd client
npm install
npm run dev
`
El cliente estará disponible en http://localhost:5173

### Instalación con Docker

1. **Ejecutar el Backend**
`ash
cd server
docker-compose up --build
`

2. **Ejecutar el Frontend**
`ash
cd client
docker-compose up --build
`

##  Tecnologías

### Backend (Server)
- **Framework**: NestJS
- **Lenguaje**: TypeScript
- **Herramientas de desarrollo**: 
  - Nodemon para hot-reload
  - ESLint y Prettier para calidad de código
  - Jest para testing
- **Puerto**: 3000

### Frontend (Client)
- **Framework**: React 19
- **Lenguaje**: TypeScript
- **Build Tool**: Vite
- **Estilos**: TailwindCSS
- **Navegación**: React Router DOM
- **HTTP Client**: Axios
- **Iconos**: Lucide React
- **Puerto**: 5173 (desarrollo) / 4200 (Docker)

##  Estructura Detallada

### Server
`
server/
 src/
    app.module.ts
    main.ts
    common/
    config/
    interfaces/
    modules/
        info/
 test/
 docker-compose.yml
 Dockerfile.dev
 package.json
`

### Client
`
client/
 src/
    components/
       ui/
       layout/
       pages/
    hooks/
    routes/
    services/
    styles/
    constants/
 public/
 docker-compose.yml
 Dockerfile.dev
 package.json
`

##  Scripts Disponibles

### Backend (Server)
`ash
npm run start          # Iniciar en producción
npm run start:dev      # Iniciar en desarrollo con hot-reload
npm run start:debug    # Iniciar en modo debug
npm run build          # Compilar el proyecto
npm run test           # Ejecutar tests
npm run test:e2e       # Ejecutar tests end-to-end
npm run lint           # Ejecutar linter
npm run format         # Formatear código
`

### Frontend (Client)
`ash
npm run dev            # Iniciar servidor de desarrollo
npm run build          # Compilar para producción
npm run preview        # Vista previa de la build
npm run lint           # Ejecutar linter
`

##  Características del Frontend

- **Dark Mode**: Soporte completo para modo oscuro con toggle personalizable
- **Responsive Design**: Diseñado con TailwindCSS para ser completamente responsive
- **Componentes Reutilizables**: Sistema de componentes UI modular
- **Routing**: Navegación SPA con React Router
- **TypeScript**: Tipado estático completo

##  API Endpoints

El backend expone varios endpoints REST. Consulta la documentación específica en el directorio server/ para más detalles.

##  Docker

Ambos servicios incluyen configuración Docker para desarrollo:

- **Server**: Puerto 3000 con hot-reload
- **Client**: Puerto 4200 con hot-reload y polling habilitado

##  Testing

### Backend
`ash
cd server
npm run test           # Unit tests
npm run test:e2e       # Integration tests
npm run test:cov       # Coverage report
`

### Frontend
Los tests del frontend pueden ejecutarse según la configuración específica del proyecto.

##  Desarrollo

### Configuración del Entorno

1. **Variables de Entorno**: Configura las variables necesarias en cada submódulo
2. **ESLint**: Ambos proyectos incluyen configuración de ESLint
3. **Hot Reload**: Configurado tanto para desarrollo local como en Docker

### Estructura de Commits

Se recomienda seguir [Conventional Commits](https://www.conventionalcommits.org/) para mantener un historial de cambios claro.

##  Contribución

1. Fork el proyecto
2. Crea una rama para tu feature (git checkout -b feature/AmazingFeature)
3. Commit tus cambios (git commit -m 'Add some AmazingFeature')
4. Push a la rama (git push origin feature/AmazingFeature)
5. Abre un Pull Request

##  Licencia

Este proyecto es privado y su licencia está sin especificar.

##  Autores

- **Javs-Arbulu** - Desarrollo inicial

---

Para más información específica sobre cada módulo, consulta los README.md individuales en las carpetas server/ y client/.
