# Guía para el agente

## Estructura del proyecto

Este es un monorepo con múltiples proyectos en la carpeta `Projects/`.

## Contexto tecnológico

Los proyectos utilizan principalmente:
- **Contenedores**: Docker y Docker Compose
- **Frontend**: React, Next.js
- **Backend**: PHP (Laravel, vanilla), Node.js
- **Bases de datos**: MySQL, PostgreSQL, MongoDB
- **Web Server**: Nginx como reverse proxy

## Cómo trabajar

1. Cuando el usuario mencione un proyecto, identificar su ruta dentro de `Projects/`
2. Antes de hacer cambios, explorar la estructura del proyecto
3. **Archivos clave a identificar:**
   - `docker-compose.yml` → configuración de producción
   - `docker-compose.dev.yml` → configuración de desarrollo local
   - `Dockerfile` → imagen del contenedor
   - Configuraciones de Nginx (desarrollo y producción)
4. La mayoría del tiempo se trabaja con `docker-compose.dev.yml` (configuración local)
