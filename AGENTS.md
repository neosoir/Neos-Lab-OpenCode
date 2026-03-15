# Guía para el agente

## Estructura del proyecto

Este es un monorepo con múltiples proyectos en la carpeta `Projects/`. Cada vez que entres a un repo e busca su archivo AGENTS.md para que tengas el contexto cada proyecto.

## Contexto tecnológico

Los proyectos utilizan principalmente:
- **Contenedores**: Docker y Docker Compose
- **Frontend**: React, Next.js
- **Backend**: PHP (Laravel, vanilla), Node.js
- **Bases de datos**: MySQL, PostgreSQL, MongoDB
- **Web Server**: Nginx como reverse proxy

## Cómo trabajar

1. El usuario del sistema se llama Neo y quiero que te refieras a el de esta manera.

2. Antes de hacer cambios, explorar los archivos que vas a modificar.

3. **Archivos clave a identificar:**
   - `docker-compose.yml` → configuración de producción
   - `docker-compose.dev.yml` → configuración de desarrollo local
   - `Dockerfile` → imagen del contenedor
   - Configuraciones de Nginx (desarrollo y producción)

4. No puedes ejecutar los contenedores de los proyectos por timismo pide ayuda al usuario para eso (pero si tienes curl y wscat para debuguear ciertas configuraciones).

5. Siempre ocupar variables de entono, no harcodes ninguna varible eso puede ser peligroso, asegurate de poner debugs para rastrear los errores en las env. si no tienes una variable en tu proceso de contruccion avisalea a neo para que este enterado y la ponga.

   - En el codigo que creas nunca poner un segunda opcion en la variable de entorno por defecto ejemplo $this->appId = env('FACEBOOK_APP_ID', '1234567890'); o  BASE_URL: import.meta.env.VITE_API_BASE_URL || 'http://api.cms', si el sistema no tiene la env debe de fallar este tipo de propuestas hacen dificil el debug.

   - En lavel simpre usa las variables de entorno este tipo de configuraciones hacen mas dificil el codigo: $mediaUrl = config('app.api_url', 'https://api.neoslab.tech') . '/media/' . $relativePath;

