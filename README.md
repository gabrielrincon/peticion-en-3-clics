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