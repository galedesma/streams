# Streams - Frontend

## Descripción

SPA (Single Page Application) cuyo frontend fue desarrollado en React, a partir de las siguientes unidades del curso Modern React with Redux, de Stephen Grider en Udemy:

- 20 Navigation with React Router

- 21 Handling Authentication with React

- 22 Redux Dev Tools

- 23 Handling Forms with Redux Form

- 24 REST Based React Apps

- 25 Using React Portals

- 26 Implementing Streaming Video

### client

Se usa react-router-dom para manejar la navegación dentro de la página. Al hacer clic en cualquier link dentro de la página, se renderizan los componentes correspondientes a la ruta mientras de ocultan los que no, y se cambia el contenido de la barra de dirección.

El manejo del state de la aplicación se realiza con Redux y varias dependencias asociadas como Redux-Thunk, React-Redux, Redux-Form.

Se implementa autenticación del usuario a través de Google OAuth. Al hacer clic en el botón de inicio de sesión en el header, aparecerá un pop-up de confirmación por parte de Google para que el usuario acepte compartir su id de usuario de Google. Luego, dicho id será asociado a los streams que el usuario cree, para luego poder editarlos o borrarlos.

Toda la información relacionada a los streams creados es almacenada en una base de datos en MongoDB, conectado al backend de esta aplicación, el cual se conecta con el frontend mediante axios. De esta forma se puede realizar y enviar pedidos a nuestra base de datos desde el frontend.

Para más información del backend de este proyecto, dirigirse a: [streams-backend](https://github.com/galedesma/streams-backend)

### rtmp

Contiene los archivos de configuración necesarios para poder transmitir hacia la app. El usuario hará uso de Node-Media-Server para crear un servidor RTMP (Real Time Media Protocol) local, para luego configurar su software de grabación y transmisión de video de preferencia (se recomienda [OBS](https://obsproject.com/es)) correspondientemente.

## [Ir a la app](https://streams-galedesma.netlify.app)