# Microservicio de Metadatos de Archivo

Proyecto de la certificación **Back End Development and APIs Projects** de freeCodeCamp.

Un microservicio simple que analiza archivos subidos y devuelve información básica sobre ellos (nombre, tipo MIME y tamaño).

## API

**POST** `/api/fileanalyse`

Sube un archivo usando el campo `upfile` en un formulario multipart/form-data.

### Respuestas

**Respuesta exitosa:**
```json
{
  "name": "documento.pdf",
  "type": "application/pdf", 
  "size": 245760
}
```

**Sin archivo:**
```json
{
  "error": "File not found"
}
```

### Campos de respuesta

- `name` - Nombre original del archivo
- `type` - Tipo MIME del archivo (ej: image/jpeg, text/plain, application/pdf)
- `size` - Tamaño del archivo en bytes

## Tecnologías

Node.js, Express.js, Multer para manejo de archivos

## Ejecutar

```bash
npm install
npm run start
```

Servidor disponible en `http://localhost:3000`
