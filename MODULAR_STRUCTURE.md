# Estructura Modular de Componentes - Iglesia Nueva Casa

## Estructura de Archivos

```
src/
├── components/
│   ├── layout/           # Componentes de layout reutilizables
│   │   ├── Layout.tsx    # Layout principal con Navbar y Footer
│   │   ├── Navbar.tsx    # Barra de navegación
│   │   └── Footer.tsx    # Pie de página
│   │
│   ├── sections/         # Secciones de la página principal
│   │   ├── HeroSection.tsx       # Sección hero con estadísticas
│   │   ├── ServiciosSection.tsx  # Sección de servicios
│   │   ├── NosotrosSection.tsx   # Sección "Sobre nosotros"
│   │   ├── ConectaSection.tsx    # Sección de conexión/ministerios
│   │   └── CTASection.tsx        # Sección de llamada a la acción
│   │
│   ├── pages/            # Páginas completas
│   │   ├── IglesiaPage.tsx       # Página principal modularizada
│   │   ├── about/
│   │   │   └── index.tsx         # Página "Nosotros"
│   │   ├── ContactoPage.tsx      # Página de contacto
│   │   └── index.tsx             # Home que renderiza IglesiaPage
│   │
│   ├── ui/               # Componentes UI base
│   └── index.ts          # Exports centralizados
│
├── routes/               # Configuración de rutas
│   ├── AppRoutes.tsx
│   ├── routes.config.tsx
│   └── routes.constants.ts
```

## Componentes Disponibles

### Layout Components

- **Layout**: Wrapper principal que incluye Navbar y Footer
- **Navbar**: Barra de navegación con enlaces a rutas
- **Footer**: Pie de página con información de contacto

### Section Components

- **HeroSection**: Sección principal con hero y estadísticas
- **ServiciosSection**: Información sobre horarios y servicios
- **NosotrosSection**: Historia y valores de la iglesia
- **ConectaSection**: Ministerios y grupos disponibles
- **CTASection**: Llamada a la acción y formulario de suscripción

### Page Components

- **IglesiaPage**: Página principal que combina todas las secciones
- **AboutPage**: Página detallada sobre la iglesia
- **ContactoPage**: Página de contacto con formulario

## Cómo Usar

### Crear una Nueva Página

```tsx
import Layout from "@/components/layout/Layout";

export default function NuevaPagina() {
  return (
    <Layout>
      {/* Tu contenido aquí */}
      <section className="py-24">
        <div className="container mx-auto px-4">
          <h1>Mi Nueva Página</h1>
        </div>
      </section>
    </Layout>
  );
}
```

### Agregar una Nueva Ruta

1. Agrega la constante en `routes/routes.constants.ts`:

```typescript
export const ROUTES = {
  // ... rutas existentes
  NUEVA_PAGINA: "/nueva-pagina",
} as const;
```

2. Agrega la ruta en `routes/routes.config.tsx`:

```tsx
import NuevaPagina from "../components/pages/NuevaPagina";

export const routes: RouteObject[] = [
  // ... rutas existentes
  {
    path: ROUTES.NUEVA_PAGINA,
    element: <NuevaPagina />,
  },
];
```

### Reutilizar Secciones

Puedes reutilizar cualquier sección en otras páginas:

```tsx
import Layout from "@/components/layout/Layout";
import { HeroSection, CTASection } from "@/components";

export default function PaginaPersonalizada() {
  return (
    <Layout>
      <HeroSection />
      {/* Tu contenido personalizado */}
      <CTASection />
    </Layout>
  );
}
```

## Ventajas de esta Estructura

1. **Modularidad**: Cada componente tiene una responsabilidad específica
2. **Reutilización**: Los componentes pueden usarse en múltiples páginas
3. **Mantenimiento**: Fácil de mantener y actualizar
4. **Escalabilidad**: Simple agregar nuevas páginas y secciones
5. **Consistencia**: Layout uniforme en todas las páginas
6. **Performance**: Carga solo los componentes necesarios

## Rutas Disponibles

- `/` - Página principal (IglesiaPage)
- `/about` - Página sobre nosotros
- `/contacto` - Página de contacto
- `/ministerios/jovenes` - Ministerio de jóvenes
- `/ministerios/ninos` - Ministerio de niños
- `/ministerios/matrimonios` - Ministerio de matrimonios
- `/eventos` - Página de eventos

## Próximos Pasos

1. Implementar las páginas faltantes (ministerios, eventos)
2. Agregar funcionalidad de formularios
3. Implementar modo oscuro consistente
4. Agregar animaciones y transiciones
5. Optimizar para SEO
