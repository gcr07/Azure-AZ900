# Azure Certification

# Link del portal de Azure

> https://portal.azure.com

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

>  permite a los usuarios iniciar sesión una vez y utilizar esa credencial para acceder a varios recursos y aplicaciones de distintos proveedores. Para que el inicio de sesión único funcione, las distintas aplicaciones y proveedores deben confiar en el autenticador inicial.

## Azure AD Multi-Factor Authentication

Azure AD Multi-Factor Authentication es un servicio de Microsoft que proporciona funcionalidades de autenticación multifactor. Azure AD Multi-Factor Authentication permite a los usuarios elegir una forma adicional de autenticación durante el inicio de sesión, como una llamada de teléfono o una notificación de aplicación móvil.

## Microsoft Azure global y Azure Government

 las siguientes tres opciones de autenticación sin contraseña que se integran con Azure Active Directory (Azure AD):

### Windows Hello para empresas

Windows Hello para empresas resulta muy conveniente para los trabajadores de la información que tienen su propio equipo con Windows designado. La información biométrica y las credenciales de PIN están vinculadas directamente al equipo del usuario, lo que impide el acceso de cualquier persona que no sea el propietario. Con la integración de la infraestructura de clave pública (PKI) y la compatibilidad integrada con el inicio de sesión único (SSO), Windows Hello para empresas ofrece un método sencillo y práctico de acceder directamente a los recursos corporativos del entorno local y la nube.

### Aplicación Microsoft Authenticator

También puede permitir que el teléfono del empleado se convierta en un método de autenticación sin contraseña. Es posible que ya esté usando la aplicación Microsoft Authenticator como una opción de autenticación multifactor cómoda sumada a una contraseña. También puede usar la aplicación Authenticator como una opción sin contraseña.

### Claves de seguridad FIDO2

Los usuarios pueden registrarse y luego seleccionar una llave de seguridad de FIDO2 en la interfaz de inicio de sesión como medio principal de autenticación. Estas llaves de seguridad de FIDO2 suelen ser dispositivos USB, pero también pueden usar Bluetooth o NFC. Con un dispositivo de hardware que controla la autenticación, se aumenta la seguridad de una cuenta, ya que no hay ninguna contraseña que pueda quedar expuesta ni adivinarse

# Identidades externas de Azure (  Azure AD External Identities )

Una identidad externa es una persona, un dispositivo, un servicio, etc. que está fuera de la organización. Azure AD External Identities hace referencia a todas las formas en que puede interactuar de forma segura con usuarios externos a su organización. Si quiere colaborar con asociados, distribuidores o proveedores, puede compartir los recursos y definir cómo los usuarios internos pueden acceder a organizaciones externas. Si es un desarrollador que crea aplicaciones orientadas al consumidor, puede administrar las experiencias de identidad de los clientes.

Las identidades externas pueden parecerse al inicio de sesión único. Con External Identities, los usuarios externos pueden "traer sus propias identidades". Tanto si tienen una identidad digital corporativa o gubernamental, como una identidad social no administrada, como Google o Facebook, pueden usar sus propias credenciales para iniciar sesión. El proveedor de identidades administra la identidad del usuario externo y el usuario administra el acceso a sus aplicaciones con Azure AD o Azure AD B2C para mantener protegidos los recursos.

## Acceso condicional de Azure

El acceso condicional es una herramienta que usa Azure Active Directory para permitir (o denegar) el acceso a los recursos en función de señales de identidad. Estas señales incluyen quién es el usuario, dónde se encuentra y desde qué dispositivo solicita el acceso.

La aplicación es la acción que lleva a cabo la decisión. Por ejemplo, la acción es permitir el acceso o exigir al usuario que proporcione una segunda forma de autenticación.

## Control de acceso basado en roles de Azure

Cuando tenemos varios equipos de TI e ingeniería, ¿cómo podemos controlar el acceso que tienen a los recursos del entorno de nube? El principio de privilegios mínimos indica que solo debe conceder acceso al nivel necesario para completar una tarea. Si solo necesita acceso de lectura a un blob de almacenamiento, solo se le debe conceder acceso de lectura a ese blob de almacenamiento. No se debe conceder acceso de escritura a ese blob ni debe tener acceso de lectura a otros blobs de almacenamiento. Es una buena práctica de seguridad seguir.

Pero, administrar ese nivel de permisos para todo el equipo se volvería tedioso. En vez de definir los requisitos de acceso detallados de cada individuo y, después, ir actualizándolos a medida que se vayan creando más recursos o se unan nuevos miembros al equipo, Azure permite controlar el acceso a través del ***control de acceso basado en roles de Azure (RBAC de Azure).****

