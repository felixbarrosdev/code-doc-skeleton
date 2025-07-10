## 🧩 Reglas de Negocio - Autenticación

Las siguientes reglas definen el comportamiento esperado durante el proceso de autenticación. Su objetivo es proteger la integridad de las cuentas y garantizar una experiencia consistente.

### Listado de reglas

- **R1** – Todo usuario debe proveer un *correo electrónico* y *contraseña* válidos para acceder al sistema.
- **R2** – Después de **5 intentos fallidos** el usuario será bloqueado durante 10 minutos.
- **R3** – Las contraseñas se almacenan de forma cifrada utilizando un algoritmo de hashing robusto.
- **R4** – El token de sesión expira luego de 60 minutos de inactividad.

### Aplicación

Estas reglas se aplican en el flujo de inicio de sesión y en cada llamada que requiera autenticación. Cualquier modificación debe actualizarse también en la [API de Login](../apis/login-api.md) para mantener la coherencia.

