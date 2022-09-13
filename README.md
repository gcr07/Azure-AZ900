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

2ble factor de autenticacion para mayor seguridad tambien llamado MFA 






















