> Azure proporciona roles integrados que describen las reglas de acceso comunes de los recursos en la nube. También podemos definir nuestros propios roles. Cada rol tiene un conjunto asociado de permisos de acceso que tienen que ver con ese rol. Cuando se asignan usuarios o grupos a uno o varios roles, reciben todos los permisos de acceso asociados.

## ¿Cómo se aplica el control de acceso basado en roles a los recursos?

El control de acceso basado en roles se aplica a un ámbito, que es un recurso o un conjunto de recursos en los que este acceso se permite.

Los ámbitos pueden ser lo siguiente:

1. Un grupo de administración (una colección de varias suscripciones)
2. Una sola suscripción
3. Un grupo de recursos.
4. Un solo recurso

# Azure Resource Manager ¿Cómo se aplica RBAC de Azure?

RBAC de Azure se aplica a cualquier acción que se inicie en un recurso de Azure que pasa por Azure Resource Manager. Resource Manager es un servicio de administración que proporciona una forma de organizar y proteger nuestros recursos en la nube.

Normalmente, se accede a Resource Manager a través de Azure Portal, Azure Cloud Shell, Azure PowerShell y la CLI de Azure. RBAC de Azure no aplica permisos de acceso en el nivel de aplicación ni de datos. La seguridad de la aplicación debe controlarla la propia aplicación.


# Modelo de Confianza cero

Confianza cero es un modelo de seguridad que supone el peor de los escenarios posibles y protege los recursos con esa expectativa. Confianza cero presupone que hay una vulneración y comprueba todas las solicitudes como si provinieran de una red no controlada.

Para abordar este nuevo mundo informático, Microsoft recomienda encarecidamente el modelo de seguridad de Confianza cero, que se basa en estos principios rectores:

### Comprobar explícitamente: 

realice siempre las operaciones de autorización y autenticación en función de todos los puntos de datos disponibles.

### Usar el acceso de privilegios mínimos:

limite el acceso de los usuarios con Just-in-Time y Just-Enough-Access (JIT/JEA), directivas que se adaptan al nivel de riesgo y protección de datos.

### Asumir que hay brechas: 

minimice el radio de expansión y el acceso a los segmentos. Comprobación del cifrado de un extremo a otro. Utilice el análisis para obtener visibilidad, impulsar la detección de amenazas y mejorar las defensas.


# Defensa en profundidad

El objetivo de la defensa en profundidad es proteger la información y evitar que personas no autorizadas a acceder puedan sustraerla.

Una estrategia de defensa en profundidad usa una serie de mecanismos para ralentizar el avance de un ataque dirigido a adquirir acceso no autorizado a los datos.


# Capas de defensa en profundidad


Aquí tiene una breve descripción del rol de cada capa:

## La capa de seguridad física

Es la primera línea de defensa para proteger el hardware informático del centro de datos.

## La capa de identidad y acceso

Controla el acceso a la infraestructura y al control de cambios.

## La capa perimetral 

Usa protección frente a ataques de denegación de servicio distribuido (DDoS) para filtrar los ataques a gran escala antes de que puedan causar una denegación de servicio para los usuarios.

## La capa de red

Limita la comunicación entre los recursos a través de controles de acceso y segmentación.

## La capa de proceso

Protege el acceso a las máquinas virtuales.

## La capa de aplicación

Ayuda a garantizar que las aplicaciones sean seguras y estén libres de vulnerabilidades de seguridad.

## La capa de datos 

Controla el acceso a los datos empresariales y de clientes que es necesario proteger.

# Microsoft Defender for Cloud

Microsoft Defender for Cloud es una herramienta de supervisión para la administración de la posición de seguridad y la protección contra amenazas. Supervisa los entornos en la nube, locales, híbridos y multinube para ofrecer instrucciones y notificaciones destinadas a reforzar la posición de seguridad.

Defender for Cloud proporciona las herramientas necesarias para proteger los recursos, realizar un seguimiento de su posición de seguridad, protegerse frente a ciberataques y simplificar la administración de la seguridad. La implementación de Defender for Cloud es fácil, ya está integrada de forma nativa en Azure.

> Dado que Defender for Cloud es un servicio nativo de Azure, muchos servicios de Azure se supervisan y protegen sin necesidad de ninguna implementación. 


Cuando sea necesario, Defender for Cloud puede implementar automáticamente un agente de Log Analytics para recopilar datos relacionados con la seguridad. En el caso de las máquinas de Azure, la implementación se controla directamente. Para entornos híbridos y de varias nubes, los planes de Microsoft Defender se amplían a máquinas que no son de Azure con la ayuda de Azure Arc. Las características de la Administración de la posición de seguridad en la nube (CSPM) se amplían a máquinas de varias nubes sin necesidad de ningún agente.


