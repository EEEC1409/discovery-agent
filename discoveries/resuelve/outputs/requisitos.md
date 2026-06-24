# Requisitos candidatos — Discovery Resuelve

> **Fuente única:** `Entrevistas_APP_Resuelve.md`
> Todos los requisitos se derivan de las 39 user stories del backlog convertidas
> en formato de entrevista. Se listan primero los funcionales agrupados por dominio,
> luego los no funcionales.

---

## Requisitos funcionales

### Onboarding e identidad de marca

- **[R-01]** La APP debe mostrar una pantalla de bienvenida animada con el logo y video de la marca Resuelve al primer inicio.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-001 · Cliente

### Verificación y enrutamiento

- **[R-02]** La APP debe verificar si el número de cédula ingresado corresponde a un cliente Resuelve y determinar el flujo a seguir (pre-aprobado, nuevo, en revisión, no califica).
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-002 · Cliente

- **[R-03]** El cliente pre-aprobado debe poder ver su oferta de línea de crédito y completar la solicitud en 3 pasos desde la APP.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-003 · Cliente

- **[R-04]** La APP debe mostrar un mensaje claro de rechazo cuando el cliente no califica o está en lista negra.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-004 · Cliente

- **[R-05]** El cliente con solicitud en proceso debe poder ver el estado actual de su solicitud.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-005 · Cliente

- **[R-06]** El cliente con línea de crédito inactiva debe ver su capacidad de pago y las opciones disponibles para activarla.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-006 · Cliente

### Registro

- **[R-07]** El cliente nuevo debe poder ingresar sus datos personales (nombre, teléfono, correo) para crear una cuenta en la APP.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-007 · Cliente

- **[R-08]** El sistema debe enviar un código OTP al correo del cliente y validarlo durante el registro para confirmar su identidad.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-008 · Cliente

- **[R-09]** El cliente debe poder crear una contraseña personal para acceder a su cuenta de forma segura.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-009 · Cliente

- **[R-10]** Al completar el registro, el sistema debe persistir la información del cliente en todos los sistemas integrados garantizando consistencia.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-010 · Sistema

- **[R-11]** La APP debe mostrar mensajes de error claros y accionables cuando algo falle durante el proceso de registro.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-011 · Cliente

### Autenticación y sesión

- **[R-12]** El cliente registrado debe poder iniciar sesión con su cédula y contraseña.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-012 · Cliente

- **[R-13]** La APP debe admitir autenticación biométrica (Face ID o huella dactilar) como alternativa al login con contraseña.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-013 · Cliente

- **[R-14]** El cliente debe poder recuperar su contraseña mediante un enlace enviado a su correo registrado.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-014 · Cliente

- **[R-15]** La APP debe permitir cerrar sesión desde cualquier pantalla.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-015 · Cliente

- **[R-35]** La APP debe detectar la expiración de sesión, notificar al cliente y redirigirlo al login.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-035 · Cliente

### Dashboard y estado de cuenta

- **[R-16]** La APP debe mostrar un dashboard con saludo personalizado y resumen del estado del crédito al iniciar sesión.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-016 · Cliente

- **[R-17]** El cliente debe poder seleccionar el modelo visual de su tarjeta Resuelve dentro de la APP.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-017 · Cliente

- **[R-18]** El cliente debe poder consultar su estado de cuenta con el detalle de cuota al cobro, cuota consumida y fecha mínima de pago.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-018 · Cliente

- **[R-21]** El cliente debe poder ver el historial de movimientos (consumos y notas de crédito).
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-021 · Cliente

### Gamificación y retención

- **[R-19]** La APP debe mostrar un gráfico de progreso con los beneficios y premios que el cliente puede obtener según su comportamiento de pago.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-019 · Cliente

- **[R-20]** La APP debe mostrar una notificación visual de celebración con el premio ganado cuando el cliente pague a tiempo.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-020 · Cliente

- **[R-37]** El sistema debe enviar notificaciones push al cliente cuando se aproxime su fecha de pago.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-037 · Cliente

### Programa de puntos y canje

- **[R-22]** La APP debe mostrar el saldo de puntos vigentes del cliente.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-022 · Cliente

- **[R-23]** El cliente debe poder ver el historial detallado de puntos recibidos y redimidos.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-023 · Cliente

- **[R-24]** El cliente debe poder explorar el catálogo de productos disponibles para canje.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-024 · Cliente

- **[R-25]** El cliente debe poder usar sus puntos para reducir la cuota mensual de un producto en canje.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-025 · Cliente

- **[R-26]** La APP debe mostrar el detalle completo de un producto (descripción, puntos requeridos, cuota) antes de confirmar el canje.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-026 · Cliente

- **[R-27]** El cliente debe poder confirmar o modificar su dirección de entrega durante el proceso de canje.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-027 · Cliente

- **[R-28]** El sistema debe validar en tiempo real si el cliente cumple los requisitos de elegibilidad antes de registrar el canje.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-028 · Sistema

- **[R-29]** El cliente debe poder validar su identidad con Face ID para autorizar el canje de forma segura.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-029 · Cliente

- **[R-30]** El sistema debe registrar el canje correctamente y enviar confirmación visual y por correo al cliente.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-030 · Cliente

- **[R-31]** La APP debe informar al cliente no elegible el motivo específico del rechazo del canje y las acciones que puede tomar.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-031 · Cliente

### Perfil y gestión de cuenta

- **[R-32]** El cliente debe poder ver toda su información personal en un solo lugar dentro de la APP.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-032 · Cliente

- **[R-33]** El cliente autenticado debe poder cambiar su contraseña desde la sección Mi Perfil sin necesidad de cerrar sesión.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-033 · Cliente

- **[R-34]** El cliente debe poder solicitar la eliminación de su cuenta mediante un proceso claro con confirmación.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-034 · Cliente

### Administración de contenido

- **[R-38]** El administrador de negocio debe poder actualizar el banner de la APP desde el back-office sin necesidad de publicar una nueva versión.
  - Tipo: funcional
  - Origen: `Entrevistas_APP_Resuelve.md` · US-038 · Administrador de negocio

---

## Requisitos no funcionales

- **[R-36]** La APP debe mostrar mensajes de error claros y diferenciados cuando no haya conexión a internet o los servicios estén caídos.
  - Tipo: no funcional (experiencia ante fallos)
  - Origen: `Entrevistas_APP_Resuelve.md` · US-036 · Cliente

- **[R-39]** La APP debe ser accesible y garantizar tiempos de respuesta aceptables con independencia del dispositivo o las capacidades del usuario.
  - Tipo: no funcional (accesibilidad y rendimiento)
  - Origen: `Entrevistas_APP_Resuelve.md` · US-039 · Cliente

- **[R-40]** Todos los flujos críticos (registro, login, canje, pago) deben completarse de forma simple, rápida y segura; ninguna operación sensible debe quedar expuesta sin autenticación.
  - Tipo: no funcional (usabilidad y seguridad transversal)
  - Origen: `Entrevistas_APP_Resuelve.md` · respuesta genérica recurrente en las 39 entrevistas · Cliente
