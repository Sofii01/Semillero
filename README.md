# Ecosistema - Directorio de impacto
Fue propuesto por  [Semillero Latam](https://www.linkedin.com/company/semillero-latam/) y se desarrollo en forma conjunta en equipo a lo largo de 4 sprint que duro la experiencia. Se trata de una pagina que ayuda a emprendedores a conectar con personas interesadas en sus productos/servicios por su localizacion. Se muestra informacion del proveedor mas cercano como su facebook, instagram, etc. Un administrador puede gestionar sus publicacion y a los proveedores. El login se realiza mediante autenticacion de la cuenta de Google.
Utilizamos: OAuth 2.0, JWT, Java Mail Sender, Geocoding, Cloudinary.

Nota: Para poder probarla va a tener que crear algunos proveedores y publicaciones.

## Configuraciones Generales

### Requisitos Previos para el back

- JDK (Java Development Kit) versión 17.x o superior.
- Maven versión 3.9.x o superior.

### Configuración del Entorno: Variables de entorno

Para facilitar la configuración del proyecto y garantizar que cada desarrollador tenga una configuración consistente, se establece la práctica de utilizar un archivo de variables de entorno. Este archivo se crea a partir de un archivo de ejemplo llamado .env.example.

1. Crear el Archivo .env a partir del .env.example
2. Una vez creado el archivo .env, es importante revisar y modificar cada variable de entorno según sea necesario.
3. El archivo .env ya está ignorado en el .gitignore
Y agregar al .env lo siguiente:
```
CLIENT_SECRET=
CLIENT_ID=
REDIRECT_URI=
CLOUDINARY_URL=
CLOUDINARY_CLOUD_NAME=
CLOUDINARY_API_KEY=
CLOUDINARY_API_SECRET=
MAIL_USERNAME=
MAIL_PASSWORD=
GOOGLE_MAPS_API_KEY=
```
#### Para modificar el OAuth 2.0
Detalles y Pasos de Configuración:
1. Crear un Proyecto en Google Cloud Platform: Ve a [Google Cloud Platform ](https://console.cloud.google.com/projectselector2/apis/dashboard?supportedpurview=project)
Crea un nuevo proyecto y asígnale un nombre.

2. Configurar el OAuth 2.0 Consentimiento:
En el menú lateral, ve a "APIs & Services" > "OAuth consent screen".
Completa la información requerida, como el nombre de la aplicación, el email de soporte y los dominios autorizados.

3. Crear Credenciales:
Ve a "APIs & Services" > "Credentials".
Crea nuevas credenciales de OAuth 2.0 Client ID.
Configura las credenciales para la aplicación web e ingresa las URIs de redireccionamiento autorizadas.

4. Integrar Google OAuth en la Aplicación:
Copia el Client ID y el Client Secret generados.
Integra estos valores en la configuración de tu aplicación para establecer la conexión con Google OAuth.

#### Configuración de la Cuenta en Cloudinary:
Crea una cuenta en Cloudinary y configura las credenciales necesarias para la autenticación segura.

#### Configuración de Mail
En la cuenta de google buscar "Verificacion en 2 pasos" y crear una "Contraseña de aplicación", para agregarla como password.

Configuracion Geocoding
Seguir los pasos de [google](https://developers.google.com/maps/documentation/geocoding/cloud-setup?hl=es-419)

### Configuracion para el front
1. Instala las dependencias: npm install
2. Ejecutar con npm run dev. 
3. URL utilizada: http://localhost:5173

