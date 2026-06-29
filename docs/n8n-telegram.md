# n8n y Telegram - Notificación no sensible

## Objetivo

Notificar que se registró un nuevo apoyo en una causa comunitaria sin exponer datos personales.

## Flujo

1. Usuario registra apoyo en la plataforma.
2. Node.js guarda el apoyo en SQLite.
3. Node.js llama webhook de n8n.
4. n8n envía mensaje por Telegram.
5. Telegram solo recibe una alerta general.

## Webhook

Variable:

```env
N8N_WEBHOOK_APOYO=
```
## payload enviado al n8n

```json
{
  "evento": "nuevo_apoyo",
  "causaId": 1,
  "mensaje": "Nuevo apoyo registrado en una causa comunitaria.",
  "datosPersonales": false
}
```

