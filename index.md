# AWS Conceptos Certificacion Practitioner

# AWS Partner: Accreditation
### Servicios de computo:
Desarrollar, implementar, ejecutar y escalar cargas de trabajo en la nube de AWS.

- **Amazon EC2**: Capacidad de computo de tamaño modificable
- **Amazon EC2 Auto Scaling**: Aumentar o disminuir el numero de instancias
- **Elastic Loan Balancing**: Distribuir el trafico entrante
- **Amazon Elastic Container Service**: Ejecutar aplicaciones en un cluster administrado
- **Amazon Elastic Kubernetes Service**: Ejecutar aplicaciones de cubernetes en AWS y en las instalaciones
- **AWS Lambda**: Ejecutar codigo de respuesta a eventos

#### Beneficios de Amazon EC2
- Elasticidad
- Control
- Flexibilidad
- Integracion
- Fiable
- Proteccion
- Rentabilidad
- Sencillo

#### Opciones de Amazon EC2: tipos de instancias
Amplia seleccion de configuraciones de harware y software optimizadas para adaptarse a diferentes casos practicos.

- **General Purpose:** Proporciona una combinacion equilibrada de recursos
- **Compute Optimized**: Son ideales para las aplicaciones que dependen de los recursos de computo y se benefician de los procesadores de alto rendimiento
- **Memory Optimized**: estan diseñadas para ofrecer un rendimiento rapido para cargas de trabajo que procesan grandes conjuntos de datos en la memoria.
- **Accelerated Computing**: usan aceleradores de hardware o procesadores de codigo para realizar funciones, como el calculo de numeros de coma flotante, el procesamiento de graficos, concordancia de patrones de datos, con una mayor eficacia comparado con un software que se ejecuta en un cpu.
- **Storage Optimized**: sirven para las cargas de trabajo que requieren un acceso secuencial de lectura y escritura a los conjuntos de datos en el almacenamiento local. Estan optimizados para entregar decenas de miles de operaciones E/S aleatorias de baja latencia por segundo, o IOPS, a las aplicaciones

#### Por que el escalado es importante:
1. Ejecucion de nuevas instancias antes de los periodos de carga maxima.
1. Uso de supervision para escalar horizontalmente mediante programacion
1. Reduccion horizontal automatica
1. Pago por los recursos necesarios cuando sea necesario

#### EC2 AutoS caling
- Ajusta automaticamente los recursos
- Defina donde Amazon E2C Auto Scaling implementa los recursos
- Especifique la Amazon VCP y las subredes

Capacidad minima: Garantiza que siempre tenga instancias E2C en constante ejecucion.

Capacidad Maxima: Hace que Amazon Auto Scaling escale horizontalmente el numero de instancias de E2C para gestionar el aumento de demanda.

Capacidad Deseada: Debe ser mayor o igual al limite minimo o inferior o igual al limite maximo.

#### Elastic Loan Balancing
Distribucion automatica del trafico entre varias instancias E2C.
- Mayor disponibilidad y tolerancia a errores.
- Configuracion de comprobacion de estados.
- Reasignacion de cifrado y descifrado.

Admite 3 tipos de carga:

1. **Application Load Balancer(Equilibrador de carga de aplicacion):** Especialmente diseñado para aplicaciones web
1. **Network Load Balancer(capa de red)**: Opera en la capa de red y es mas resistentes a los picos de traficos repentinos.
1. **Gateway Load Balancer**: Dirige el trafico a los dispositivos virtuales que se encuentran en AWS Marketplace.

**AMI**: Amazon Machine Images
#### En resumen:

**Instancias EC2** = bloques de creacion.
Aplicar **AMI** para personalizar.
Configurar el escalado automatico y el equilibrio de carga.
Pago por lo que utilizo.

### Introducción al almacenamiento AWS
Esta sección se centra principalmente en Amazon Simple Storage Service (Amazon S3) y Amazon Elastic Block Store (Amazon EBS),

#### Servicios de almacenamiento
Un lugar fiable, escalable y seguro para los datos

