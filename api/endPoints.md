# Endpoints de la API

Nuestra API utiliza los principales métodos HTTP para interactuar con los recursos: `GET`, `POST`, `PUT`, `PATCH` y `DELETE`. Las rutas están organizadas por módulos funcionales, cada uno implementando las operaciones CRUD correspondientes.

---

## Convenciones Generales

### Métodos HTTP

| Método     | Propósito                                       | Idempotente |
| :--------- | :---------------------------------------------- | :---------: |
| `GET`      | Obtener datos del servidor                      |     Sí      |
| `POST`     | Enviar nuevos datos al servidor                 |     No      |
| `PUT`      | Reemplazar completamente un recurso existente   |     Sí      |
| `PATCH`    | Actualizar parcialmente un recurso existente    |     No      |
| `DELETE`   | Eliminar un recurso existente                   |     Sí      |



## Autenticación (`/api/auth`)

| Método | Endpoint                     | Descripción             | 
| :----- | :--------------------------- | :-----------------------|
| POST   | `/auth/register`             | Registrar nuevo cliente |  
| POST   | `/auth/login`                | Iniciar sesión          | 


---

## Cliente (`/api/cliente`)

| Método | Endpoint                   | Descripción                        | 
| :----- | :------------------------- | :----------------------------------|
| GET    | `/cliente/:id`         | Obtener perfil del cliente             |
| PUT    | `/cliente/id`          | Actualizar perfil del cliente actual   |
| GET    | `/cliente/count`       | Cuenta el total de clientes registrados|
| GET    | `/cliente/serch`       | Obterne cliente por descripcion Parcial|

---

## Producto (`/api/producto`)

| Método | Endpoint                                        | Descripción                              | 
| :----- | :---------------------------------------------  | :--------------------------------------- |
| GET    | `/producto`                                     | Obtener todos los productos disponibles      |   
| GET    | `/producto/stockTotal`                          | Obtener stock total del supermercado     | 
| GET    | `/producto/searchCat`                           | Obtener producto por categoria           |  
| GET    | `/producto/search`                              | Obtener producto por descripcion parcial |
| GET    | `/producto/:id`                                 | Obtener detalles de un producto          | 
| POST   | `/producto`                                     | Crear nuevo producto                     | 
| PUT    | `/producto/:id`                                 | Actualizar producto                      | 
| DELETE | `/producto/:id`                                 | Eliminar producto                        | 
| POST   | `/producto/imagen`                              | Actualizar imagen del producto           |

---

## Venta (`/api/venta`)

| Método | Endpoint              | Descripción                            
| :----- | :-------------------- | :-----------------------------|
| GET    | `/venta`              | Obtener todas las ventas      |
| GET    | `/venta/:id`          | Obtener detalles de una venta |
| POST   | `/procesarCompra`     | Crea la venta                 |
| PUT    | `/venta/:id`          | Actualizar estado de la venta |

---

## Distribuidor (`/api/distribuidor`)

| Método | Endpoint                     | Descripción                        | 
| :----- | :--------------------------- | :--------------------------------- |
| GET    | `/distribuidor`              | Obtener todos los distribuidores   |  
| GET    | `/distribuidor/:id`          | Obtener detalles del distribuidor  | 
| GET    | `/distribuidor/zona/:zonaId` | Obtener distribuidor por zona      |
| PUT    | `/distribuidor/:id`          | Actualizar distribuidor            | 
| DELETE | `/distribuidor/:id`          | Eliminar distribuidor              | 

---

## Zona (`/api/zona`)

| Método | Endpoint        | Descripción                             | 
| :----- | :-------------- | :---------------------------------------|
| GET    | `/zona`         | Obtener todas las zona                  |   
| GET    | `/zona/serch`   | Obtener zonas por descripcion parcial   |   
| GET    | `/zona/:id`     | Obtener detalles de la zona             |   
| POST   | `/zona`         | Crear nueva zona                        |  
| PUT    | `/zona/:id`     | Actualizar zona                         |
| DELETE | `/zona/:id`     | Eliminar zona                           | 

---

## Categoria de productos (`/api/categoria`)

| Método | Endpoint              | Descripción                              | 
| :----- | :------------------ | :------------------------------------------| 
| GET    | `/categoria`        | Obtener todas las categorias               |  
| GET    | `/categoria/:id`    | Obtener detalles de la categoria           | 
| GET    | `/categoria/search` | Obtener Categorias por descripcion parcial |   
| POST   | `/categoria`        | Crear nueva categoria                      |
| PUT    | `/categoria/:id`    | Actualizar categoria                       |
| DELETE | `/categoria/:id`    | Eliminar categoria                         | 

---

## item-venta (`/api/item-venta`)

| Método | Endpoint         | Descripción                      |
| :----- | :------------------ | :---------------------------- | 
| GET    | `/item-venta`       | Obtener todos los items       |    
| GET    | `/item-venta/:id`   | Obtener detalles de una item  |  
| POST   | `/item-venta`       | Crear item                    |  
| PUT    | `/item-venta/:id`   | Actualizar item               | 
| DELETE | `/item-venta/:id`   | Eliminar item                 | 

---

## MercadoPago (`/api/mercadopago`)

| Método | Endpoint                        | Descripción                | 
| :----- | :------------------------------ | :--------------------------| 
| POST   | `/mercadopago/create-preference`| Crear orden de pago        | 
| GET    | `/mercadopago//success`         | Verificar estado del pago  |  

---
