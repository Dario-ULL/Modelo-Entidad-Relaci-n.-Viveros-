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
1. **Vivero:**
   - **Código vivero (Clave primaria):** Identificador único para cada vivero. Ejemplo: V001
   - **Nombre:** Nombre del vivero. Ejemplo: "Vivero Central"
   - **Georreferencia:** Información espacial que describe la ubicación exacta del vivero. Compuesto por:
     - **Latitud:** Coordenadas geográficas que ubican el vivero. Ejemplo: -34.603722
     - **Longitud:** Coordenadas geográficas que ubican el vivero. Ejemplo: -58.381592
2. **Zona:**

   - **Código zona (Clave primaria):** Identificador único de la zona dentro del vivero. Ejemplo: Z001
   - **Nombre:** Nombre de la zona dentro del vivero. Ejemplo: "Zona Norte"
   - **Georreferencia:** Ubicación espacial de la zona. Compuesto por: 
     - **Latitud:** Coordenadas geográficas que ubican el vivero. Ejemplo: -34.603722
     - **Longitud:** Coordenadas geográficas que ubican el vivero. Ejemplo: -58.381592
   - **Productividad (Opcional):** Un atributo relacionado con la productividad de la zona (puede estar relacionado con cultivos, rendimiento, etc.). Ejemplo: 85%
3. **Empleado:**

   - **Código empleado (Clave primaria):** Identificador único para cada empleado. Ejemplo: E123
   - **Nombre:** Nombre del empleado. Ejemplo: "Juan"
   - **Apellidos:** Apellidos de la persona. Compuesto por:
     - **Primer apellido:** Primer apellido de la persona. Ejemplo: "Pérez"
     - **Segundo apellido:** Segundo apellido de la persona. Ejemplo: "García"
   - **Fecha ingreso:** Fecha en la que el empleado comenzó a trabajar. Ejemplo: 01/03/2021
   - **DNI:** Documento de identidad del empleado. Ejemplo: 12345678
   - **Productividad (Opcional):** Medida del rendimiento del empleado. Ejemplo: 90%
4. **Cliente fidelizado:**

   - **Código cliente (Clave primaria):** Identificador único del cliente. Ejemplo: C001
   - **Nombre:** Nombre del empleado. Ejemplo: "María"
   - **Apellidos:** Apellidos de la persona. Compuesto por:
     - **Primer apellido:** Primer apellido de la persona. Ejemplo: "González"
     - **Segundo apellido:** Segundo apellido de la persona. Ejemplo: "López"
   - **Email:** Correo electrónico del cliente. Ejemplo: "maria.gonzalez@example.com"
   - **Teléfono:** Número de contacto. Ejemplo: 555123456
   - **Fecha registro:** Fecha en la que el cliente se registró. Ejemplo: 05/07/2022
   - **Compra total:** Monto total acumulado por las compras del cliente. Ejemplo: $2,500
   - **Bonificación:** Información sobre las bonificaciones obtenidas. Ejemplo: 5%
5. **Producto:**

   - **Código producto (Clave primaria):** Identificador único del producto. Ejemplo: P001
   - **Nombre:** Nombre del producto. Ejemplo: "Planta de Rosas"
   - **Precio:** Precio unitario del producto. Ejemplo: $20
   - **Descripción:** Descripción del producto. Ejemplo: "Planta de rosa roja"
6. **Pedido:**

   - **Código pedido (Clave primaria):** Identificador único del pedido. Ejemplo: O001
   - **Fecha:** Fecha en la que se realizó el pedido. Ejemplo: 10/10/2024
## 3. Descripción de cada una de las relaciones definidas y sus cardinalidades
## 4. Restricciones semánticas
