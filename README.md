
![backend_API](https://github.com/user-attachments/assets/035e3342-2a18-4e85-bfb6-ea58e9e932dc)

# Proyecto Backend con Express y MongoDB

Este es un proyecto backend desarrollado con Node.js, Express y MongoDB. Proporciona una API para manejar productos, usuarios y carritos de compra. Los productos y usuarios se almacenan en una base de datos MongoDB. El backend permite la gestión completa de productos y usuarios, así como la funcionalidad de un carrito de compra, que se asocia a cada usuario.

## Contenidos

- [Instalación](#instalación)
- [Configuración](#configuración)
- [Uso](#uso)
- [Endpoints](#endpoints)
- [Contribución](#contribución)
- [Licencia](#licencia)

## Instalación

1. Clona el repositorio:
   ```bash
   git clone 
   cd 

2. Instala las dependencias:
   ```bash
   npm install

3. Asegúrate de tener MongoDB instalado y en ejecución en tu máquina local o en un servicio de MongoDB en la nube.


## Configuración

1. Crea un archivo .env en la raíz del proyecto , el contenido esta incluido en el archivo example.env
2. Reemplaza todas las variables con el nombre de tus variables.

## Uso

1. Inicia el servidor
    ```bash
    npm start

2. La API estará disponible en http://localhost:3000.

## Endpoints

Autenticación
POST /auth/login: Inicia sesión de un usuario.
Cuerpo de la solicitud:
json
Copiar código
{
  "email": "email@ejemplo.com",
  "password": "tu_contraseña"
}
Usuarios
GET /usuarios: Obtiene todos los usuarios.
GET /usuarios/
: Obtiene un usuario por ID.
POST /usuarios: Crea un nuevo usuario.
Cuerpo de la solicitud:
json
Copiar código
{
  "nombre": "Nombre del Usuario",
  "email": "email@ejemplo.com",
  "password": "tu_contraseña"
}
PUT /usuarios/
: Actualiza un usuario por ID.
Cuerpo de la solicitud:
json
Copiar código
{
  "nombre": "Nombre Actualizado",
  "email": "email@ejemplo.com",
  "password": "tu_contraseña_actualizada"
}
DELETE /usuarios/
: Elimina un usuario por ID.
Productos
GET /productos: Obtiene todos los productos.
GET /productos/
: Obtiene un producto por ID.
POST /productos: Crea un nuevo producto.
Cuerpo de la solicitud:
json
Copiar código
{
  "nombre": "Nombre del Producto",
  "descripcion": "Descripción del Producto",
  "precio": 100,
  "stock": 50
}
PUT /productos/
: Actualiza un producto por ID.
Cuerpo de la solicitud:
json
Copiar código
{
  "nombre": "Nombre Actualizado",
  "descripcion": "Descripción Actualizada",
  "precio": 150,
  "stock": 30
}
DELETE /productos/
: Elimina un producto por ID.
Carrito
GET /cart/
: Obtiene el carrito de un usuario por ID de usuario.
POST /cart/
: Añade un producto al carrito de un usuario.
Cuerpo de la solicitud:
json
Copiar código
{
  "productoId": "id_del_producto",
  "cantidad": 2
}
DELETE /cart/
/
: Elimina un producto del carrito de un usuario.
POST /cart/
/checkout: Finaliza la compra del carrito de un usuario y registra la compra.

  
