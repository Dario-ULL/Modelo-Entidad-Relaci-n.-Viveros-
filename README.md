# Modelo-Entidad-Relacion-Viveros
### Integrantes del grupo: Darío Domínguez González y Lihao Shu
## 1. Descripción de cada una de las entidades definidas
1. **Viveros:**
2. **Zona:**
3. **Empleado:**
4. **Producto:**
5. **Pedido:**
6. **Cliente fidelizado:**
## 2. Descripción y ejemplos ilustrativos del dominio de cada uno de los atributos de las entidades
1. Vivero:

Atributos:
Código vivero (Clave primaria): Identificador único para cada vivero.
Nombre: Nombre del vivero.
Latitud y Longitud: Coordenadas geográficas que ubican el vivero.
Georreferencia: Información espacial que describe la ubicación exacta del vivero.
Ejemplo:
Código vivero: V001
Nombre: "Vivero Central"
Latitud: -34.603722
Longitud: -58.381592
Georreferencia: (34.603722, -58.381592)
Zona:

Atributos:
Código zona (Clave primaria): Identificador único de la zona dentro del vivero.
Nombre: Nombre de la zona dentro del vivero.
Latitud y Longitud: Coordenadas específicas de la zona.
Georreferencia: Ubicación espacial de la zona.
Productividad (Opcional): Un atributo relacionado con la productividad de la zona (puede estar relacionado con cultivos, rendimiento, etc.).
Ejemplo:
Código zona: Z001
Nombre: "Zona Norte"
Latitud: -34.603000
Longitud: -58.380000
Georreferencia: (34.603000, -58.380000)
Productividad: 85%
Empleado:

Atributos:
Código empleado (Clave primaria): Identificador único para cada empleado.
Nombre, Primer apellido, Segundo apellido: Datos del empleado.
Fecha ingreso: Fecha en la que el empleado comenzó a trabajar.
DNI: Documento de identidad del empleado.
Productividad (Opcional): Medida del rendimiento del empleado.
Ejemplo:
Código empleado: E123
Nombre: "Juan"
Primer apellido: "Pérez"
Segundo apellido: "García"
Fecha ingreso: 01/03/2021
DNI: 12345678
Productividad: 90%
Cliente fidelizado:

Atributos:
Código cliente (Clave primaria): Identificador único del cliente.
Nombre, Primer apellido, Segundo apellido: Datos del cliente.
Email: Correo electrónico del cliente.
Teléfono: Número de contacto.
Fecha registro: Fecha en la que el cliente se registró.
Compra total: Monto total acumulado por las compras del cliente.
Bonificación: Información sobre las bonificaciones obtenidas.
Ejemplo:
Código cliente: C001
Nombre: "María"
Primer apellido: "González"
Segundo apellido: "López"
Email: "maria.gonzalez@example.com"
Teléfono: 555123456
Fecha registro: 05/07/2022
Compra total: $2,500
Bonificación: 5%
Producto:

Atributos:
Código producto (Clave primaria): Identificador único del producto.
Nombre: Nombre del producto.
Precio: Precio unitario del producto.
Descripción: Descripción del producto.
Stock: Cantidad disponible del producto.
Ejemplo:
Código producto: P001
Nombre: "Planta de Rosas"
Precio: $20
Descripción: "Planta de rosa roja"
Stock: 150 unidades
Pedido:

Atributos:
Código pedido (Clave primaria): Identificador único del pedido.
Fecha: Fecha en la que se realizó el pedido.
Ejemplo:
Código pedido: O001
Fecha: 10/10/2024
Tarea:

Atributos: No parece tener atributos definidos directamente en el diagrama, pero probablemente se refiere a las tareas que realizan los empleados en la zona.
Ejemplo:
Una tarea podría ser "Plantar semillas".
## 3. Descripción de cada una de las relaciones definidas y sus cardinalidades
## 4. Restricciones semánticas
