# Flujo funcional - Petición en 3 Clics

## Flujo principal

1. Crear una causa comunitaria.
2. Registrar apoyos ciudadanos.
3. Visualizar número de apoyos.
4. Generar documento PDF.
5. Notificar nuevo apoyo por n8n/Telegram.
6. Presentar demo final.

## Día 1

En la Clase 56 se creó:

- Repositorio nuevo.
- Servidor Node.js.
- Base de datos SQLite.
- Tabla causas.
- Tabla apoyos.
- Rutas iniciales.
- Pruebas con curl.


### Paso 7: Probar crear causa
curl -X POST http://localhost:3000/api/causas \
  -H "Content-Type: application/json" \
  -d '{
    "titulo": "Solicitud de iluminación del parque comunitario",
    "descripcion": "La comunidad solicita revisar y mejorar la iluminación del parque principal para facilitar su uso seguro en horas de la noche."
  }'
### Respuesta esperada:
{
  "ok": true,
  "mensaje": "Causa creada correctamente",
  "id": 1
}


### Paso 8: Probar listar causas
curl http://localhost:3000/api/causas
### Respuesta esperada:
{
  "ok": true,
  "total": 1,
  "causas": [
    {
      "id": 1,
      "titulo": "Solicitud de iluminación del parque comunitario",
      "descripcion": "La comunidad solicita revisar y mejorar la iluminación del parque principal para facilitar su uso seguro en horas de la noche.",
      "fecha_creacion": "2026-..."
    }
  ]
}

### Paso 9: Probar registrar apoyo
curl -X POST http://localhost:3000/api/apoyos \
  -H "Content-Type: application/json" \
  -d '{
    "causa_id": 1,
    "nombre": "Ciudadano de práctica",
    "comentario": "Apoyo esta solicitud porque beneficia a la comunidad."
  }'
### Respuesta esperada:
{
  "ok": true,
  "mensaje": "Apoyo registrado correctamente",
  "id": 1
}

### Paso 10: Probar listar apoyos
curl http://localhost:3000/api/apoyos/1
### Respuesta esperada:
{
  "ok": true,
  "total": 1,
  "apoyos": [
    {
      "id": 1,
      "causa_id": 1,
      "nombre": "Ciudadano de práctica",
      "comentario": "Apoyo esta solicitud porque beneficia a la comunidad.",
      "fecha": "2026-..."
    }
  ]
}


# Flujo funcional - Petición en 3 Clics

## Flujo principal

1. Crear una causa comunitaria.
2. Registrar apoyos ciudadanos.
3. Visualizar número de apoyos.
4. Generar documento PDF.
5. Notificar nuevo apoyo por n8n/Telegram.
6. Presentar demo final.

## Día 1

En la Clase 56 se creó:

- Repositorio nuevo.
- Servidor Node.js.
- Base de datos SQLite.
- Tabla causas.
- Tabla apoyos.
- Rutas iniciales.
- Pruebas con curl.

## Regla de privacidad

No se solicitan cédulas, teléfonos, direcciones ni datos sensibles.




## Regla de privacidad

No se solicitan cédulas, teléfonos, direcciones ni datos sensibles.