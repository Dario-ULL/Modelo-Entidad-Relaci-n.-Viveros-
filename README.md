# Modelo-Entidad-Relacion-Viveros
### Integrantes del grupo: Darío Domínguez González y Lihao Zhu
## 1. Descripción de cada una de las entidades definidas
1. **Viveros:** Entidad que representa los viveros que disponen en una Tajinaste S.A.
2. **Zona:** Entidad que representa las diferentes zonas que existen dentro de un mismo vivero.
3. **Empleado:** Persona que trabaja para la empreza en un vivero.
4. **Producto:** Entidad que representa todos los vienenes o servicios que ofrece la Tajinaste S.A.
5. **Pedido:** Entidad que representa la informacion de los pedidos realizados por los clientes.
6. **Cliente fidelizado:** Clasificacion de todos los clientes afiliados.
## 2. Descripción y ejemplos ilustrativos del dominio de cada uno de los atributos de las entidades
1. **Vivero:**

   - **Código vivero (Atributo identificador):** Identificador único para cada vivero. Ejemplo: V001
   - **Nombre:** Nombre del vivero. Ejemplo: "Vivero Central"
   - **Georreferencia:** Información espacial que describe la ubicación exacta del vivero. Compuesto por:
     - **Latitud:** Coordenadas geográficas que ubican el vivero. Ejemplo: -34.603722
     - **Longitud:** Coordenadas geográficas que ubican el vivero. Ejemplo: -58.381592
   
   ![image](https://github.com/user-attachments/assets/badf0c24-cc86-49ed-ae4e-fb890a7cf105)

2. **Zona:**

   - **Código zona (Atributo identificador):** Identificador único de la zona dentro del vivero. Ejemplo: Z001
   - **Nombre:** Nombre de la zona dentro del vivero. Ejemplo: "Zona Norte"
   - **Georreferencia:** Ubicación espacial de la zona. Compuesto por: 
     - **Latitud:** Coordenadas geográficas que ubican el vivero. Ejemplo: -34.603722
     - **Longitud:** Coordenadas geográficas que ubican el vivero. Ejemplo: -58.381592
   - **Productividad (Opcional):** Un atributo relacionado con la productividad de la zona (puede estar relacionado con cultivos, rendimiento, etc.). Ejemplo: 85%

   ![image](https://github.com/user-attachments/assets/789cb98f-a8e1-400e-a642-d58c2a19077c)

3. **Empleado:**

   - **Código empleado (Atributo identificador):** Identificador único para cada empleado. Ejemplo: E123
   - **Nombre:** Nombre del empleado. Ejemplo: "Juan"
   - **Apellidos:** Apellidos de la persona. Compuesto por:
     - **Primer apellido:** Primer apellido de la persona. Ejemplo: "Pérez"
     - **Segundo apellido:** Segundo apellido de la persona. Ejemplo: "García"
   - **Fecha ingreso:** Fecha en la que el empleado comenzó a trabajar. Ejemplo: 01/03/2021
   - **DNI:** Documento de identidad del empleado. Ejemplo: 12345678A
   - **Productividad (Opcional):** Medida del rendimiento del empleado. Ejemplo: 90%

  ![image](https://github.com/user-attachments/assets/820c637f-fb23-46a0-9a40-c02cacee92c5)

4. **Cliente fidelizado:**

   - **Código cliente (Atributo identificador):** Identificador único del cliente. Ejemplo: C001
   - **Nombre:** Nombre del empleado. Ejemplo: "María"
   - **Apellidos:** Apellidos de la persona. Compuesto por:
     - **Primer apellido:** Primer apellido de la persona. Ejemplo: "González"
     - **Segundo apellido:** Segundo apellido de la persona. Ejemplo: "López"
   - **Email:** Correo electrónico del cliente. Ejemplo: "maria.gonzalez@example.com"
   - **Teléfono:** Número de contacto. Ejemplo: 555123456
   - **Fecha registro:** Fecha en la que el cliente se registró. Ejemplo: 05/07/2022
   - **Compra total:** Monto total acumulado por las compras del cliente. Ejemplo: $2,500
   - **Bonificación:** Información sobre las bonificaciones obtenidas. Ejemplo: 5%
  
   ![image](https://github.com/user-attachments/assets/29fe9d2c-c884-4cec-a9c5-a45206f5acbb)

5. **Producto:**

   - **Código producto (Atributo identificador):** Identificador único del producto. Ejemplo: P001
   - **Nombre:** Nombre del producto. Ejemplo: "Planta de Rosas"
   - **Precio:** Precio unitario del producto. Ejemplo: $20
   - **Descripción:** Descripción del producto. Ejemplo: "Planta de rosa roja"
  
   ![image](https://github.com/user-attachments/assets/933448a6-37f3-4b4c-8fb9-b8639603e043)

6. **Pedido:**

   - **Código pedido (Atributo identificador):** Identificador único del pedido. Ejemplo: O001
   - **Fecha:** Fecha en la que se realizó el pedido. Ejemplo: 10/10/2024
  
   ![image](https://github.com/user-attachments/assets/9aedf578-6e80-40f2-9bb6-48de81f9eee4)

## 3. Descripción de cada una de las relaciones definidas y sus cardinalidades
1. **Vivero - Zona (tiene):**
   - Un vivero tiene varias zonas (1, N).
   - Cada zona pertenece a un solo vivero (1, 1).
   - **Ejemplo:** El "Vivero Central" tiene la "Zona Norte" y la "Zona Sur".
  
   ![image](https://github.com/user-attachments/assets/c04ae433-3881-4991-8215-fc9db71b330f)

2. **Zona - Producto (tiene [stock]):**
   - Una zona puede tener varios productos en stock (1, N).
   - Un producto puede tener stock en varias zonas (1, N).
   - **Atributo:**
     - **Stock:** Cantidad de un determinado producto en una zona.
   - **Ejemplo:** La "Zona Norte" tiene en stock "Planta de Rosas" y "Planta de Tulipanes".
  
   ![image](https://github.com/user-attachments/assets/bee0dc99-e40e-445d-9a11-63c36e99f021)

3. **Vivero- Empleado(trabaja):**
   - Un empleado trabaja en un vivero (1, 1).
   - Cada vivero tiene uno o más empleados (1, N).
   - **Ejemplo:** El empleado "Juan Pérez" trabaja en el vivero del norte.
  
   ![image](https://github.com/user-attachments/assets/1417be6d-c1d4-45f2-a94f-ebc6fbd77bd2)

4. **Empleado - Zona(realiza [tarea]):**
   - Un empleado realiza la tarea en una zona(1,1).
   - Cada zona tiene varios empleados que realizan la tarea (1,N).
   - **Atributo:**
     - **Tarea:** Labor específica que realiza un empleado.
   - **Ejemplo:** “Juan” riega las flores en la “Zona Sur”.
  
   ![Captura](https://github.com/user-attachments/assets/b9f479cb-1e82-4cc1-8f8f-de7c41635954)

5. **Vivero - Empleado - Zona (Restricción de inclusividad):**
   - Para que un empleado realice una tarea en una zona, tiene que, previamente, estar trabajando en un vivero (1,1).
   - **Ejemplo:** “Juan Pérez” riega las flores en la “Zona Sur” del “Vivero Central” mientras que “Pepito López” no está asignado a una zona ya que no trabaja en un vivero.
  
   ![Captura2](https://github.com/user-attachments/assets/946467fb-7d2f-48b9-bfe2-5f945b948b6b)

6. **Empleado - Pedido - Cliente fidelizado (realiza):**
   - Un cliente fidelizado realiza varios pedidos a varios  empelados (1,N,N).
   - Un empleado atiende varios pedidos a varios clientes fidelizados (1,N,N).
   - Un cliente fidelizado realiza a un empleado uno o varios pedidos (1,1,N).
   - **Ejemplo:** "Jose" es un cliente fidelizado que hace 3 pedios a "Maria".
  
   ![image](https://github.com/user-attachments/assets/f675658d-eea7-49e1-b107-494b4b101de7)

## 4. Restricciones semánticas
1. **Vivero**
   - **Restricción de unicidad en el código del vivero:** El código vivero debe ser único para evitar confusiones entre diferentes viveros.
   - **Coherencia en georreferencias:** La latitud y longitud deben estar dentro de los rangos válidos para garantizar ubicaciones geográficas precisas.
2. **Zona**
   - **Restricción de unicidad en el código de la zona:** El código zona debe ser único dentro de cada vivero para diferenciar las zonas adecuadamente.
   - **Coherencia en georreferencias:** La latitud y longitud de la zona deben ser válidas y no pueden ser iguales a las de otros viveros.
3. **Empleado**
   - **Restricción de unicidad en el código del empleado:** El código empleado debe ser único para cada persona en la base de datos.
   - **Validez de la fecha de ingreso:** La fecha de ingreso debe ser anterior o igual a la fecha actual, garantizando que los empleados registrados sean válidos.
   - **Unicidad del DNI:** El DNI debe ser único para cada empleado, evitando duplicados que puedan generar confusión.
4. **Cliente fidelizado**
   - **Restricción de unicidad en el código del cliente:** El código cliente debe ser único para cada cliente registrado en el sistema.
   - **Validez del correo electrónico:** El email debe ser único y seguir un formato válido para asegurar la correcta comunicación con los clientes.
   - **Restricción sobre la fecha de registro:** La fecha de registro debe ser anterior o igual a la fecha actual.
5. **Producto**
   - **Restricción de unicidad en el código del producto:** El código producto debe ser único para evitar confusiones entre diferentes productos.
   - **Validez del precio:** El precio del producto no puede ser negativo, asegurando que todos los productos tengan un valor válido.
6. **Pedido**
   - **Restricción de unicidad en el código del pedido:** El código pedido debe ser único para identificar cada transacción de manera clara.
   - **Validez de la fecha del pedido:** La fecha del pedido debe ser anterior o igual a la fecha actual para garantizar que las transacciones sean cronológicamente correctas.