- **Amazon Elastic Block Store:** Almacenamiento persistente a nivel de bloque.
- **Amazon S3**: Almacenamiento de objetos duradero y escalable.
- **Amazon S3 Glacier**: Archivado y respaldo de datos.
- **AWS Storage Gateway**: Integracion del almacenamiento en la nube con cargas de trabajo en las instalaciones.
- **Amazon Elastic File System**: Almacenamiento de archivos para las instancias de Amazon EC2.
- **Amazon FSx**: Almacenamiento de archivos para sistemas de archivos muy utilizados.

#### Clases de almacenamiento S3
- Amazon S3 Standard.
- Amazon S3 Standard - Acceso proco frecuente.
- Amazon S3 One Zone - Acceso proco frecuente.
- Clases de almacenamiento de S3 Glacier.

S3 Intelligent-Tiering mueve automaticamente los objetos entre niveles segun los patrones de acceso.

Amazon Glacier: almacenamiento de copias de seguridad a largo plazo.

### Introducción a los servicios de base de datos de AWS
- **Amazon Relational Database Service (RDS):** Capacidad rentable de tamaño modificable. Es un servicio de BD relacionales con 6 motores de BD populares
- **Amazon DynamoDB**: Rendimiento rapido y predecible. Es una BD noSQL
- **Amazon Elastic Cache**: Recuperacion de informacion rapida y administrada. Es un servicio de cache para implementar, usar y escalar cache en memoria en la nube.

#### Ventajas de RDS:
1. Facil configuracion, administracion y mantenimiento.
1. Reduccion de las cargas pesadas sin diferenciar.
1. Alta disponibilidad con un boton de comando.
1. Respaldo y recuperacion automatico.
1. Escalar o reducir verticalmente en funcion del patron.

#### Ventajas Bases de datos en EC2:
1. Mayor control y flexibilidad.
1. Acceso al sistema operativo.
1. Necesidades de funciones de una aplicacion especifica.

#### En resumen:
Su enfoque es reemplazar las tareas de administracion por procesos de valor agregado.

### Introducción a las redes
Aislamiento de la infraestructura de la nube y escalado de capacidad de gestion de solicitudes.

- **Amazon VPC(Virtual private cloud):** Crear una red virtual en la nube.
- **Grupos de seguridad**: Control de acceso a la instancias.
- **Listas de control de acceso a la red(NACL)**: Control de acceso a las subredes
- **Amazon Route 53**: Enrutar a los usuarios finales a aplicaciones de internet.

### Introducción a la seguridad en AWS
En AWS, la segurida en la nube es la mayor prioridad.

- Posibilidad de heredar los beneficios del centro de datos y la arquitectura de red AWS.
- Similitud con los centros de datos en las instalaciones, sin mantenimiento de instalaciones ni hardware.
- Capacidad de automatizacion con facilidad.
- Posibilidad de heradar todas las practicas recomendadas de AWS.

AWS se creo con el fin de ayudar a crear una infraestrutura segura, de alto desempeño, resiliente y eficiente para aplicaciones.

#### Servicios seguridad, identidad y conformidad.
- **Identity an Access Managment(IAM):** Administra identidades, recursos y permisos de forma segura a gran escala.
- **Proteccion de infraestructura**: Inspecciona y filtra el trafico para evitar el acceso no autorizado en el host, la red y aplicacion.
- **Conformidad**: Monitorea constantemente su entorno con verificaciones basadas en las mejores practicas recomendadas por AWS y los estandares del sector de la organizacion.

#### Administracion segura del acceso a los recursos y servicios de AWS.
1. Control de acceso detallado de los recursos AWS.
1. Autenticacion multifactor.
1. Capacidad de analizar el acceso.
1. Integracion de directorios corporativos.

### Resumen
#### Interfaces de administración de AWS
![img](img/02.png)
Los usuarios de AWS pueden crear y administrar recursos en la plataforma de tres formas. Las tres opciones se basan en una interfaz de programa de aplicación (API) común de REST que funciona como la base de AWS. 

**La consola de administración de AWS** proporciona una interfaz gráfica completa para la mayoría de las características que ofrece AWS. Facilita la administración en la nube para todos los aspectos de la cuenta de AWS del cliente, incluido el monitoreo del gasto mensual, la administración de credenciales de seguridad y la configuración de nuevos usuarios de IAM.

