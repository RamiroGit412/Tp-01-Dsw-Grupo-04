
#  TP1 - Sistema de Ordenes (Desarrollo de Software)

Este proyecto es un sistema backend para la gestion de ordenes de compra. Implementa una API REST que permite registrar ordenes, consultar detalles, filtrar por estado o cliente, y actualizar su estado.

## Tecnologias utilizadas

- .NET Core (C#)
- Entity Framework Core
- SQL Server
- Swagger (para documentacion de la API)

##  Estructura del proyecto

- Controllers: logica de los endpoints
- Models: clases de dominio como Order, Product, OrderItem
- DTOs: objetos para transferencia de datos
- Data: configuracion de la base de datos y contextos
- Migrations: migraciones de EF Core

##  Funcionalidades principales

1.  Crear orden
   - POST /api/orders
   - Verifica stock y registra la orden
   - Si no hay stock suficiente, devuelve error

2.  Listar ordenes
   - GET /api/orders
   - Soporta filtros: estado, cliente, paginación

3.  Obtener orden por ID
   - GET /api/orders/{id}
   - Devuelve los detalles completos de la orden

4.  Actualizar estado
   - PUT /api/orders/{id}/status
   - Solo permite transiciones válidas entre estados

##  Requisitos previos

- Tener instalado .NET SDK
- Base de datos SQL Server funcionando
- Ejecutar migraciones:  
  ```bash
  dotnet ef database update
  ```

##  Como ejecutar

1. Clona este repositorio:
   git clone https://github.com/usuario/proyecto.git
   

2. Navega al proyecto y ejecuta:
   dotnet run

3. Abre Swagger en:
   http://localhost:5000/swagger
   
##  Capturas del funcionamiento

Ver el archivo PDF adjunto para ejemplos visuales de casos de éxito y error en cada endpoint.

##  Autor

Ramiro Alejandro Vides Gimenez – UTN FRT – Desarrollo de Software


Este sistema fue desarrollado como parte del Trabajo Práctico 1 de la materia Testing y Desarrollo de Software.
