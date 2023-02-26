<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e8/Logo_Tecmilenio_2014.png/1200px-Logo_Tecmilenio_2014.png">
</p>

<p align="center" style="padding: 30px; margin: 0;">
 Tecmilenio Outcoms 1 for each module : 1, 2 &amp; 3 (Final Proyect)
  

</p>

-------------
  
 ### Caso a trabajar

<p>
"Halcon" es un distribuidor de materiales de construcción que requiere una aplicación web para automatizar sus procesos internos. Después de una entrevista, las necesidades del cliente son las siguientes:
</p>

 
## Outcome 1


### Necesidades

####  Primera necesidad

`
RECOMENDADO: Diagrama de actividades
`
`
BASE DE DATOS: No relacional, Motivo: Imagenes
`

 > Una aplicación web que permita a sus clientes ver el estado de sus pedidos desde una pantalla principal donde el cliente ingresa un número de cliente y un número de factura. La información a mostrar es el estado y, en caso de tener un estado de "Entregado", mostrar la foto de la evidencia de que fue entregado. Los estados son los siguientes:


*   **Pedido:** cuando se realiza un pedido de material y el ejecutivo de ventas lo ingresa al sistema.

*   **En proceso:** cuando el pedido está en stock y se está preparando para su envío o, en su defecto, cuando no está en stock y debe ser comprado a un proveedor externo.

*  **En ruta:** cuando el pedido ha sido enrutado para su distribución.

*   **Entregado:** cuando el pedido ha sido entregado en las instalaciones del cliente.

#### Segunda necesidad

`
RECOMENDADO: Diagrama de casos de uso, clases
`
`
BASE DE DATOS: Relacional
`

> El personal que trabaja en la empresa puede acceder a un panel de control administrativo para llevar a cabo sus respectivas actividades. Esto requiere lo siguiente:

- Que el sistema traiga por defecto un usuario administrativo, que pueda registrar nuevos usuarios y asignar roles a los usuarios.


  - Los roles son los departamentos (importante: los clientes no podrán registrarse):
    - **Ventas:** los encargados de tomar pedidos de los clientes.
	
    -  **Compras:** en caso de no tener algún material, estos son los usuarios que gestionan la compra de materiales.
	
    - **Almacén:** quienes gestionan el almacén y preparan los pedidos para el envío, también informan a Compras sobre los materiales que no existen o tienen poco stock.

    - **Ruta:** quienes supervisan la distribución de los pedidos a los clientes. 


#### Tercera necesidad

`
RECOMENDADO: Diagrama BPMN
`
`
BASE DE DATOS: No relacional, Motivo: Imagenes
`

> Se respeta el ciclo de vida de un pedido:

- Un cliente llama a la empresa para realizar un pedido.

- El vendedor toma el pedido y asigna una nueva entrada a la plataforma, que debe contener lo siguiente:

  - Número de factura consecutivo al que corresponderá el pedido.
  
  - Nombre o razón social del cliente que realiza el pedido.
  
  - Un número de cliente único que se asignará arbitrariamente.
  
  - Datos fiscales del cliente para el llenado de la factura física que luego se enviará por correo electrónico (la aplicación no enviará facturas, cada pedido está vinculado con un número de factura, pero una persona de administración supervisa la elaboración de las facturas por separado).
  
  - Fecha y hora del pedido.
  
  - Dirección de entrega del pedido.
  
  - Un campo para ingresar cualquier nota o información adicional.
  
- El estado por defecto que adquiere el pedido después de ser ingresado es "Pedido" y en ese momento el pedido debería ser visible para todos los empleados de la empresa.

- Una persona del almacén debe encargarse del pedido y cambiar su estado a "En proceso". Una vez que haya terminado de reunir los materiales (almacén interno o acordando con Compras la adquisición del producto faltante), cambia el estado a "En ruta" y, a su vez, carga físicamente una unidad junto con el transportista.

- La persona en la ruta debe tomar una foto de la unidad cargada y subirla a la plataforma (considere que la opción de carga de fotos solo debe ser visible para las personas en el departamento de Ruta).

## Outcome 2
## Outcome 3

## Metodologia del que se hara uso

La realizacion de este proyecto se hara con la metodologia Agil `Scrum` para adaptarse a los cambios de requisitos, ciclos de desarrollo más cortos, mayor colaboración y comunicación, y enfoque en la entrega de valor.

## Tipos de diagramas utilizados y recomendados:

#### Diagrama BPMN 
Podría ser útil para representar el flujo de trabajo de los procesos del negocio, desde el momento en que se recibe la orden hasta que se entrega al cliente. Sería útil para visualizar los diferentes estados de los pedidos, y las acciones que se llevan a cabo en cada uno de ellos.

#### Diagrama de clases
Los diagramas de clases serían útiles para representar la estructura de datos de la aplicación. Por ejemplo, se podrían representar las clases para las órdenes, los clientes, los usuarios, y los roles. De esta forma, se podría tener una vista general de las diferentes entidades de la aplicación y cómo están relacionadas entre sí.

#### Diagrama de actividades
Los diagramas de actividad podrían utilizarse para representar los diferentes pasos que se llevan a cabo en cada uno de los estados de las órdenes. Por ejemplo, se podría utilizar un diagrama de actividad para representar el proceso que se lleva a cabo cuando una orden se encuentra en estado "In process", detallando las tareas que se realizan para preparar el pedido para su entrega.

#### Diagrama de casos de uso
Los diagramas de casos de uso podrían utilizarse para representar los diferentes roles que interactúan con la aplicación, y las acciones que cada uno de ellos puede realizar. Por ejemplo, se podría representar un caso de uso para los usuarios que pueden visualizar el estado de sus pedidos, otro para los usuarios encargados de la gestión de las órdenes, y otro para los usuarios encargados de la distribución de los pedidos.
