# Azure Certification

# Define Cloud Computing

## Shared responsability model

Igual que aws lo que tu eres responsable y lo que ellos son 

## Public Cloud

La que se usa cuando generas una VM

## Private cloud o Azure Stack(revisar nombre)

La que es solo como tu red de la empresa .

## Nube gubernamental 

Tienes que demostrar que trabajas para el gobierno

## Nube Hybrida

Cosas que se tienen on premise pero tambien se conectan con cosas que estan montadas en la nube.

# Resource Groups

Son organizacion logica de los elementos que que usas de la nube no importa si por ejemplo una base de datos esta en Europa
y una maquina virtual en Estados Unidos.
Esto permite que puedan actuar como uno y se les puede aplicar por ejemplo una politica o seguridad como uno.
Un resorce solo puede ser parte de un ***grupo*** no de varios.

Por arriba de los grupos esta la subscripcion que es quien paga la cuenta y arriba de esta el manejo de grupos (no se porque pero asi esta)

# Servicios

## Functions App

Se trata de  funciones serverless estilo LAMBDA AWS.


# Azure Storage

Nota cuando creas una storage account debe de tener un nombre unico tal y como en aws( me gusta mas aws)
Existen el Hot access que se cobra por el almacenamiento y por acceder a el y el 
cool access este ahorra dinero pero pagas cuando accedes pero cuesta mucho teimpo acceder a los archivos. Existe una opcion de inmutabilidad para tenams de que no se pueda cambiar los archivos (temas legales podrian ser).
Basicamente es como el S3 de aws y este se divide en:

## General Propose

Es el mas comun tipo de almacenamiento se abrevia como gpv2

## Azure Data Lake Storage

Es el mas barato tipo de almacenamiento 1.8 centavos por GB

## BLOB Binary Large Objet

Es un objeto o archivo como archivos zip de texto binarios todo lo que se pueda guarfar o incluso datos guardado 

## Managed Disks 

Son discos de almacenamiento virtaules reservas y pagas por la capacidad que estas rentando no por lo que uses en de espacio.

# Identity 

Representation  de algo una identidad tienes que probar que eres quien dices ser con un password un certificado una llave secreta 

## Via Active Directory

Te permite autenticarte con AD aqui se llama  AS18 tambien al parecer. Es un poco diferente en azure Identity as as service 
tiene ventajas porque no se tiene que preocuápst por el codigo  que maneja el password 

### Security

se usa para evitar hackers ademas tiene muchas funciones permisos de usuarios tienen centralizadas su aplicaciones 
Single Sing On (devices pueden tener identidad) 

## AD COnditional Access


Para detectar por ejemplo accesos sospechosos. por ejemplo un logeao desde otro pais. Detectar primeros inicios de secion no normales
IPS etc manda mensaje para verificar que si sea la persona osea toma una descicion 

## 2FA

2ble factor de autenticacion para mayor seguridad tambien llamado MFA. Existen varios metodos para esto SMS, Email, authenticator, app, phone call.

## Three Factors

COmo por ejemplo tus huellas tu rostro  algo que no se puede cambiar

## Passwordless

una nueva forma de autenticarte te pide que memorices algunas cosas y usa por ejemplo tu huella o tu tu patron o por ejemplo el reconocimiento de tu rostro 
o el que se usa en outlook que te dice un numero para entrar.


## Role Base Access COntrol (RBAC)

Tiene que ver con autorizacion . Si tienes un token puedes acceder esa es la escencia. Se pueden generar roles. Depende por ejemplo de los departamentos
Cada rol puede tener permisos granulares. COmo en Linux puedes asginar permisos de lectura y escritura a archivos.


## Zero Trist Model Security

Es un modelo que te dice de los privilegios minimos que tienes que utilizar cuando creas usuarios o dar privilegios a unos existentes.Es como cerrar todas las puertas 
de dentro de tu casa y solo las perosnas que tienen la llave prodran abrir los cuartos. NO confies en otros.

Hay tes pricipios fundamentales de esta metodologia:

1. Verifique explicitamente
2. Use el acceso con menos privilegios
3. Asuma que ha habido una violacion de datos.

