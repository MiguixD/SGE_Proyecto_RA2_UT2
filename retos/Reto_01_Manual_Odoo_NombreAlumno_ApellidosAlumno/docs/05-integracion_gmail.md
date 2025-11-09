# 05 — Integración con Gmail

## Requisitos
- Cuenta Google Cloud (GCP).

## Pasos resumidos

1. **Activar plugin de correo**

Lo primero que tenemos que hacer es activar el plugin de correo desde Odoo. Para esto nos vamos a la pestaña de ajustes generales que hemos visto antes, bajamos a la sección de integraciones y marcamos la casilla de Plugin de correo. Le damos a guardar cambios en la esquina superior izquierda.  

![Activar plugin de correo](../assets/img/05-integracion_gmail/paso01_activar-plugin-correo.png)  

Ahora vamos a ir a nuestro correo electrónico, una vez dentro en la barra que sale a la derecho le damos al más y buscamos la aplicación Odoo Inbox Addin.  

![Instalar apps google](../assets/img/05-integracion_gmail/paso02_instalar-apps-correo.png)  

![Instalar Odoo Inbox Addin](../assets/img/05-integracion_gmail/paso03_instalar-odoo-inbox-addin.png)  

Podemos abrir esta aplicación de gmail cuando tenemos un correo abierto y nos saldrá un botón de login. Lo pulsamos, introducimos la URL de nuestra base de datos e iniciamos sesión.  

![Inicio sesión Odoo Inbox Addin](../assets/img/05-integracion_gmail/paso04_inicio-sesion-odoo-inbox-addin.png)  

Con este plugin podremos ver información sobre la empresa que nos manda correos electrónicos.  

2. **Vincular con gmail**

Vamos a los ajustes generales, sección de integraciones y activamos Autenticación OAuth. Le damos a guardar cambios.  

![Activar OAuth](../assets/img/05-integracion_gmail/paso05_activar-oauth.png)  

Abrimos esta opción y seleccionamos Google OAuth2, vamos a necesitar una ID de cliente, para esto iremos a la Google Cloud Console.  

![Google OAuth](../assets/img/05-integracion_gmail/paso06_google-oauth.png)  

Dentro de Google Cloud Console buscamos Gmail API. Le damos a Habilitar  

![Gmail API](../assets/img/05-integracion_gmail/paso07_buscar-gmail-api.png)  

Una vez habilitada le damos a crear credenciales.  

![Crear credenciales](../assets/img/05-integracion_gmail/paso08_crear-credenciales.png)  

Le damos a Datos de los usuarios y siguiente.  

![Crear credenciales 01](../assets/img/05-integracion_gmail/paso09_crear-credenciales-01.png)  

Como nombre de aplicación ponemos odoo-email, introducimos nuestro correo y siguiente.  

![Crear credenciales 02](../assets/img/05-integracion_gmail/paso10_crear-credenciales-02.png)  

En agregar o quitar permisos buscamos gmail y marcamos los que sean necesarios, como por ejemplo leer correos o enviar correos a tu nombre, le damos a actualizar y continuar.  

![Crear credenciales 03](../assets/img/05-integracion_gmail/paso11_crear-credenciales-03.png)  

Seleccionamos aplicacion web, de nombre ponemos nuevamente odoo-email y en URLs de redireccionamiento autorizados ponemos la url de nuestro Odoo con el añadido /google_gmail/confirm.  

![Crear credenciales 04](../assets/img/05-integracion_gmail/paso12_crear-credenciales-04.png)  

Si ahora vamos a la pantalla de credenciales y seleccionamos la cuenta que hemos creado podremos ver y copiar nuestro Cliente ID y nuestro secreto de cliente.  

![Copiar Client ID](../assets/img/05-integracion_gmail/paso13_copiar-client-id.png)  

Ahora volvemos a Odoo, pegamos la ID del cliente y marcamos la casilla Permitido y le damos a guardar cambios.  

![Pegar Client ID](../assets/img/05-integracion_gmail/paso14_pegar-client-id.png)  

Si vamos a ajustes generales, en el apartado de Correos electrónicos, si tenemos marcada la opción Utilizar servidores de correo electrónico personalizados nos saldrá una nueva opción: Usar un servidor de Gmail. Aqui tenemos que poner nuestro ID y secreto de cliente.  

![Usar servidor gmail](../assets/img/05-integracion_gmail/paso15_usar-servidor-gmail.png)  

De esta forma el correo electrónico ya está vinculado a Odoo y podemos manejarlo desde dentro de Odoo.  
