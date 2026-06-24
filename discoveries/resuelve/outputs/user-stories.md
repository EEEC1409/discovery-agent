# User Stories — APP Resuelve (MVP)

> **Discovery:** `resuelve`
> **Persona central:** Cliente de tarjeta Resuelve (`primera mano`)
> **Criterio de priorización:** se incluyen solo las historias que cubren el núcleo
> de valor — poder ingresar a la APP, ver el estado de crédito y usar el programa
> de puntos. El resto queda marcado como "fuera del MVP v1" en el Canvas.

---

## Bloque 1 — Identidad y acceso

- **[US-01]** Como cliente, quiero ingresar mi número de cédula para que la APP
  determine si soy cliente Resuelve y me indique qué flujo debo seguir
  (pre-aprobado, nuevo, en revisión, no califica), para no tener que llamar y
  descubrir mi situación por teléfono.
  - Criterios de aceptación:
    - Dado que abro la APP por primera vez, cuando ingreso mi cédula y presiono
      continuar, entonces la APP consulta el sistema y me muestra la pantalla
      correspondiente a mi estado en menos de 3 segundos.
    - Dado que mi cédula no está en la base de datos de Resuelve, cuando la ingreso,
      entonces veo un mensaje claro que indica que no tengo oferta disponible y qué
      alternativa tengo.
    - Dado que la conexión falla durante la consulta, cuando intento continuar,
      entonces veo un mensaje de error de conectividad accionable.
  - Fuente: `Entrevistas_APP_Resuelve.md` (US-002, US-004, US-036)

---

- **[US-02]** Como cliente nuevo (no registrado en la APP), quiero ingresar mis
  datos personales, validar un código OTP enviado a mi correo y crear una
  contraseña, para tener una cuenta de autoservicio en la APP Resuelve.
  - Criterios de aceptación:
    - Dado que soy cliente nuevo, cuando completo nombre, teléfono y correo y
      presiono continuar, entonces el sistema envía un OTP a mi correo en menos
      de 60 segundos.
    - Dado que ingreso el OTP correcto, cuando presiono validar, entonces la APP
      me permite crear mi contraseña y registra mi cuenta en todos los sistemas
      integrados.
    - Dado que el OTP es incorrecto o expira, cuando lo ingreso, entonces recibo
      un mensaje de error claro con la opción de reenviar el código.
    - Dado que el registro falla por un error de sistema, entonces veo un mensaje
      accionable que me indica qué hacer.
  - Fuente: `Entrevistas_APP_Resuelve.md` (US-007, US-008, US-009, US-010, US-011)

---

- **[US-03]** Como cliente registrado, quiero iniciar sesión con mi cédula y
  contraseña para acceder a mi información de crédito de forma rápida y segura.
  - Criterios de aceptación:
    - Dado que tengo cuenta registrada, cuando ingreso cédula y contraseña
      correctas, entonces accedo al dashboard en menos de 3 segundos.
    - Dado que ingreso credenciales incorrectas, cuando presiono ingresar, entonces
      veo un mensaje de error que no revela si el fallo fue en la cédula o la
      contraseña (seguridad).
    - Dado que no recuerdo mi contraseña, cuando presiono "¿Olvidé mi contraseña?",
      entonces el sistema inicia el flujo de recuperación por correo.
  - Fuente: `Entrevistas_APP_Resuelve.md` (US-012, US-014)

---

- **[US-04]** Como cliente que olvidó su contraseña, quiero solicitar un enlace
  de recuperación a mi correo registrado para recuperar el acceso a mi cuenta
  sin necesidad de crear una cuenta nueva.
  - Criterios de aceptación:
    - Dado que presioné "Olvidé mi contraseña", cuando ingreso mi correo
      registrado, entonces recibo un enlace de recuperación en menos de 2 minutos.
    - Dado que el enlace es válido, cuando accedo y creo una nueva contraseña,
      entonces puedo iniciar sesión con la nueva contraseña inmediatamente.
    - Dado que el correo no está registrado, cuando lo ingreso, entonces recibo
      un mensaje que indica que no hay cuenta asociada.
  - Fuente: `Entrevistas_APP_Resuelve.md` (US-014)

---

## Bloque 2 — Estado de cuenta y crédito

- **[US-05]** Como cliente, quiero ver un dashboard con saludo personalizado y el
  resumen de mi crédito (cuota al cobro, cuota consumida, fecha mínima de pago)
  al ingresar a la APP, para tener una visión inmediata de mi situación financiera
  sin tener que buscar en varios menús.
  - Criterios de aceptación:
    - Dado que inicio sesión correctamente, cuando llego al dashboard, entonces
      veo mi nombre, la cuota al cobro del mes en curso, la cuota consumida y la
      fecha límite de pago.
    - Dado que mi línea de crédito está inactiva, cuando accedo al dashboard,
      entonces veo mi capacidad de pago disponible y una acción clara para activar
      mi línea.
    - Dado que tengo una solicitud en proceso, cuando accedo, entonces veo el
      estado actual de la solicitud.
  - Fuente: `Entrevistas_APP_Resuelve.md` (US-005, US-006, US-016, US-018)