***Cloud Security Posture Management (CSPM)****

Cuando sea necesario, Defender for Cloud puede implementar automáticamente un agente de Log Analytics para recopilar datos relacionados con la seguridad. En el caso de las máquinas de Azure, la implementación se controla directamente. Para entornos híbridos y de varias nubes, los planes de Microsoft Defender se amplían a máquinas que no son de Azure con la ayuda de Azure Arc. Las características de la Administración de la posición de seguridad en la nube (CSPM) se amplían a máquinas de varias nubes sin necesidad de ningún agente.

Se puede convinar esto con AWS 

Microsoft Defender para servidores proporciona la detección de amenazas y defensas avanzadas a las instancias de EC2 con Windows y Linux.

## Evaluación, protección y defensa

Defender for Cloud cubre tres necesidades vitales a medida que administra la seguridad de los recursos y las cargas de trabajo en la nube y en el entorno local:

Evaluación continua: conozca la posición de seguridad. Identifique y realice un seguimiento de las vulnerabilidades.

Protección: proteja los recursos y los servicios con Azure Security Benchmark.

Defensa: detecte y resuelva las amenazas a recursos, cargas de trabajo y servicios.

# Azure Security Benchmark. 

Este punto de referencia es el conjunto de directrices específico de Azure y creado por Microsoft relativo a los procedimientos recomendados de seguridad y cumplimiento basados en marcos de cumplimiento comunes.

The Azure Security Benchmark contains recommendations that help you improve the security of your applications and data on Azure.


# Cuentas de Azure

uando trabaje con aplicaciones y necesidades empresariales propias, tendrá que crear una cuenta de Azure y se creará una suscripción de forma automática. Después de crear una cuenta de Azure, puede crear suscripciones adicionales. Por ejemplo, es posible que la empresa use una única cuenta de Azure para el negocio y suscripciones independientes para los departamentos de desarrollo, marketing y ventas. Una vez que ha creado una suscripción de Azure, puede empezar a crear recursos de Azure dentro de cada suscripción.

# Regions

Una región es un área geográfica del planeta que contiene al menos un centro de datos, aunque podrían ser varios cercanos y conectados mediante una red de baja latencia. Azure asigna y controla los recursos de forma inteligente dentro de cada región para garantizar que las cargas de trabajo están bien compensadas.



Como proveedor de nube global, Azure tiene centros de datos en todo el mundo. Pero estos centros de datos individuales no son accesibles directamente. Los centros de datos se agrupan en regiones de Azure o Azure Availability Zones, están diseñados para ayudarle a lograr resistencia y confiabilidad para las cargas de trabajo críticas para la empresa.

## Availability Zones

Las zonas de disponibilidad son centros de datos separados físicamente dentro de una región de Azure. Cada zona de disponibilidad consta de uno o varios centros de datos equipados con alimentación, refrigeración y redes independientes. Una zona de disponibilidad se configura para constituir un límite de aislamiento. Si una zona deja de funcionar, la otra continúa trabajando. Las zonas de disponibilidad están conectadas a través de redes de fibra óptica de alta velocidad privadas.

> Para garantizar la resistencia, se configuran un mínimo de tres zonas de disponibilidad independientes en todas las regiones habilitadas. Pero no todas las regiones de Azure admiten actualmente las zonas de disponibilidad.


>Pares de región
> La mayoría de las regiones de Azure se emparejan con otra región de la misma zona geográfica (por ejemplo, EE. UU., Europa o Asia) que se encuentre como mínimo a 500 km de distancia. Este enfoque permite la replicación de recursos en una zona geográfica que ayuda a reducir la probabilidad de que se produzcan interrupciones provocadas por eventos como desastres naturales, disturbios sociales, cortes del suministro eléctrico o interrupciones de la red física que afecten a una región completa. Por ejemplo, si una región de un par se ve afectada por un desastre natural, los servicios conmutarán por error automáticamente a la otra región de su par de regiones.

## Regiones soberanas

Además de las regiones normales, Azure también tiene regiones soberanas. Las regiones soberanas son instancias de Azure que están aisladas de la instancia principal de Azure. Es posible que tenga que usar una región soberana con fines legales o de cumplimiento.

Entre las regiones soberanas de Azure se incluyen las siguientes:

US DoD (centro), US Gov Virginia, US Gov Iowa y más: Estas regiones son instancias físicas y lógicas con aislamiento de red de Azure para asociados y agencias de la administración pública de EE. UU. Estos centros de datos están operados por personal estadounidense sometido a evaluación e incluyen certificaciones de cumplimiento adicionales.
Este de China, Norte de China y más: Estas regiones están disponibles gracias a una asociación exclusiva entre Microsoft y 21Vianet, por la cual Microsoft no mantiene directamente los centros de datos.

