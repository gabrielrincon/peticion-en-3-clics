## Paso 3: Crear `docs/transferencia-tecnica.md`

# Transferencia técnica - Petición en 3 Clics

## Objetivo

Permitir que otra persona pueda instalar, ejecutar y entender el proyecto.

## Requisitos

- Node.js
- npm
- Git
- GitHub Codespaces o entorno local
- n8n opcional
- Telegram opcional

## Instalación

```bash
npm install
```

## Ejecución

```bash
npm start
```

## Variables de entorno

```bash
PORT=3000
DB_PATH=./database.sqlite
N8N_ENABLED=false
N8N_WEBHOOK_APOYO=
```

## Rutas principales

- GET /estado
- GET /api/causas
- POST /api/causas
- POST /api/apoyos
- GET /api/apoyos/:causaId
- GET /api/pdf/:causaId

## Flujo funcional

Crear causa.
Registrar apoyo.
Ver contador.
Descargar PDF.
Notificar por n8n/Telegram si está configurado.
