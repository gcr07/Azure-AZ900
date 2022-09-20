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


# Azure Storage


Una cuenta de almacenamiento proporciona un espacio de nombres único para los datos de Azure Storage al que se puede acceder desde cualquier lugar del mundo a través de HTTP o HTTPS. Los datos de esta cuenta son seguros, de alta disponibilidad, duraderos y escalables de forma masiva.

Al crear la cuenta de almacenamiento, primero seleccionará el tipo de cuenta de almacenamiento.

1. Almacenamiento con redundancia local (LRS)
2. Almacenamiento con redundancia geográfica (GRS)
3. Almacenamiento con redundancia geográfica con acceso de lectura (RA-GRS).
4. Almacenamiento con redundancia de zona (ZRS)
5. Almacenamiento con redundancia de zona geográfica (GZRS)
6. Almacenamiento con redundancia de zona geográfica con acceso de lectura (RA-GZRS)

Lo anterior es en cuanto a donde se replican los archivos

VER CAPTURAS de pantalla


# Redundancia y como los datos se replican

## Redundancia en la región primaria

Los datos de una cuenta de Azure Storage siempre se replican tres veces en la región primaria. Azure Storage ofrece dos opciones para replicar los datos en la región primaria, el almacenamiento con redundancia local (LRS) y el almacenamiento con redundancia de zona (ZRS).

## Almacenamiento con redundancia local

El almacenamiento con redundancia local (LRS) replica los datos tres veces dentro de un único centro de datos en la región primaria. LRS ofrece una durabilidad mínima de 11 nueves (99,999999999 %) de los objetos en un año determinado.

LRS es la opción de redundancia de costo más bajo y ofrece la menor durabilidad en comparación con otras opciones. LRS protege los datos frente a errores en la estantería de servidores y en la unidad. No obstante, si se produce un desastre como un incendio o una inundación en el centro de datos, es posible que todas las réplicas de una cuenta de almacenamiento con LRS se pierdan o no se puedan recuperar. Para mitigar este riesgo, Microsoft recomienda el uso del almacenamiento con redundancia de zona (ZRS), el almacenamiento con redundancia geográfica (GRS) o el almacenamiento con redundancia de zona geográfica (GZRS).

## Almacenamiento con redundancia de zona

Para las regiones con zona de disponibilidad habilitada, el almacenamiento con redundancia de zona (ZRS) replica los datos de Azure Storage sincrónicamente en tres zonas de disponibilidad de Azure en la región primaria. ZRS proporciona a los objetos de datos de Azure Storage una durabilidad de al menos 12 nueves (99,9999999999 %) durante un año determinado.

## Almacenamiento con redundancia geográfica

GRS copia los datos de manera sincrónica tres veces dentro de una ubicación física única en la región primaria mediante LRS. Luego copia los datos de forma asincrónica en una única ubicación física en la región secundaria (el par de regiones) mediante LRS. GRS proporciona a los objetos de datos de Azure Storage una durabilidad de al menos 16 nueves (99,99999999999999 %) durante un año determinado.

## Almacenamiento con redundancia de zona geográfica ( la mas )

GZRS combina la alta disponibilidad que proporciona la redundancia entre zonas de disponibilidad con la protección frente a interrupciones regionales que proporciona la replicación geográfica. Los datos de una cuenta de almacenamiento de GZRS se almacenan en tres zonas de disponibilidad de Azure en la región primaria (de manera similar a ZRS) y también se replican en una región geográfica secundaria para protegerlos frente a desastres regionales. Microsoft recomienda el uso de GZRS en aplicaciones que requieran de coherencia, durabilidad y disponibilidad máximas, además de rendimiento excelente y resistencia para la recuperación ante desastres.

# Servicios de almacenamiento de Azure

## Blobs de Azure

un almacén de objetos que se puede escalar de forma masiva para datos de texto y binarios. También incluye compatibilidad con el análisis de macrodatos a través de Data Lake Storage Gen2.

 ## Azure Files
 
 Recursos compartidos de archivos administrados para implementaciones locales y en la nube.
 
## Colas de Azure

Un almacén de mensajería para mensajería confiable entre componentes de aplicación.


## Azure Disks

Volúmenes de almacenamiento en el nivel de bloque para máquinas virtuales de Azure.

# Blob Storage

