# OpenCoVive

Entorno de desarrollo containerizado para trabajar con OpenCode AI.

## Instalación y Uso

### 1. Arrancar los contenedores

```bash
docker compose up -d
```

### 2. Entrar al contenedor

```bash
docker compose exec -it opencode bash
```

### 3. Ejecutar OpenCode

```bash
npx opencode
```

## Estructura de Proyectos

```
workspace/
├── Projects/           # ← Carpeta donde se proyectos
│   ├── proyecto-1/     #   para analizar con IA
│   │   ├── src/
│   │   └── ...
│   ├── proyecto-2/
│   │   ├── src/
│   │   └── ...
│   └── ...
├── docker-compose.yml
└── README.md
```

Todos los proyectos que deseas analizar deben estar dentro de la carpeta `Projects/`. La IA podrá acceder y analizar todos los proyectos de manera anidada desde esa ubicación.
