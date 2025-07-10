## 📡 API de Login

`POST /api/login`

Permite autenticar al usuario y obtener un token de acceso para operaciones posteriores.

### Campos requeridos

- `email` – Dirección de correo electrónico registrada.
- `password` – Contraseña correspondiente.

### Ejemplo de petición
```json
{
  "email": "usuario@example.com",
  "password": "MiC0ntr4sena"
}
```

### Respuesta exitosa
```json
{
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "expires_in": 3600
}
```

!!! note "Seguridad"
    El token debe enviarse en el encabezado `Authorization: Bearer` en cada solicitud posterior. Utiliza HTTPS para proteger las credenciales.