#  Infraestructura de administración de Azure

La infraestructura de administración incluye recursos de Azure y grupos de recursos, suscripciones y cuentas. Comprender la organización jerárquica le ayudará a planear los proyectos y productos dentro de Azure.


Un recurso es el bloque de creación básico de Azure. Todo lo que cree, aprovisione, implemente, etc., es un recurso. Máquinas virtuales (VM), redes virtuales, bases de datos, servicios cognitivos, etc., se consideran recursos dentro de Azure.

Los grupos de recursos son simplemente agrupaciones de recursos. Al crear un recurso, es necesario colocarlo en un grupo de recursos. Aunque un grupo de recursos puede contener muchos recursos, un único recurso solo puede estar en un grupo de recursos a la vez.

Es posible que algunos recursos se muevan entre grupos de recursos, pero al mover un recurso a un nuevo grupo, ya no estará asociado al grupo anterior. Además, los grupos de recursos no se pueden anidar, lo que significa que no se puede colocar el grupo de recursos B dentro del grupo de recursos A.


# Suscripciones de Azure

El uso de Azure requiere una suscripción de Azure. Una suscripción le proporciona acceso autenticado y autorizado a los servicios y productos de Azure. Además, también le permite aprovisionar los recursos. Una suscripción de Azure se vincula a una cuenta de Azure, que es una identidad en Azure Active Directory (Azure AD) o en un directorio en el que Azure AD confía.

Una cuenta puede tener varias suscripciones, pero solo es obligatorio tener una. En una cuenta de varias suscripciones, puede usarlas para configurar diferentes modelos de facturación y aplicar diferentes directivas de administración de acceso. Puede usar las suscripciones de Azure para definir límites en torno a los productos, servicios y recursos de Azure. Hay dos tipos de límites de suscripción que puede utilizar:

Límite de facturación: Este tipo de suscripción determina cómo se factura una cuenta de Azure por el uso de Azure. Puede crear varias suscripciones para diferentes tipos de requisitos de facturación. Azure genera facturas e informes de facturación independientes para cada suscripción, de modo que pueda organizar y administrar los costos.

Límite de control de acceso: Azure aplica las directivas de administración de acceso en el nivel de suscripción, por lo que puede crear suscripciones independientes para reflejar distintas estructuras organizativas. Por ejemplo, dentro de una empresa hay diferentes departamentos a los que se pueden aplicar directivas de suscripción de Azure distintas. Este modelo de facturación le permite administrar y controlar el acceso a los recursos que los usuarios aprovisionan con suscripciones específicas.

OSea para separar departamentos por ejemplo

# Grupos de administración de Azure

 Los grupos de administración de Azure proporcionan un nivel de ámbito por encima de las suscripciones. Las suscripciones se organizan en contenedores llamados grupos de administración, a los que se aplican condiciones de gobernanza. Todas las suscripciones de un grupo de administración heredan automáticamente las condiciones que tenga aplicadas, de la misma manera que los grupos de recursos heredan la configuración de las suscripciones y los recursos heredan de los grupos de recursos. Los grupos de administración proporcionan capacidad de administración de nivel empresarial a gran escala con independencia del tipo de suscripciones que tenga. Los grupos de administración se pueden anidar.
 
 
# Azure Blueprints



Azure Blueprints le permite estandarizar las implementaciones de entorno o suscripción en la nube. En lugar de tener que configurar características como Azure Policy para cada nueva suscripción, con Azure Blueprints puede definir la configuración repetible y las directivas que se aplican a medida que se crean suscripciones. ¿Necesita un nuevo entorno de pruebas y desarrollo? Azure Blueprints permite implementar un nuevo entorno de pruebas y desarrollo con las opciones de seguridad y cumplimiento ya configuradas. De este modo, los equipos de desarrollo pueden crear e implementar rápidamente nuevos entornos sabiendo que se crean de acuerdo con los estándares organizativos.

Cada componente de la definición de un plano técnico se denomina artefacto.

Azure Blueprints implementa un nuevo entorno en función de todos los requisitos, las opciones y las configuraciones de los artefactos asociados. Los artefactos pueden incluir cosas como las siguientes:

Asignaciones de roles
Asignaciones de directivas
Plantillas de Azure Resource Manager
Grupos de recursos
 
# Azure Policy

¿Cómo puede asegurarse de que estos recursos mantengan su cumplimiento? ¿Puede recibir un aviso cuando la configuración de un recurso cambie?

Azure Policy es un servicio de Azure que permite crear, asignar y administrar directivas que controlan o auditan los recursos. Dichas directivas aplican distintas reglas en las configuraciones de los recursos para que esas configuraciones sigan cumpliendo con los estándares corporativos.


