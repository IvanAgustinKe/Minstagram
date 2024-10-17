# Minstagram - Proyecto PWA Similar a Instagram

## Descripción

Minstagram es una aplicación progresiva (PWA) sencilla que simula una versión simplificada de Instagram, permitiendo a los usuarios capturar y publicar fotos con títulos. Esta aplicación tiene un diseño responsive y está optimizada para su uso en dispositivos móviles y escritorios. Incluye funcionalidades como el uso de la cámara del dispositivo, almacenamiento de las imágenes en formato Base64, y una interfaz similar a la de Instagram.

## Tecnologías Utilizadas

**HTML5 y CSS3**: Para la estructura y el diseño del proyecto, asegurando que sea visualmente atractivo y fácil de navegar.
**Bootstrap**: Para estilizar componentes y lograr un diseño más moderno y amigable. Bootstrap ayuda a hacer la aplicación responsive sin necesidad de escribir demasiado CSS personalizado.
**JavaScript**: Para manejar la lógica de la aplicación, como la captura de imágenes, el almacenamiento y la comunicación con el servidor.
**JSON Server**: Se utilizó como simulador de una API REST para almacenar los datos de las imágenes y títulos. Este fue una alternativa a MockAPI para realizar las operaciones CRUD.
**Manifest.json**: Para convertir la aplicación en una PWA, permitiendo su instalación en dispositivos.

## Estructura del Proyecto

- **index.html**: La página principal donde se visualizan todas las publicaciones en forma de un "reel".
- **camara.html**: La página donde se puede capturar una nueva imagen utilizando la cámara del dispositivo o seleccionando una imagen desde el almacenamiento local. Esta página también permite agregar un título a la imagen.
- **style.css**: Archivo CSS para la personalización de los estilos de la aplicación.
- **Manifest.json**: Archivo de configuración para que la aplicación sea reconocida como una PWA.
- **JSON Server**: Base de datos local para simular una API REST que almacene las publicaciones.
- **db.json**

## Características Principales

- **PWA Instalable**: El archivo manifest.json proporciona información sobre la aplicación, como íconos, colores y opciones de despliegue, permitiendo que los usuarios instalen Minstagram en su dispositivo.
- **Captura de Imágenes**: Utiliza un input de tipo file con la opción capture para abrir la cámara del dispositivo. Las imágenes capturadas se convierten a formato Base64.
- **Publicaciones con Título y Fecha**: Cada imagen tiene un título editable y una fecha que se actualiza cuando se modifica la publicación.
- **Editar y Eliminar Publicaciones**: Cada publicación tiene la opción de editar su título o eliminarla completamente.
- **Manejo de Conectividad**: Se bloquea el botón de "Publicar" cuando no hay conexión a Internet y se habilita nuevamente cuando se restablece.

## Uso de JSON Server

Inicialmente, se planeaba utilizar MockAPI como el servicio para manejar las publicaciones (GET y POST). Sin embargo, se descubrió que la funcionalidad de realizar operaciones POST con MockAPI requiere una suscripción paga. Por lo tanto, se optó por JSON Server, que es una solución local gratuita que nos permite simular una API REST con todas las funcionalidades CRUD (GET, POST, PUT, DELETE). Esta elección permitió desarrollar todas las funcionalidades requeridas sin restricciones, manteniendo la experiencia lo más cercana posible al uso de una API real.

## Instalación del Proyecto

1. **Clonar el Repositorio**:
    ```bash
    git clone <URL_DEL_REPOSITORIO>
    ```
2. **Instalar Dependencias**:
    Se recomienda utilizar npm para instalar JSON Server.
    ```bash
    npm install -g json-server
    ```
3. **Iniciar JSON Server**:
    JSON Server se utilizará para manejar las publicaciones.
    ```bash
    json-server --watch db.json
    ```
4. **Abrir el Proyecto**:
    Navega a `index.html` en tu navegador para comenzar a usar la aplicación.

## Funcionalidades de la Aplicación

- **Visualizar Publicaciones**: En `index.html`, se muestran todas las publicaciones almacenadas en el servidor.
- **Capturar y Publicar**: Desde `camara.html`, los usuarios pueden capturar una nueva imagen y publicarla.
- **Editar y Eliminar**: Los usuarios pueden modificar el título de una publicación o eliminarla si así lo desean.
- **Indicador de Conectividad**: El botón de "Publicar" está deshabilitado si el dispositivo no tiene conexión a Internet.


![screenshot390x790](https://github.com/user-attachments/assets/4b40d3e9-363a-4a00-99b7-31cf4573c6aa)
![screenshot660x1000](https://github.com/user-attachments/assets/30b469ae-571d-4108-8a1e-591651f41325)
![screenshot1200x840](https://github.com/user-attachments/assets/bceb900e-d7d4-4027-86ba-552f14b34d3b)
![Ejemplo2](https://github.com/user-attachments/assets/d36d2fe4-5e65-415e-aa73-97fa2b76d823)