**AWS Command Line Interface (AWS CLI)** proporciona un conjunto de servicios que se puede lanzar desde un programa de comando en Linux, Mac o Windows La CLI es una herramienta de código abierto que ofrece comandos para interactuar con los servicios de AWS.

**Los Kits de desarrollo de software (SDK)** de AWS son paquetes que brindan acceso a AWS en una variedad de lenguajes de programación populares. AWS administra la infraestructura como código mediante los SDK de AWS y las API que los subyacen. Estos SDK específicos del lenguaje contienen API que permiten a los clientes incorporar de forma fácil la amplia gama de servicios en la nube de AWS a su código sin tener que escribir las funciones ellos mismos.

#### Variedad y penetración de los servicios de AWS
![img](img/03.png)
AWS ofrece un amplio conjunto de productos y servicios basados en la nube, entre otros, cómputo, almacenamiento, bases de datos, análisis, redes, dispositivos móviles, herramientas para desarrolladores, herramientas de administración, Internet de las cosas (IoT), seguridad y aplicaciones de empresas. Estos servicios ayudan a las organizaciones a avanzar con mayor rapidez, reducir los costos de TI y les permiten escalar cuando es necesario. AWS cuenta con la confianza de las empresas más grandes y emergentes para hacer posible una amplia variedad de cargas de trabajo, como aplicaciones web y móviles, desarrollo de juegos, procesamiento y almacenamiento de datos, almacenamiento, archivado y muchas otras.


## Dominio I: Conceptos de la nube de AWS

### On Premise
Con mis propios recursos. Es decir hacer realizar el despliegue requerido con recursos propios. Por mencionar algunos de ellos:
- Rentas o construccion de inmueble(data center)
- Seguros
- Luz, internet
- Licencias
- Salarios
- Equipo(Servidores, routers, cables, herramientas, monitores, computadores)

### Cloud
Nube. Es decir solo se renta el servicio dependiendo de las necesidades de la aplicacion o despliegue. En caso de requerir mas servidores o requerimientos se renta lo antes mencionado.

### On Premise vs Cloud
|**On Premise**                             |**Cloud**                                                                                                                                                                                                                   |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|Costes Fijos de Harware                    |Pago por uso                                                                                                                                                                                                                |
|Precios de adquisicion de usuario final    |Precios de gran proveedo (economia de escala)                                                                                                                                                                               |
|Dimensionado inicial y escalado            |Disponilibidad bajo de demanda: **Escalado vertical**: contratar mas requerimientos, mas nucleos, ram, etc. **Escalado Horizontal**: Contratar mas recursos, en ves de un servidor contratar 2, dependiendo de la necesidad.|
|Tiempos y tramites de solicitud de recursos|Entrega casi inmediata                                                                                                                                                                                                      |
|Mantenimiento de centro de datos           |Externalizado                                                                                                                                                                                                               |
|Problemas para despliegues mundiales       |Red global                                                                                                                                                                                                                  |


### Capex
**Capital Expenditure**
CapEx o Capital Expenditure se reﬁere a los gastos de capital o las inversiones que realiza una empresa al adquirir un activo.

Por ejemplo:
- **Infraestructura de TI**
- **Equipamiento informático**
- **Automóviles**

**Características**:
- **Inversión en infraestructura física, se pierde liquidez**
- **Depreciación de la inversión en impuestos con el tiempo**
- **Se conoce el monto y se puede presupuestar**

### Opex
**Operational Expenditure**
OpEx conocido como Operational Expenditure, se reﬁere a los gastos operativos que realiza una empresa para que sus productos, sistemas o negocio en sí, funcionen.

Por ejemplo:

- **Compra de tóner para la impresora**
- **Arrendamiento de infraestructura**
- **Costos de mantenimiento de oficinas**

Cuando una empresa compra servicios, forman parte de OpEx, ya que no son parte de los activos, sino que se consumen por servicio, tal es el caso de los servicios en la nube, con la cual se suministran servicios bajo demanda y de forma flexible, como es IaaS, PaaS y SaaS.

**Características**

- **Gasto en productos/servicios que se facturan al consumir**
- **Sin costos iniciales, conservas liquidez, deducción del 100%**
- **No se conoce el gasto, se paga a medida que se usa**
- **El proveedor es también responsable por la adopción**

