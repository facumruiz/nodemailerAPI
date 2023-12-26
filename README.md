# Proyecto de Envío de Correos con Express y Nodemailer

Este proyecto utiliza Node.js con Express para crear un servidor que gestiona el envío de correos electrónicos a través de la librería Nodemailer. Además, hace uso de `multiparty` para procesar formularios y `cors` para habilitar el intercambio de recursos entre diferentes orígenes.

## Requisitos previos

- **Node.js**: Asegúrate de tener Node.js instalado en tu máquina.
- **Variables de entorno**: El proyecto utiliza variables de entorno para configurar el correo electrónico y la contraseña. Asegúrate de tener un archivo `.env` con las siguientes variables: `PORT`, `EMAIL`, y `PASS`.
- **Servicio de correo**: Utiliza una cuenta de Gmail o el servicio de correo correspondiente para enviar los correos.

## Tecnologías principales utilizadas

- **Express**: Utilizado para configurar el servidor y definir rutas.
- **Nodemailer**: Librería de Node.js para enviar correos electrónicos.
- **Cors**: Middleware para permitir las solicitudes de diferentes dominios.
- **Multiparty**: Utilizado para analizar formularios multipartes.

## Configuración del proyecto

1. **Instalación de dependencias**: Ejecuta `npm install` para instalar todas las dependencias necesarias.
2. **Variables de entorno**: Crea un archivo `.env` y define las variables `PORT`, `EMAIL` y `PASS` con los valores correspondientes.
3. **Servicio de correo**: Asegúrate de permitir el acceso de aplicaciones menos seguras si utilizas Gmail u otorga los permisos necesarios para el servicio de correo que utilices.

## Estructura del proyecto

- **`app.js`**: El archivo principal que configura el servidor Express y gestiona el envío de correos.
- **`/public`**: Directorio que contiene archivos estáticos, como la página HTML para el formulario de contacto.

## Configuración del servidor

El servidor se configura en el puerto definido por la variable de entorno `PORT`. Se establece una conexión con el servicio de correo utilizando Nodemailer, verificando la configuración para asegurarse de que esté lista para enviar correos.

El endpoint `/send` se encarga de recibir los datos del formulario, procesarlos y enviar un correo electrónico al destinatario configurado.

## Ejecución del proyecto

Para ejecutar el proyecto:

1. Ejecuta `npm start` en la terminal para iniciar el servidor.
2. Accede a la ruta `http://localhost:PORT` en tu navegador para utilizar el formulario de contacto.