Azure Policy permite definir tanto directivas individuales como grupos de directivas relacionadas, lo que se conoce como iniciativas. Azure Policy evalúa los recursos y resalta los que no cumplen las directivas que hemos creado. Azure Policy también puede impedir que se creen recursos no conformes.

Las directivas de Azure se pueden establecer en cada nivel, lo que le permite establecer directivas en un recurso específico, un grupo de recursos, una suscripción, etc. Además, las directivas de Azure se heredan, por lo que si establece una directiva de nivel alto, se aplicará automáticamente a todas las agrupaciones que se encuentran dentro del elemento primario. 

## Iniciativas Azure Policy

Una iniciativa de Azure Policy es una forma de agrupar las directivas relacionadas. La definición de iniciativa contiene todas las definiciones de directiva para facilitar el seguimiento del estado de cumplimiento de cara a un objetivo mayor.

Por ejemplo, Azure Policy incluye una iniciativa denominada Habilitar la supervisión en Azure Security Center, Su objetivo es supervisar todas las recomendaciones de seguridad disponibles para todos los tipos de recursos de Azure en Azure Security Center.

#  Bloqueos de recursos

Aun cuando haya directivas de control de acceso basado en roles de Azure (RBAC de Azure) en vigor, sigue existiendo el riesgo de que alguien con el nivel de acceso adecuado elimine recursos de nube críticos. Los bloqueos de recursos impiden que los recursos se eliminen o actualicen, según el tipo de bloqueo. Los bloqueos de recursos se pueden aplicar a recursos individuales, grupos de recursos o incluso a una suscripción completa. Los bloqueos de recursos se heredan, lo que significa que si coloca un bloqueo de recursos en un grupo de recursos, también se aplicará el bloqueo a todos los recursos dentro del grupo.


## Tipos de bloqueos de recursos

Hay dos tipos de bloqueos de recursos, uno que impide que los usuarios eliminen un recurso y otro que impide que los usuarios lo cambien o eliminen.

Eliminar significa que los usuarios autorizados pueden leer y modificar un recurso, pero no eliminarlo.
ReadOnly significa que los usuarios autorizados solo pueden leer recursos, pero no actualizarlos ni eliminarlos. Aplicar este bloqueo es similar a restringir todos los usuarios autorizados a los permisos concedidos por el rol Lector.


## ¿Cómo se elimina o cambia un recurso bloqueado?

Para modificar un recurso bloqueado, primero hay que quitar el bloqueo. Tras quitarlo, podemos aplicar cualquier acción que podamos realizar de acuerdo a nuestros permisos. Los bloqueos de recursos se aplican con independencia de los permisos RBAC. Es decir, aun siendo el propietario del recurso, tendremos que quitar el bloqueo antes de poder realizar la actividad bloqueada.




# Azure Portal

The Azure portal is a web-based, unified console that provides an alternative to command-line tools. With the Azure portal, you can manage your Azure subscription using a graphical user interface. You can build, manage, and monitor everything from simple web apps to complex cloud deployments in the portal

# The Azure Command-Line Interface (CLI)

Is a cross-platform command-line tool to connect to Azure and execute administrative commands on Azure resources. It allows the execution of commands through a terminal using interactive command-line prompts or a script.

The Azure command-line interface (Azure CLI) is a set of commands used to create and manage Azure resources. The Azure CLI is available across Azure services and is designed to get you working quickly with Azure, with an emphasis on automation


# Azure Cloud Shell

> en resumen Azure Cloud Shell ( padre ) , incluida la CLI de Azure (bash)  y Azure PowerShell ( PowerShell para WIN)

Es como la Aws console que le picas en el portal y te abre una linea de comandos.
Tendrá la opción de elegir entre PowerShell o Bash. Si desea administrar máquinas virtuales basadas en Windows, elegirá PowerShell; por otro lado, si desea administrar máquinas virtuales Linux, Bash es la opción que necesita.

Dicho esto, tiene la CLI de Azure, que se usa para emitir un conjunto de comandos para agregar, eliminar o modificar recursos en Azure. Con eso me refiero a los recursos reales de Azure y no al sistema operativo que reside en los recursos. La CLI de Azure está disponible en las secciones Bash y PowerShell de Azure Cloud Shell.

¿Qué es Azure Cloud Shell?
Azure Cloud Shell es un entorno de shell hospedado que se ejecuta en un contenedor de Ubuntu.

Cloud Shell proporciona dos entornos de shell: Bash (con la CLI de Azure preinstalada) y PowerShell (con Azure PowerShell preinstalado). Una lista desplegable en la parte superior de la ventana de Cloud Shell le permite cambiar fácilmente entre los dos entornos.

