# Petición en 3 Clics

Plataforma comunitaria para crear causas, registrar apoyos y generar un PDF colectivo.

## Objetivo

Construir una herramienta sencilla de participación ciudadana que permita organizar solicitudes comunitarias y registrar apoyos.

## Instalación

```bash
npm install
```

## Generación de PDF

La Clase 58 agrega generación de PDF colectivo.

Ruta:

```txt
GET /api/pdf/:causaId
```

```bash
curl -L http://localhost:3000/api/pdf/1 --output peticion-causa-1.pdf
```

No hay mas comentarios

## Paso 4: Actualizar README.md

Agregar o reemplazar con una versión más completa:

# Petición en 3 Clics

Plataforma comunitaria para crear causas, registrar apoyos, generar un PDF colectivo y notificar nuevos apoyos de forma segura.

## Objetivo

Construir una herramienta sencilla de participación ciudadana para organizar causas comunitarias y evidenciar apoyos ciudadanos sin recolectar datos sensibles.

## Tecnologías

- Node.js
- Express
- SQLite
- HTML
- CSS
- JavaScript
- PDFKit
- n8n opcional
- Telegram opcional

## Instalación

```bash
npm install
```

## CURLs

```bash
curl -X POST http://localhost:3000/api/apoyos \
  -H "Content-Type: application/json" \
  -d '{
    "causa_id": 1,
    "nombre": "Ciudadano de práctica",
    "comentario": "Apoyo esta causa."
  }'
```

### respuesta

```json
{
  "ok": true,
  "mensaje": "Apoyo registrado correctamente",
  "notificacion": {
    "ok": false,
    "modo": "mock",
    "mensaje": "Notificación n8n no configurada"
  }
}
```