Existen 2 maneras de tener accceso Just in Time (JIT)
Just enough access ( JEA)

Proteccion con tra ataques de fuerza bruta. Descarga de archicos todo esto se necesitara detener.
Se podria encryptar la informacion.

## Defense in Depth

Se refiere a que  no solo uses una proteccion si no intentes usar multiples herramientas para proteger la seguridad de las aplicaciones como 
identity perimeter ( DDoS) API Mangment firewalls etc. No todos los usuarios seran aptos para conectarse al escritorio remoto. Existen 7 capas segun Microsoft

#  Micorosft Defender for Cloud 

Es un producto por el cual tienes que pagar. Protege servicios que tengas en la nube pero existe un costo al mes 





# de aqui en adelante la informacion fue sacada de Microsoft

# Modelos de la Nube

## Nube privada

Es la nube que por poner un ejemplo se traslada de tu infra on premise a azure y es mas cara que la publica.

## Nube pública

Un proveedor de nube de terceros crea, controla y mantiene una nube pública. Con una nube pública, cualquier persona que quiera comprar servicios en la nube puede acceder a los recursos y usarlos. La disponibilidad pública general es una diferencia clave entre las nubes públicas y privadas.

## Nube híbrida

Una nube híbrida es un entorno informático que usa nubes públicas y privadas en un entorno interconectado. Se puede usar un entorno de nube híbrida para permitir el incremento de una nube privada y acomodarse al aumento de la demanda temporal mediante la implementación de recursos de nube pública. La nube híbrida se puede usar para proporcionar una capa adicional de seguridad.

# Ventajas de Azure o la Nube

## Alta disponibilidad

Que los recursos esten siempre disponibles...

## SLA Acuerdos de nivel de Servicio

Es el acuerdo formal entre un proveedor de servicios y un cliente que garantiza al cliente un nivel de servicio establecido.

## Escalabilidad

 La escalabilidad hace referencia a la capacidad de ajustar los recursos para satisfacer la demanda.
 
 ## Escalado vertical ( capacidad de procesamiento etc)
 
 Con el escalado vertical, si estuviera desarrollando una aplicación y necesitase más potencia de procesamiento, podría escalar verticalmente para agregar más CPU o RAM a la máquina virtual. 
 
 ## Escalado horizontal ( mas maquinas virtuales contenedores etc)
 
 Con el escalado horizontal, si de repente experimentase un salto elevado en la demanda, los recursos implementados se podrían escalar horizontalmente (ya sea de forma automática o manual). Por ejemplo, podría agregar máquinas virtuales o contenedores adicionales, mediante el escalado horizontal. De la misma manera, si hubiera una caída significativa en la demanda, los recursos implementados se podrían escalar (ya sea de forma automática o manual), mediante el escalado vertical.
 
 ## Reliability Confiabilidad
 
 La confiabilidad es la capacidad de un sistema de recuperarse de los errores y seguir funcionando. También es uno de los pilares del Marco de arquitectura de Microsoft Azure.
 
 ## Prediction 
 
 La previsibilidad en la nube le permite avanzar con confianza. La previsibilidad se puede centrar en el rendimiento o los costos. Tanto la previsibilidad de rendimiento como la de costos están muy influidas por el Marco de arquitectura de Microsoft Azure. Implemente una solución creada en torno a este marco que sea predecible en relación con el costo y el rendimiento.
 
 ## Rendimiento
 
La previsibilidad del rendimiento se centra en predecir los recursos necesarios para ofrecer una experiencia positiva para los clientes. El escalado automático, el equilibrio de carga y la alta disponibilidad son solo algunos de los conceptos de nube que admiten la previsibilidad del rendimiento. 

## Coste

La predicción de costos se centra en pronosticar el costo del gasto en la nube. Con la nube, puede realizar el seguimiento del uso de recursos en tiempo real, supervisar los recursos para asegurarse de que los usa de la manera más eficaz y aplicar análisis de datos para buscar patrones y tendencias que ayuden a planear mejor las implementaciones de recursos.
























