Cloud Shell es accesible en un explorador web y tiene integraciones para terminal de Windows y Visual Studio Code.

# Azure Resource Manager  Azure Resource Manager (ARM), Arc

La administración de entornos híbridos y de varias nubes puede complicarse rápidamente. Azure proporciona una serie de herramientas para aprovisionar, configurar y supervisar recursos de Azure. ¿Qué ocurre con los recursos locales en una configuración híbrida o los recursos de nube en una configuración de varias nubes?

Al usar Azure Resource Manager (ARM), Arc le permite ampliar el cumplimiento y la supervisión de Azure a las configuraciones híbridas y de varias nubes. Azure Arc simplifica el gobierno y la administración al ofrecer una plataforma de administración local y multinube coherente.

# Acceso al Portal de confianza de servicios

> Puede acceder al Portal de confianza de servicios en https://servicetrust.microsoft.com/

El Portal de confianza de servicios de Microsoft es un portal que proporciona contenido, herramientas y otros recursos sobre las prácticas de seguridad, privacidad y cumplimiento de Microsoft.

## Reglamento general de protección de datos; documentación útil para la responsabilidad del RGPD



#  Las plantillas de Azure Resource Manager y Azure ARM  Infraestructuras como código (IaC)

Es lo mismo 

ARM agrupa los recursos en contenedores que reúnen los activos de Azure. Resources Manager se puede usar para desplegar activos de múltiples servicios de proveedores Azure como Microsoft Storage o Microsoft Compute.


Azure Resource Manager (ARM) es el servicio de implementación y administración de Azure. Proporciona una capa de administración que le permite crear, actualizar y eliminar recursos de la cuenta de Azure. Cada vez que haga algo con los recursos de Azure, ARM está implicado.

Cuando un usuario envía una solicitud de cualquiera de las herramientas, API o SDK de Azure, ARM la recibe. ARM autentica y autoriza la solicitud. Después, ARM envía la solicitud al servicio de Azure, que lleva a cabo la acción solicitada. Verá resultados y funcionalidades coherentes en todas las herramientas, ya que todas las solicitudes se controlan mediante la misma API.


Administrar la infraestructura mediante plantillas declarativas en lugar de scripts. Una plantilla de Resource Manager es un archivo JSON que define lo que quiere implementar en Azure.



#  Herramientas de supervisión de Azure

# Azure Advisor

Azure Advisor evalúa los recursos de Azure y hace recomendaciones que contribuyen a mejorar la confiabilidad, la seguridad y el rendimiento, lograr la excelencia operativa y reducir los costos. Azure Advisor está diseñado para ayudarle a ahorrar tiempo en la optimización en la nube. El servicio de recomendaciones sugiere medidas que puede adoptar de inmediato, posponer o descartar.

# Azure Service Health

Microsoft Azure proporciona una solución global en la nube para ayudarle a administrar sus necesidades de infraestructura, llegar a sus clientes, innovar y adaptarse rápidamente. Conocer el estado de la infraestructura global de Azure y los recursos individuales podría parecer una tarea abrumadora. Azure Service Health le permite realizar un seguimiento de los recursos de Azure, tanto los recursos implementados específicamente como el estado general de Azure. Azure Service Health lo hace combinando tres servicios de Azure diferentes:

Con el Estado de Azure, Service Health y Resource Health, Azure Service Health ofrece una vista completa de todo el entorno de Azure, desde el estado global de los servicios y regiones de Azure hasta los recursos específicos. Además, las alertas históricas se almacenan y son accesibles para su revisión posterior. Algo que inicialmente pensó que era una simple anomalía que se ha convertido en una tendencia, se puede revisar e investigar fácilmente gracias a las alertas históricas.

# Azure Monitor

Azure Monitor es una plataforma para recopilar datos sobre los recursos, analizar esos datos, visualizar la información e incluso actuar en función de los resultados. Azure Monitor puede supervisar los recursos de Azure, los recursos locales e incluso los recursos de varias nubes, como las máquinas virtuales hospedadas con otro proveedor de nube.

Además, puede usar los datos para ayudarle a reaccionar ante eventos críticos en tiempo real gracias a las alertas enviadas a los equipos por SMS, correo electrónico, etc. También puede usar umbrales que desencadenen la funcionalidad de escalado automático para ajustarse a la demanda.

# Azure Log Analytics