Azure Blob Storage es una solución de almacenamiento de objetos para la nube. Puede almacenar grandes cantidades de datos, como datos de texto o binarios. Azure Blob Storage es no estructurado, lo que significa que no hay ninguna restricción en cuanto a los tipos de datos que puede contener.

Los blobs no están limitados a formatos de archivo comunes. Un blob podría contener gigabytes de datos binarios transmitidos desde un instrumento científico, un mensaje cifrado para otra aplicación o datos en un formato personalizado para una aplicación que se está desarrollando. 

Azure Storage ofrece diferentes niveles de acceso para el almacenamiento de blobs, lo que le ayuda a almacenar datos de objetos de la manera más rentable. Entre los niveles de acceso disponibles se incluyen:

***Nivel de acceso frecuente:*** optimizado para almacenar datos a los que se accede con frecuencia (por ejemplo, imágenes para el sitio web).

***Nivel de acceso esporádico:*** optimizado para datos a los que se accede con poca frecuencia y que se almacenan al menos durante 30 días (por ejemplo, las facturas de los clientes).

***Nivel de acceso de archivo:*** conveniente para datos a los que raramente se accede y que se almacenan durante al menos 180 días con requisitos de latencia flexibles (por ejemplo, copias de seguridad a largo plazo).



# Azure Files


Azure Files ofrece recursos compartidos de archivos totalmente administrados en la nube a los que se puede acceder mediante los protocolos SMB (Bloque de mensajes del servidor) o NFS (Network File System) estándar del sector. Los recursos compartido de archivos de Azure Files se pueden montar simultáneamente mediante implementaciones locales o en la nube. 

# Queue Storage

Azure Queue Storage es un servicio para almacenar grandes cantidades de mensajes, Una vez que están almacenados, se puede acceder a los mensajes desde cualquier lugar del mundo mediante llamadas autenticadas con HTTP o HTTPS. Una cola puede contener tantos mensajes como el espacio que tenga la cuenta de almacenamiento (pueden ser millones). Cada mensaje individual de la cola puede llegar a tener un tamaño máximo de 64 KB. Las colas se utilizan normalmente para crear un trabajo pendiente del trabajo que se va a procesar de forma asincrónica.

Queue Storage se puede combinar con funciones de proceso como Azure Functions para realizar una acción cuando se recibe un mensaje. Por ejemplo, supongamos que quiere realizar una acción después de que un cliente cargue un formulario en el sitio web. Podría hacer que el botón enviar en el sitio web desencadene un mensaje en Queue Storage. Después, podría usar Azure Functions para desencadenar una acción una vez recibido el mensaje.

# Disk Storage

El almacenamiento en disco o los discos administrados de Azure son volúmenes de almacenamiento de nivel de bloque que administra Azure para su uso con máquinas virtuales de Azure. Conceptualmente, son iguales que un disco físico, pero están virtualizados, lo que ofrece mayor resistencia y disponibilidad que un disco físico. Con los discos administrados, lo único que debe hacer es aprovisionar el disco; Azure se encargará del resto.

# opciones de migración de datos de Azure

## Azure Migrate

Azure Migrate es un servicio que le ayuda a migrar desde un entorno local a la nube. Azure Migrate funciona como centro para ayudarle a administrar la valoración y la migración del centro de datos local a Azure.

## Azure Data Box

Azure Data Box es un servicio de migración física que ayuda a transferir grandes cantidades de datos de forma rápida, económica y confiable. La transferencia de datos segura se acelera mediante el envío de un dispositivo de almacenamiento propietario de Data Box que tiene una capacidad de almacenamiento utilizable máxima de 80 terabytes. Data Box se transporta hacia y desde el centro de datos a través de un transportista regional. Una caja resistente asegura y protege Data Box de daños durante el trayecto.

Data Box es ideal para transferir tamaños de datos con más de 40 TB en escenarios sin conectividad de red limitada. El movimiento de datos puede ser único, periódico o una transferencia de datos masiva inicial seguida de transferencias periódicas.

# Opciones de movimiento de archivos de Azure

## AzCopy

AzCopy es una utilidad de línea de comandos que puede usar para copiar blobs o archivos a una cuenta de almacenamiento o desde una cuenta de almacenamiento. Con AzCopy, puede copiar archivos entre cuentas de almacenamiento, cargarlos, descargarlos e incluso sincronizarlos. AzCopy incluso se puede configurar para trabajar con otros proveedores de nube para ayudar a mover archivos entre nubes.

