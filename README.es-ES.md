

# Better-T Stack

Una plantilla moderna de monorepositorio en TypeScript impulsada por Hono, tRPC, TanStack Router, Tailwind CSS, shadcn/ui, Better-Auth y
Drizzle con libSQL: todo empaquetado junto con Bun para un máximo rendimiento.

## 🚀 Stack Tecnológico

### Núcleo
- [Bun](https://bun.sh/) - Runtime de JavaScript todo en uno y rápido
- [TypeScript](https://www.typescriptlang.org/) - Seguridad de tipos en todo el stack
- [tRPC](https://trpc.io/) - APIs con seguridad de tipos de extremo a extremo

### Frontend
- [TanStack Router](https://tanstack.com/router) - Enrutamiento con seguridad de tipos
- [Tailwind CSS](https://tailwindcss.com/) - Framework CSS orientado a utilidades
- [shadcn/ui](https://ui.shadcn.com/) - Componentes reutilizables

### Backend
- [Hono](https://hono.dev/) - Framework web ultrarrápido
- [Better-Auth](https://www.better-auth.com/) - Solución de autenticación moderna
- [Drizzle ORM](https://orm.drizzle.team/) - ORM para TypeScript
- [libSQL](https://github.com/libsql/libsql) - Motor de base de datos compatible con SQLite

## 📁 Estructura del Proyecto

```bash
.
├── packages/
│   ├── client/                 # Aplicación React del frontend
│   │   ├── src/
│   │   │   ├── components/    # Componentes de UI
│   │   │   ├── routes/        # Rutas de TanStack Router
│   │   │   └── lib/           # Utilidades y configuraciones
│   │   └── ...
│   └── server/                 # API Backend con Hono
│       ├── src/
│       │   ├── db/            # Esquema y configuración de la base de datos
│       │   ├── lib/           # Configuración de autenticación y tRPC
│       │   └── routers/       # Routers de tRPC
│       └── ...
```

## 🚦 Primeros Pasos

1. Clona (o utiliza la plantilla de GitHub) e instala las dependencias:
```bash
npx degit AmanVarshney01/Better-T-Stack my-project
cd my-project
bun install
```

2. Configura la base de datos:
```bash
# Inicia la base de datos SQLite local con turso
bun run db:local

# Empuja el esquema de la base de datos
bun run db:push
```

3. Inicia los servidores de desarrollo:
```bash
# Inicia tanto el cliente como el servidor
bun run dev

# O individualmente:
bun run dev:client
bun run dev:server
```

El cliente estará disponible en `http://localhost:3001`

## 📝 Scripts Disponibles

### Raíz
- `bun dev` - Inicia todos los servidores de desarrollo
- `bun dev:client` - Inicia el servidor de desarrollo del cliente
- `bun dev:server` - Inicia el servidor de desarrollo del backend
- `bun db:local` - Inicia la base de datos SQLite local
- `bun db:push` - Empuja los cambios del esquema de la base de datos
- `bun clean` - Limpia todos los directorios node_modules y archivos de bloqueo

### Cliente
- `bun typecheck` - Ejecuta la verificación de tipos de TypeScript
- `bun build` - Compila para producción
- `bun serve` - Previsualiza la compilación de producción

### Servidor
- `bun dev` - Inicia el servidor de desarrollo con recarga en caliente
- `bun wrangler:dev` - Ejecuta con Cloudflare Workers localmente
- `bun wrangler:deploy` - Implementa en Cloudflare Workers

## 💻 Desarrollo

Esta plantilla está configurada para ofrecer una experiencia de desarrollo óptima desde el primer momento:

- Configuración TypeScript full-stack
- Seguridad de tipos de extremo a extremo con tRPC
- Autenticación moderna con Better-Auth
- Componentes de UI atractivos de shadcn/ui
- Servidor de desarrollo rápido con Bun
- Listo para producción con soporte para Cloudflare Workers
