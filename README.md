# 🚀 NC Deployment

Aplicación **full-stack** con backend en **NestJS** y frontend en **React** con **TypeScript**.

---

## 📄 Descripción

Este proyecto es una aplicación moderna de arquitectura cliente-servidor:

- **Server**: API REST desarrollada con NestJS y TypeScript.
- **Client**: Aplicación web construida con React, Vite, TailwindCSS y TypeScript.

---

## 🗂️ Estructura del Proyecto

```bash
nc-deployment/
├── server/        # Backend - API NestJS
├── client/        # Frontend - React App
└── README.md      # Este archivo
```

---

## ⚙️ Inicio Rápido

### 📌 Prerrequisitos

- Node.js v18+
- npm o yarn
- Docker y Docker Compose (opcional)

### 💻 Instalación Local

1. **Clonar el repositorio**

```bash
git clone --recurse-submodules <repository-url>
cd nc-deployment

# Si ya lo clonaste sin submódulos
git submodule update --init --recursive
```

2. **Backend**

```bash
cd server
npm install
npm run start:dev
```

> El servidor estará disponible en: http://localhost:3000

3. **Frontend**

```bash
cd ../client
npm install
npm run dev
```

> El cliente estará disponible en: http://localhost:5173

---

### 🐳 Instalación con Docker

```bash
cd nc-deployment
docker-compose up --build
```


---

## 🧰 Tecnologías

### 🔧 Backend

- **Framework**: NestJS
- **Lenguaje**: TypeScript
- **Herramientas**:
  - Nodemon (desarrollo)
  - ESLint + Prettier
  - Jest (testing)
- **Puerto**: `3000`

### 🎨 Frontend

- **Framework**: React 19
- **Lenguaje**: TypeScript
- **Build Tool**: Vite
- **Estilos**: TailwindCSS
- **Routing**: React Router DOM
- **HTTP Client**: Axios
- **Iconos**: Lucide React
- **Puertos**:
  - `5173` (desarrollo)
  - `4200` (Docker)

---

## 🏗️ Estructura Detallada

### Server

```bash
server/
├── src/
│   ├── app.module.ts
│   ├── main.ts
│   ├── common/
│   ├── config/
│   ├── interfaces/
│   └── modules/
│       └── info/
├── test/
├── docker-compose.yml
├── Dockerfile.dev
└── package.json
```

### Client

```bash
client/
├── src/
│   ├── components/
│   │   ├── ui/
│   │   └── layout/
│   │   └── pages/
│   ├── hooks/
│   ├── routes/
│   ├── services/
│   ├── styles/
│   └── constants/
├── public/
├── docker-compose.yml
├── Dockerfile.dev
└── package.json
```

---

## 📜 Scripts Disponibles

### 🔧 Backend

```bash
npm run start         # Inicia en modo producción
npm run start:dev     # Inicia en modo desarrollo con hot-reload
npm run start:debug   # Inicia en modo debug
npm run build         # Compila el proyecto
npm run test          # Ejecuta tests unitarios
npm run test:e2e      # Ejecuta tests e2e
npm run lint          # Corre el linter
npm run format        # Formatea el código
```

### 🎨 Frontend

```bash
npm run dev           # Inicia servidor de desarrollo
npm run build         # Compila para producción
npm run preview       # Vista previa de la build
npm run lint          # Corre el linter
```

---

## ✨ Características del Frontend

- 🌙 **Dark Mode** con toggle personalizado
- 📱 **Responsive Design** con TailwindCSS
- 🧩 **Componentes Reutilizables** organizados modularmente
- 🔁 **SPA Routing** con React Router
- ✅ **TypeScript** en toda la base de código

---

## 🔌 API Endpoints

El backend expone múltiples endpoints REST. Consulta la documentación detallada dentro de `server/`.

---

## 🐋 Docker

- **Server**: puerto `3000`, con hot-reload
- **Client**: puerto `4200`, hot-reload con polling

---

## 🧪 Testing

### Backend

```bash
cd server
npm run test        # Unit tests
npm run test:e2e    # End-to-end tests
npm run test:cov    # Cobertura
```

### Frontend

> Los tests pueden ser ejecutados según la configuración interna del proyecto.

---

## 🛠️ Desarrollo

- 🧪 Variables de entorno por módulo (`.env`)
- 🧹 ESLint + Prettier configurados
- 🔄 Hot Reload en modo desarrollo (local y Docker)

---

## 🧾 Convención de Commits

Se recomienda seguir [Conventional Commits](https://www.conventionalcommits.org/) para mantener un historial de cambios claro y organizado.

---

## 🤝 Contribución

1. Haz un fork del proyecto
2. Crea una rama (`git checkout -b feat/mi-feature`)
3. Commit de tus cambios (`git commit -m 'feat: agrega mi-feature'`)
4. Push a tu rama (`git push origin feat/mi-feature`)
5. Abre un Pull Request

---

## 📄 Licencia

Este proyecto es privado y no cuenta con una licencia pública especificada.

---

## 👨‍💻 Autor

- **Javs-Arbulu** – Desarrollo inicial

---

Para detalles específicos, revisa los archivos `README.md` dentro de los directorios `server/` y `client/`.