## Explorador de Azure Storage

Explorador de Azure Storage es una aplicación independiente que proporciona una interfaz gráfica para administrar archivos y blobs en la cuenta de Azure Storage. Funciona en sistemas operativos Windows, macOS y Linux y usa AzCopy en el back-end para realizar todas las tareas de administración de archivos y blobs. Con Explorador de Storage, puede cargar en Azure, descargar desde Azure o moverse entre cuentas de almacenamiento.

### Azure File Sync

Es una herramienta que permite centralizar los archivos compartidos en Azure Files y mantener la flexibilidad, el rendimiento y la compatibilidad de un servidor de archivos de Windows. Es casi como convertir el servidor de archivos de Windows en una red de entrega de contenido en miniatura. Una vez que instale Azure File Sync en el servidor local de Windows, se mantendrá sincronizado bidireccionalmente con los archivos en Azure de forma automática.

Con Azure File Sync, puede:

Usar cualquier protocolo disponible en Windows Server para acceder a sus datos de forma local, como SMB, NFS y FTPS.
Tener todas las cachés que necesite en todo el mundo.
Reemplazar un servidor local con errores instalando Azure File Sync en un nuevo servidor del mismo centro de datos.
Configurar la nube por niveles para que los archivos a los que se accede con más frecuencia se repliquen localmente, mientras que los archivos a los que se accede con poca frecuencia se mantienen en la nube hasta que se soliciten.


#  Active Directory no es igual a Azure AD

> Si protege las identidades de forma local con Active Directory, Microsoft no supervisa los intentos de inicio de sesión. Si conecta Active Directory con Azure AD, Microsoft puede detectar intentos de inicio de sesión sospechosos para ayudarle a proteger su entorno sin costo adicional. Por ejemplo, Azure AD puede detectar intentos de inicio de sesión desde ubicaciones inesperadas o dispositivos desconocidos.

> Si tuviera un entorno local que ejecuta Active Directory y una implementación en la nube mediante Azure AD, tendría que mantener dos conjuntos de identidades. Pero puede conectar Active Directory con Azure AD, lo que permite una experiencia de identidad coherente entre la nube y el entorno local.

> Un método de conectar Azure AD con el AD local es usar Azure AD Connect. Azure AD Connect sincroniza las identidades de usuario entre la instalación local de Active Directory y Azure AD. Azure AD Connect sincroniza los cambios entre ambos sistemas de identidades, para que pueda usar características como SSO, la autenticación multifactor y el autoservicio de restablecimiento de contraseña en ambos sistemas.


# Azure Active Directory Domain Services


Azure Active Directory Domain Services (Azure AD DS) es un servicio que proporciona ***servicios de dominio administrados*** como, por ejemplo, unión a un dominio, directivas de grupo, protocolo ligero de acceso a directorios (LDAP) y autenticación Kerberos o NTLM. Al igual que Azure AD le permite usar servicios de directorio sin tener que mantener la infraestructura que lo admite, gracias a Azure AD DS obtiene la ventaja de los servicios de dominio sin necesidad de implementar, administrar y aplicar revisiones a los controladores de dominio (DC) en la nube



## ¿Cómo funciona Azure AD DS?

Cuando cree un dominio administrado de Azure AD DS, defina un espacio de nombres único. Este espacio de nombres es el nombre de dominio. Después, se implementan dos controladores de dominio de Windows Server en la región de Azure seleccionada. Esta implementación de controladores de dominio se conoce como "conjunto de réplicas".

No es necesario administrar, configurar ni actualizar estos controladores de dominio. La plataforma Azure administra los controladores de dominio como parte del dominio administrado, incluidas las copias de seguridad y el cifrado en reposo mediante Azure Disk Encryption.

> Las aplicaciones, los servicios y las máquinas virtuales de Azure que se conectan al dominio administrado pueden usar las características de Azure AD DS comunes, como unión a un dominio, directiva de grupo, LDAP y autenticación Kerberos o NTLM. 

# Métodos de autenticación de Azure

> Azure admite varios métodos de autenticación, incluidas las contraseñas estándar, el inicio de sesión único (SSO), la autenticación multifactor (MFA) y el acceso sin contraseña.

##  Inicio de sesión único (SSO)




























