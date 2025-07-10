## 🧑‍💻 Flujo de Login de Usuario

El siguiente diagrama de pasos describe cómo un usuario accede al sistema hasta visualizar su dashboard principal.

### Pasos del flujo

1. El usuario ingresa a la ruta `/login` desde su navegador.
2. Se carga el formulario de autenticación con campos de **correo** y **contraseña**.
3. El usuario completa sus credenciales y hace clic en **Iniciar sesión**.
4. El servidor valida los datos recibidos.
5. Si las credenciales son correctas, se genera un token de sesión y se almacena en una cookie segura.
6. El sistema redirige automáticamente al usuario a `/dashboard`.
7. Finalmente se muestran los widgets principales del panel de control.

### Notas adicionales

- El formulario debe ser accesible y responder en dispositivos móviles.
- Se recomienda mostrar un indicador de carga mientras se verifica la información.

!!! note "¿Olvidaste tu contraseña?"
    Utiliza la opción *Recuperar contraseña* para recibir un enlace de restablecimiento en tu correo electrónico.

!!! warning "Importante"
    Por motivos de seguridad se bloquea la cuenta tras **5 intentos fallidos** en un lapso de 10 minutos.