### IaaS, PaaS, SaaS
![img](img/01.png)
A considar que en estos tres servicios se nos presenta como una virtualizacion.
Como conclusion: 
- ***programador*** opta por PaaS por el simple hecho que se cuenta con todo lo requerido para realizar el despliegue de una aplicacion.
- ***Administrador de sistemas*** opta por IaaS debido a que solo requiere una infraestructura para generar un sistema con la complejidad requerida en especifico.


#### IaaS
Infraestructura como servicios (**Infraestructure as a Services**). Ellos se encargar de mantener, actualizar en optimas condiciones lo siguiente:
- Harware
- Redes
- Almacenamiento

Yo solo me haria cargo de lo siguiente:
- Sistema Operativo
- Entorno de Ejecucion
- Datos
- Aplicacion

En **IaaS** hay una clara separacion ya que solo se ofrece la infraestructura como servicio, es decir lo requerido para instalar y poner todo lo referente a software

#### PaaS
Plataformas como servicio(**Platform as a Services**), en este apartado ya se incluye una plataforma
por ende el servicio nos incluiria lo siguiente:
- Harware
- Redes
- Almacenamiento
- Sistema Operativo
- Entorno de Ejecucion

Por lo que por mi cuenta corre:
- Datos
- Aplicacion

En **PaaS** incluye ademas del harware una capa de software, es decir la base de este para poder instalar/especificar la manera en que manejare los datos y la apliacion.

#### SaaS
Software como servicios(**Software as a Services**) este servicio se incluye todo lo requerido para que este lo pueda utilizar, en ello se incluye lo siguiente:
- Harware
- Redes
- Almacenamiento
- Sistema Operativo
- Entorno de Ejecucion
- Datos
- Aplicacion

### Modelos de nube
Cuando decidimos utilizar la nube para implantar nuestro sistema, podemos elegir tres modelos:

- **Nube privada:** Toda la infraestructura y los datos se guardan en recursos privados a los que nadie mas tiene acceso.

- **Nube publica:** Utilizamos siempre uno o varios servicios de cloud computing. Todo forma parte de una o varias nubes publicas.

- **Hibrido:** Una parte se implementa en nuestros recursos privados y otra parte en la nube.

### Infraestructura tolerante a errores

- **Alta disponibilidad:** Disponilibidad a usuarios, 99.9%, 99.99%, 99.999%
- **Tolerancia a fallos:** Tolerante a errores que puedan provocar que la disponibilidad se caiga, para ello se mitiga haciendo duplicidad del servicio implementando un RAID, discos espejos. Los datos deben de estar a salvo en caso de fallas Harware

Los puntos anteriores fueron orientados a ***On Premise***. Ahora enfocando a un servicio AWS para tener un alta disponibilidad se debe implementar un balanceo de carga. Mediante 2 EC2, si una EC2 se llega a caer, el balanceo de carga se redirija a la segunda EC2

**EC2** -> Instancia de AWS.

### Aplicacion desacoplada

|Arquitecura monolitica                         |Desacopladas(Microservicios)                   |
|-----------------------------------------------|-----------------------------------------------|
|Todo el codigo en un solo elemento             |Instancias diferentes                          |
|Un error produce la caida de la infraestructura|Si falla uno, no se cae toda la infraestructura|
|Dependencia total de un conjunto a otros       |Pequeños conjuntos independientes              |


### Elasticidad
#### Escalado vertical
Crecer en potencia, aumentar 4 cpu, 8gb de ram en sistemas virtualizados
#### Escalado horizontal
Disponer de varias maquinas con la misma potencia, pero tener una comunicacion con la cantidad de maquinas virtualizadas

#### Scale in
Reducir es decir si la demanda de carga va dismunyendo, se hace la reduccion de equipo, maquinas.Es importante porque se hace un pago por uso. Con esto se refiere en que si se piensa en un **Scale in** el pago sera menor debido a que se esta reduciendo el equipo, maquina.

#### Scale out
Aumentar, es decir si la demanda de carga esta aumentando se  hace un escalado para aumentar y poder solventar la demanda. Es importante porque se hace un pago por uso. Con esto se refiere en que si se piensa en un **Scale out** se debera pagar mas por el aumento de equipo, maquinas.