Azure Log Analytics es la herramienta de Azure Portal donde escribirá y ejecutará consultas de registro en los datos recopilados por Azure Monitor. Log Analytics es una herramienta sólida que admite consultas sencillas, complejas y análisis de datos. Puede escribir una consulta sencilla que devuelva un conjunto de registros y, después, usar las características de Log Analytics para ordenarlos, filtrarlos y analizarlos. Puede escribir una consulta avanzada para realizar análisis estadísticos y visualizar los resultados en un gráfico para identificar una tendencia determinada. Tanto si trabaja con los resultados de las consultas de forma interactiva como si los usa con otras características de Azure Monitor, como las alertas de consultas de registros o los libros, Log Analytics es la herramienta que va a usar para escribir y probar esas consultas.

## Application Insights caracteristica de Azure Monitor 

Las alertas de Azure Monitor usan grupos de acciones para configurar a quién realizar la notificación y qué acción realizar. Un grupo de acciones es simplemente una colección de preferencias de notificaciones y acciones que se asocian a una o varias alertas. Azure Monitor, Service Health y Azure Advisor usan grupos de acciones para notificarle cuándo se ha desencadenado una alerta.



Application Insights, una característica de Azure Monitor, supervisa las aplicaciones web. Application Insights es capaz de supervisar aplicaciones que se ejecutan en Azure, en el entorno local o en otro entorno de nube.



# Costos

## Azure Cost Management

Cost Management proporciona la capacidad de comprobar rápidamente los costos de los recursos de Azure, crear alertas basadas en el gasto de recursos y crear presupuestos que se pueden usar para automatizar la administración de recursos.

Las alertas de costos proporcionan una única ubicación para comprobar rápidamente todos los diferentes tipos de alertas que pueden aparecer en el servicio Cost Management. Los tres tipos de alertas que pueden aparecer son las siguientes:

### Alertas de presupuesto
 
Las alertas de presupuesto le envían una notificación cuando el gasto, en función del uso o coste, alcanza o supera la cantidad definida en la condición de alerta del presupuesto. Los presupuestos de Cost Management se crean mediante Azure Portal o la API de consumo de Azure.


### Alertas de crédito

Las alertas de crédito le avisan cuando se consumen los compromisos monetarios de crédito de Azure. Los compromisos monetarios son para organizaciones con contratos Enterprise (EA). Las alertas de crédito se generan de forma automática al 90 % y al 100 % del saldo de crédito de Azure. Cada vez que se genera una alerta, se refleja en las alertas sobre los costos y en el correo electrónico que se envía a los propietarios de la cuenta.

### Alertas de cuota de gasto de departamento

Las alertas de cuota de gasto de departamento notifican cuándo el gasto del departamento alcanza un umbral fijo de la cuota. Las cuotas de gasto se configuran en el portal de EA. Cada vez que se alcanza un umbral, se genera un correo electrónico para los propietarios del departamento y se muestra en las alertas sobre los costos. Por ejemplo, el 50 % o el 75 % de la cuota.

### Presupuestos

Un presupuesto es donde se establece un límite de gasto para Azure. Puede establecer presupuestos basados en una suscripción, un grupo de recursos, un tipo de servicio u otros criterios. Al establecer un presupuesto, también establecerá una alerta de presupuesto. 


# Estudio

## AzCopy

AzCopy es una utilidad de línea de comandos que puede usar para copiar blobs o archivos a una cuenta de almacenamiento o desde una cuenta de almacenamiento. En este artículo sirve de ayuda para descargar AzCopy, conectarse a la cuenta de almacenamiento y, a continuación, transferir datos.

### Pregunta

Which of the following is the best approach when you need to copy large amount of files between two Azure Storage accounts?

##  Azure Private cloud ¿?

True or False: Azure is a public cloud, and has no private cloud offerings

Some aspects of Azure are not open to the public and require a private agreement with Microsoft such as Azure Government and DoD services<br>For more info: <a href='https://azure.microsoft.com/en-us/overview/what-are-private-public-hybrid-clouds/'>https://azure.microsoft.com/en-us/overview/what-are-private-public-hybrid-clouds/</a>



## Azure Policy

Azure Policy can add restrictions on storage account SKUs, virtual machine instance types, and rules relating to tagging of resources and groups. It cannot prompt a user to ask them if they are sure.

## Azure Consumption-based pricing model

The common pricing options for Azure services are: Consumption-based price - You are charged for only what you use. This model is also known as the Pay-As-You-Go rate. Fixed price - You provision resources and are charged for those instances whether or not they are used.

## Azure Time-based (Fixed) pricing model ( por ejemplo tu contratas una maquina virtual por 1 mes la uses o no te cobran 1 mes)

Fixed price - You provision resources and are charged for those instances whether or not they are used.

## Azure availability sets

## What is an availability set?

An availability set is a logical grouping of VMs that allows Azure to understand how your application is built to provide for redundancy and availability. We recommended that two or more VMs are created within an availability set to provide for a highly available application and to meet the 99.95% Azure SLA. There is no cost for the Availability Set itself, you only pay for each VM instance that you create.

