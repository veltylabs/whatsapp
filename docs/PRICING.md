# Cuánto cuesta enviar avisos por WhatsApp (WhatsApp Business Platform)

> **Consultado el 2026-10-19.** No pude leer las **tarifas oficiales en pesos chilenos**: Meta las publica como archivos descargables
> en <https://developers.facebook.com/docs/whatsapp/pricing> (incluye la moneda CLP). Las cifras de abajo que no son de Meta están marcadas
> como **no verificadas**. Meta puede cambiar los precios **el primer día de cada trimestre**.

## Lo que hoy tiene la clínica y lo que falta

Hoy se usa **solo el teléfono** (la aplicación de WhatsApp Business): **no sirve** para enviar mensajes automáticos desde el sistema. Para eso hace falta la **API de WhatsApp Business (Cloud API)**, que pide:

1. Una cuenta de **Meta Business** (portafolio comercial) con un administrador, y de preferencia el negocio **verificado**.
2. Un **número de teléfono** conectado a la API. Hay dos caminos:
   - **Un número nuevo** solo para la API (el número deja de funcionar en la aplicación del teléfono).
   - **Convivencia (*coexistence*):** conectar el número que **ya está en la aplicación de WhatsApp Business** a la API y seguir usando ambos. Requiere que el número ya esté registrado en la aplicación de WhatsApp Business (no en WhatsApp normal), que no se dé de baja de la aplicación, que se use el flujo de «registro integrado» de Meta con la opción de convivencia, y una versión reciente de la aplicación. *Fuente: guías de proveedores, no la documentación de Meta; verifica los requisitos antes de empezar.*
3. **Plantillas de mensaje aprobadas por Meta.** Un aviso que el negocio **inicia** fuera de la ventana de 24 horas desde el último mensaje del destinatario **debe usar una plantilla aprobada**.

## Cómo se cobra

- Meta cobra **por mensaje entregado**, según su **categoría**: *marketing*, *utilidad*, *autenticación* y *servicio* (la conversación que inicia el cliente).
- Los avisos internos del sistema («el stock de X bajó del mínimo») son **mensajes de utilidad** con plantilla.
- Cifras **no verificadas** de una calculadora de terceros ([zernio.com](https://zernio.com/whatsapp-api-pricing)), en dólares por mensaje entregado, para Chile: **marketing ≈ US$ 0,089**; **utilidad, autenticación y servicio ≈ US$ 0,020**. Úsalas solo como orden de magnitud: son **centavos de dólar por mensaje**; con unos pocos avisos al día el gasto mensual es pequeño. Confírmalas con la tarifa oficial en CLP.
- Algunos proveedores intermedios agregan una cuota mensual o un recargo por mensaje encima de lo que cobra Meta.

## Qué hacer ahora

Nada: los avisos salen por **correo** primero (ver `veltylabs/email`). Esta página queda para decidir **cuándo** configurar la API. Cuando se decida, lo primero es descargar la tarifa oficial en CLP desde la página de precios de Meta y elegir entre número nuevo o convivencia.