### Procesamiento paralelo
Crear varias instancias que se puedan procesar a la vez y asi evitar que por decirlo asi la instancia 1 termine para poder procesar la instancia 2. Si no que cada una de esas instancias se trabajan en paralelo y se aprovecha la elasticidad horizontal o escalamiento horizontal

### AWS Well-Architected Framework(Marco de buena Arquitectura)
Ayuda a los arquitectos de la nube a crear una infraestructura segura, de alto rendimiento, resistente y eficiente para una variedad de aplicaciones y cargas de trabajo. Este marco, creado en torno a seis pilares (excelencia operativa, seguridad, fiabilidad, eficiencia de rendimiento, optimización de costos y sostenibilidad), ofrece un enfoque coherente para que los clientes y los socios evalúen las arquitecturas e implementen diseños escalables.
#### Principios generales de diseño
- **Dejar de adivinar necesidades de capacidad:** escala hacia arriba, abajo automaticamente.

- **Pruebas de sistemas a escala de produccion:** haga simulaciones reales, pero cortas.

- **Automatizacion:** haga un seguimiento de las acciones y optimice en consecuencia

- **Permitir arquitecturas evolutivas:** la capacidad de automatizar y probar bajo demanda reduce el riesgo de impacto de los cambios.

- **Impulse arquitectura utilizando datos:** tome desiciones basadas en hechos.

- **Simule errores y compruebe su arquitectura:** esto lo ayudara a comprender donde se pueden realizar mejoras y puede ayudar al manejo de eventos.

AWS Well-Architected Framework describe los conceptos clave, los principios de diseño y las prácticas recomendadas de arquitectura para diseñar y ejecutar cargas de trabajo en la nube. Responda un conjunto de preguntas básicas para descubrir hasta qué punto su arquitectura está en consonancia con las prácticas recomendadas en la nube y obtenga orientación para mejorarla.

Este marco de arquitectura tiene los siguientes pilares:
1. ***Excelencia operativa:*** El pilar de la excelencia operativa se concentra en ejecutar y monitorear los sistemas y en mejorar constantemente los procesos y los procedimientos. Entre los temas clave se incluyen la automatización de cambios, la respuesta a eventos y la definición de estándares para administrar las operaciones diarias.
</br>

1. ***Seguridad:*** El pilar de la seguridad se concentra en proteger la información y los sistemas. Entre los temas clave se incluyen la confidencialidad y la integridad de los datos, la administración de los permisos de usuarios y el establecimiento de controles para detectar eventos de seguridad.
</br>

1. ***Fiabilidad:*** El pilar de fiabilidad se centra en las cargas de trabajo que realizan las funciones previstas y en cómo recuperarse rápidamente de los errores para cumplir con las demandas. Entre los temas clave se incluyen el diseño de sistemas distribuidos, la planificación de la recuperación y cómo adaptarse a los requisitos cambiantes.
</br>

1. ***Eficiencia de rendimiento:*** El pilar de eficacia del rendimiento se centra en la asignación estructurada y simplificada de TI y en los recursos informáticos. Entre los temas clave se incluyen la selección de los tipos y tamaños de recursos optimizados para los requisitos de la carga de trabajo, la supervisión del rendimiento y el mantenimiento de la eficacia a medida que evolucionan las necesidades de la empresa.
</br>

1. ***Optimizacion de precios:*** El pilar de optimización de costos se centra en evitar gastos innecesarios. Entre los temas clave se incluyen la comprensión del tiempo dedicado y el control de la asignación de fondos, la selección de recursos para el tipo y la cantidad adecuados y el escalado para cumplir con las necesidades de la empresa sin gastos excesivos.
</br>

1. ***Sostenibilidad:*** El pilar de sostenibilidad se centra en minimizar los impactos ambientales de ejecutar cargas de trabajo en la nube. Entre los temas clave se incluyen un modelo de responsabilidad compartida para la sostenibilidad, la comprensión del impacto y la maximización del uso para minimizar los recursos necesarios y reducir los impactos posteriores. 

