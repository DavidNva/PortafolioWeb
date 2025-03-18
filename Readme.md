# Integración de PayPal en ASP.NET MVC

Este proyecto proporciona una guía paso a paso para integrar PayPal en una aplicación ASP.NET MVC (.NET Framework 4.7.2). La integración permite procesar pagos a través de la API REST de PayPal y puede ser utilizada en proyectos de comercio electrónico, plataformas de donaciones u otros sistemas que requieran pagos en línea.

---

## 🚀 Requisitos

Antes de comenzar, asegúrate de contar con lo siguiente:

- Visual Studio 2019 o superior
- .NET Framework 4.7.2
- Cuenta de desarrollador en [PayPal Developer](https://developer.paypal.com/){:target="_blank"}
- Postman (opcional, para probar llamadas a la API de PayPal)

---

## 🔑 Configuración de Credenciales en PayPal

Para integrar PayPal en tu aplicación, debes generar credenciales API siguiendo estos pasos:

1. **Registrarse en PayPal Developer**
   - Accede a [PayPal Developer](https://developer.paypal.com/){:target="_blank"}.
   - Inicia sesión o crea una cuenta si aún no la tienes.

2. **Crear una aplicación de prueba**
   - Dirígete a **Dashboard > My Apps & Credentials**.
   - Selecciona **Sandbox** y haz clic en **Create App**.
   - Asigna un nombre a la aplicación y selecciona la cuenta de negocio.
   - Guarda el **Client ID** y **Secret**, ya que los necesitarás más adelante.

3. **Configurar Webhooks (Opcional)**
   - En la misma sección de **My Apps & Credentials**, puedes agregar webhooks para recibir notificaciones sobre pagos completados.

---

## 🏗️ Instalación del Proyecto

1. **Clonar el repositorio**
   ```bash
   git clone https://github.com/tu-repo/paypal-integration-mvc.git
   cd paypal-integration-mvc
   ```

2. **Abrir el proyecto en Visual Studio**
   - Abre el archivo `PaypalIntegration.sln` en Visual Studio.

3. **Configurar credenciales de PayPal**
   - En el archivo `appsettings.json` o `Web.config`, agrega las credenciales obtenidas en PayPal:
     ```json
     {
       "PayPal":