---

- **[US-06]** Como cliente, quiero ver el historial de mis movimientos (consumos
  y notas de crédito) para llevar control de mis compras y verificar cargos.
  - Criterios de aceptación:
    - Dado que estoy en el dashboard o estado de cuenta, cuando accedo a
      "Movimientos", entonces veo la lista de transacciones con fecha, descripción
      y monto, ordenadas de más reciente a más antigua.
    - Dado que no hay movimientos en el período, cuando accedo a la sección,
      entonces veo un mensaje que lo indica claramente.
  - Fuente: `Entrevistas_APP_Resuelve.md` (US-021)

---

## Bloque 3 — Programa de puntos y canje

- **[US-07]** Como cliente, quiero ver mi saldo de puntos vigentes e historial de
  puntos recibidos y redimidos, para saber cuántos puntos tengo disponibles y
  hacer seguimiento de mis recompensas.
  - Criterios de aceptación:
    - Dado que estoy autenticado, cuando accedo a la sección de puntos, entonces
      veo el saldo de puntos vigentes destacado y el historial detallado (fecha,
      tipo — recibido/redimido — y cantidad).
    - Dado que nunca he acumulado puntos, cuando accedo, entonces veo el saldo en
      cero y un mensaje que explica cómo ganar puntos.
  - Fuente: `Entrevistas_APP_Resuelve.md` (US-022, US-023)

---

- **[US-08]** Como cliente con puntos acumulados, quiero explorar el catálogo de
  productos disponibles, ver el detalle de un producto, usar mis puntos para reducir
  la cuota, confirmar mi dirección de entrega y completar el canje, para aprovechar
  el beneficio de mi fidelidad.
  - Criterios de aceptación:
    - Dado que tengo puntos suficientes, cuando selecciono un producto del catálogo,
      entonces veo su descripción, puntos requeridos, cuota mensual y la opción
      de usar puntos para reducirla.
    - Dado que presiono "Canjear", cuando el sistema valida mi elegibilidad en
      tiempo real, entonces puedo confirmar o modificar mi dirección de entrega y
      autorizar el canje.
    - Dado que el canje se registra exitosamente, entonces recibo confirmación
      visual dentro de la APP y por correo electrónico.
    - Dado que no cumplo los requisitos de elegibilidad, cuando intento canjear,
      entonces veo el motivo específico del rechazo y las acciones disponibles.
    - Dado que no tengo puntos suficientes para un producto, cuando lo veo en el
      catálogo, entonces ese producto aparece como no disponible con el déficit
      indicado.
  - Fuente: `Entrevistas_APP_Resuelve.md` (US-024, US-025, US-026, US-027, US-028, US-030, US-031)

---

## Bloque 4 — Perfil y seguridad

- **[US-09]** Como cliente autenticado, quiero ver toda mi información personal en
  un solo lugar y cambiar mi contraseña desde Mi Perfil sin cerrar sesión, para
  mantener mis datos actualizados.
  - Criterios de aceptación:
    - Dado que accedo a Mi Perfil, entonces veo nombre, cédula, teléfono y correo
      en una sola pantalla.
    - Dado que presiono "Cambiar contraseña", cuando ingreso la contraseña actual
      y la nueva (con confirmación), entonces la contraseña se actualiza y recibo
      confirmación sin necesidad de cerrar sesión.
    - Dado que la contraseña actual ingresada es incorrecta, entonces veo un
      mensaje de error y no se realiza ningún cambio.
  - Fuente: `Entrevistas_APP_Resuelve.md` (US-032, US-033)

---

- **[US-10]** Como cliente, quiero poder cerrar sesión desde cualquier pantalla y
  que la APP me notifique cuando mi sesión expire para proteger mi información en
  dispositivos compartidos.
  - Criterios de aceptación:
    - Dado que estoy en cualquier pantalla de la APP, cuando presiono "Cerrar
      sesión", entonces se cierra la sesión y soy redirigido a la pantalla de
      ingreso de cédula.
    - Dado que mi sesión expira por inactividad, cuando intento navegar a cualquier
      pantalla protegida, entonces veo un mensaje que informa la expiración y soy
      redirigido al login.
  - Fuente: `Entrevistas_APP_Resuelve.md` (US-015, US-035)

---

## Bloque 5 — Pre-aprobado (acceso rápido a crédito)

- **[US-11]** Como cliente pre-aprobado, quiero ver mi oferta de línea de crédito
  y poder continuar la solicitud desde la APP en 3 pasos simples, para no tener
  que ir a una sucursal.
  - Criterios de aceptación:
    - Dado que la APP identifica mi cédula como pre-aprobada, cuando veo mi oferta,
      entonces esta muestra el monto de la línea de crédito claramente.
    - Dado que presiono "Continuar solicitud", cuando completo los 3 pasos del
      flujo, entonces la solicitud queda registrada y recibo confirmación.
    - Dado que abandono el flujo antes de completarlo, cuando vuelvo a la APP,
      entonces puedo retomar desde donde lo dejé.
  - Fuente: `Entrevistas_APP_Resuelve.md` (US-003)