[Mas informacion sobre los pilares](https://aws.amazon.com/es/architecture/well-architected/?wa-lens-whitepapers.sort-by=item.additionalFields.sortDate&wa-lens-whitepapers.sort-order=desc&wa-guidance-whitepapers.sort-by=item.additionalFields.sortDate&wa-guidance-whitepapers.sort-order=desc)


## Dominio II: Seguridad y conformidad

### Responsibilidad compartida
Los asuntos relacionados con la seguridad y la conformidad son una responsabilidad compartida entre AWS y el cliente. Este modelo compartido puede aliviar la carga operativa del cliente, ya que AWS opera, administra y controla los componentes del sistema operativo host y la capa de virtualización hasta la seguridad física de las instalaciones en las que funcionan los servicios. El cliente asume la responsabilidad y la administración del sistema operativo invitado (incluidas las actualizaciones y los parches de seguridad), de cualquier otro software de aplicaciones asociado y de la configuración del firewall del grupo de seguridad que ofrece AWS.

#### AWS

|Software|              |             |                      |
|--------|--------------|-------------|----------------------|
|Computo |Almacenamiento|Base de datos|Infraestructura de red|
|**Harware AWS Global Infraestructuta** |
|Regiones|Zona de disponibilidad| Localicaciones|

#### Customer
|Responsabilidad del usuario              |
|-----------------------------------------|
|Datos del propio usuario                 |
|Aplicaciones instaladas, claves de acceso|
|Operacion del sistema, firewall y configuraciones, dependiendo del servicio contratado|
|Encriptacion de los datos del cliente y autenticacion|
|Encriptacion y configuracion del servidor|
|Trafico de red,proteccion de la identidad como de la integridad|

En conclusion somos responsables de lo que ocurre en la nube, es decir cuando hacemos uso de ella. Mientras AWS es responsable de que la nube este funcionando.

[Mas informacion](https://aws.amazon.com/es/compliance/shared-responsibility-model/)

### Conformidad y cumplimiento
El programa de conformidad de AWS ayuda a nuestros clientes a comprender los controles estrictos que tenemos instaurados en AWS para mantener la seguridad y la conformidad de la nube. Mediante la combinación de características de servicio centradas en el control y la auditoría con los estándares aplicables de conformidad o auditoría, los habilitadores de conformidad de AWS crean programas tradicionales que ayudan a los clientes a establecerse y trabajar en un entorno de control de seguridad de AWS.

Los estándares de TI con los que cumplimos están desglosados por certificaciones y acreditaciones; leyes, regulaciones y privacidad; y alineaciones y marcos. Un auditor independiente externo evalúa las certificaciones y acreditaciones de conformidad, lo cual tiene como resultado una certificación, un informe de auditoría o una acreditación de conformidad. Los clientes de AWS tienen la responsabilidad de cumplir las leyes y regulaciones de conformidad y programas de privacidad correspondientes. Las homologaciones y los marcos reguladores de conformidad incluyen requisitos de seguridad y conformidad publicados para una finalidad específica, como un sector o una función determinados.

#### AWS Config
- Audita las configuraciones de los recursos de AWS
- Monitorea permanentemente las configuraciones
- Evalua automaticamente las configuraciones registradas frente a las configuraciones deseadas.
- Revisa los cambios de configuracion

#### AWS Artifact
- Es un recurso destinado a la informacion relacionada con la conformidad.
- proporciona acceso a informes de seguridad y conformidad, asi como tambien a acuerdos en linea seleccionados.
- Puede obtener acceso a descargas de ejemplo: 
    - Certificaciones ISO de AWS
    - Informes del sector de tarjetas de pago (PCI) y del control de organizaciones de servicios(SOC)

### Definicion de servicios
 - **CloudWatch**: Recopila datos operativos y de monitoreo en forma de registros, metricas y eventos, y permite su visualizacion mediante paneles automatizados para obtener una vista mas unificada de los recursos, las aplicaciones y los servicios de AWS que se ejecutan en AWS y en las instalaciones.

 - **AWS Cloud Trail**: Monitorea y registra la actividad de la cuenta en toda la infraestructura de AWS, lo que permite controlar las acciones de almacenamiento , analisis y reparacion. Controla todo lo que se hace desde la consola, CLI, SDK y API.     











Lalo_2393