### Pregunta 

What benefit does Availability Sets provide when it comes to virtual machines in Azure?

Separa fisica y logicamente maquinas virtuales y ya si una se cae la otra queda 


Availability Sets allow you to tell Azure which virtual machines are identical, so that Azure will keep them apart physically inside the datacenter. This helps when there are either expected or unexpected downtime, by increasing the chances that one issue does not affect all VMs in a single Availability Set.

## Microsoft Azure VM Scale Sets 

Are groups of individual virtual machines (VMs) within the Microsoft Azure public cloud that information technology (IT) administrators can configure and manage as a single unit. Administrators can use Azure VM Scale Sets to deploy complete services, rather than duplicate the same VMs.

That's correct. Virtual machine scale sets let you deploy and manage a set of identical virtual machines.



## What is Azure role-based access control (Azure RBAC)?

Access management for cloud resources is a critical function for any organization that is using the cloud. Azure role-based access control (Azure RBAC) helps you manage who has access to Azure resources, what they can do with those resources, and what areas they have access to.

Azure RBAC is an authorization system built on Azure Resource Manager that provides fine-grained access management to Azure resources.

## Azure Management group

An Azure Management group is logical containers that allow Azure Administrators to manage access, policy, and compliance across multiple Azure Subscriptions en masse.



# Azure Storage redundancy

Tarea hacer un resumen bueno

https://learn.microsoft.com/en-us/azure/storage/common/storage-redundancy

# Azure Availability Sets



# Que es redundancia

En ingeniería, la redundancia en datos1 es la duplicación o re-escritura de información con la intención de aumentar la confiabilidad del sistema, generalmente en forma de respaldo de almacenamiento o prueba de fallas.

## Azure Regional Pairs

An Azure region is an area within a geography containing one or more datacenters. Each Azure region is paired with another region within the same geography (with the exception of Brazil South which is paired with a region outside its geography), together making a regional pair.


# Azure App Service

This platform as a service (PaaS) environment allows you to focus on the website and API logic while Azure handles the infrastructure to run and scale your web applications.

# Cuando usar contenedores o Kubernetes ¿?

While virtual machines are an excellent way to reduce costs versus the investments that are necessary for physical hardware, they're still limited to a single operating system per virtual machine. If you want to run multiple instances of an application on a single host machine, containers are an excellent choice.

Containers are a virtualization environment. Much like running multiple virtual machines on a single physical host, you can run multiple containers on a single physical or virtual host. Unlike virtual machines, you don't manage the operating system for a container. Virtual machines appear to be an instance of an operating system that you can connect to and manage, but containers are lightweight and designed to be created, scaled out, and stopped dynamically. While it's possible to create and deploy virtual machines as application demand increases, containers are designed to allow you to respond to changes on demand. With containers, you can quickly restart in case of a crash or hardware interruption. One of the most popular container engines is Docker, which is supported by Azure.

Containers are managed through a container orchestrator, which can start, stop, and scale out application instances as needed. There are two ways to manage both Docker and Microsoft-based containers in Azure: Azure Container Instances and Azure Kubernetes Service (AKS).


## Azure Container Instances

Azure Container Instances offers the fastest and simplest way to run a container in Azure without having to manage any virtual machines or adopt any additional services. It's a platform as a service (PaaS) offering that allows you to upload your containers, which it runs for you.


## Azure Kubernetes Service

The task of automating, managing, and interacting with a large number of containers is known as orchestration. Azure Kubernetes Service is a complete orchestration service for containers with distributed architectures and large volumes of containers.


## Use containers in your solutions

Containers are often used to create solutions by using a microservice architecture. This architecture is where you break solutions into smaller, independent pieces. For example, you might split a website into a container hosting your front end, another hosting your back end, and a third for storage. This split allows you to separate portions of your app into logical sections that can be maintained, scaled, or updated independently.

# Serverless

## Azure Functions


When you're concerned only about the code running your service, and not the underlying platform or infrastructure, using Azure Functions is ideal. Functions are commonly used when you need to perform work in response to an event (often via a REST request), timer, or message from another Azure service, and when that work can be completed quickly, within seconds or less.


## Azure Logic Apps

Logic apps are similar to functions. Both enable you to trigger logic based on an event. Where functions execute code, logic apps execute workflows that are designed to automate business scenarios and are built from predefined logic blocks.

## Functions vs. Logic Apps


Functions and Logic Apps can both create complex orchestrations. An orchestration is a collection of functions or steps that are executed to accomplish a complex task.

With Functions, you write code to complete each step.
With Logic Apps, you use a GUI to define the actions and how they relate to one another






































