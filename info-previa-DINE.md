
## Repositorio Datos Funcionalidad Primarias 2017

Repositorio de ficheros para los Medios de Comunicación.  

El objeto de este servicio es proporcionar a los medios de comunicación información sobre los resultados provisionales del proceso del 13 de agosto, con el fin de facilitarles su función informativa. Los medios podrán adecuar la información proporcionada por la aplicación a las características específicas en función de sus necesidades.  

El servicio consiste en la creación de un repositorio de datos al que podrán acceder para obtener la información deseada. Periódicamente se procederá a actualizar los ficheros del repositorio de forma que la información mostrada por medio de Internet sea coherente con la almacenada en este repositorio.  

Con objeto de asegurar el nivel de servicio con las máximas garantías de seguridad, se habilitarán unos usuarios y claves predefinidos que permitirán el acceso al sistema para la descarga de la información.  

La DINE comunicará a los medios la posibilidad de acceder a este tipo de servicio.  
Indra remitirá a la DINE el usuario y la password con la que los medios autorizados deben acceder al sistema, así como el nombre de la URL del sitio de descarga.  
Para garantizar que cualquier medio de información, con independencia de la infraestructura informática de la que disponga, pueda tratar los ficheros descargados, los datos se facilitan en
ficheros ASCII con separadores de campo.  
A continuación se detalla el contenido de la información disponible de que dispondrán los usuarios de este servicio, teniendo en cuenta que la descripción de estos ficheros es provisional
y podría tener alguna modificación posterior:  

### Descripción de archivos
Los archivos descargables con la información actualizada del escrutinio serán cuatro:
 - “totales.csv”
 - “totaleslista.csv”
 - “listas.csv”
 - “ámbitos.csv”

Irán comprimidos en un solo fichero: _datos<XXXXXX>.gz_, siendo _XXXXX_ una *cadena aleatoria*. Los archivos están comprimidos con "gzip", siendo compatibles con la mayoría de los descompresores como WinZip, WinRar etc.  
Todos los archivos descargables desde el servicio del repositorio presentan las siguientes características:  
 - Registros de longitud fija con final de registro tipo DOS (CR LF).
 - Campos delimitados por separadores ";"(punto y coma).
En los campos de tipo "Porcentaje", las dos últimas posiciones por la derecha se consideran decimales. Las longitudes que se detallan a continuación en los diseños de los archivos NO incluyen el separador de campos.  

### Identificación de los registros:
Identificación de tipos de elección:
 - Senadores Nacionales = 2
 - Diputados Nacionales = 3
 - Senadores Provinciales = 5
 - Diputados Provinciales = 6
Sección / comuna: Código de Provincia<>"999"

### Archivos del recuento provisional
Archivos de totales de recuento provisional
Contiene la información general del recuento provisional totalizada a nivel de sección o comuna.  
Archivo totales.csv (totales de recuento provisional)


|DESCRIPCIÓN | LONGITUD|
|------------|---------|
|Código de elección | 1|
|Código de provincia | 2|
|Código de comuna | 3|
|Total de mesas | 5|
|Mesas escrutadas | 5|
|Porcentaje de mesas escrutadas | 5|
|Electores | 8|
|Total de votantes | 8|
|Participación sobre padrón | 5|
|Participación sobre escrutado | 5|
|Electores escrutados | 8|
|Porcentaje de electores escrutados | 5|
|Votos válidos | 8|
|Porcentaje de votos válidos | 5|
|Votos positivos | 8|
|Porcentaje de votos positivos | 5|
|Votos en blanco | 8|
|Porcentaje de votos en blanco | 5|
|Votos nulos | 8|
|Porcentaje de votos nulos | 5|
|Votos recurridos, impugnados y comando | 8|
|Porcentaje de votos recurridos e impugnados | 5|
|Día | 2|
|Hora | 2|
|Minuto | 2|

### Archivo de recuento provicional por listas
Contiene la información del recuento provisional de las agrupaciones políticas y las listas, totalizada a los niveles de provincia y sección/comuna.  

Archivo totaleslistas.csv (totales por listas)

|DESCRIPCIÓN | LONGITUD|
|------------|---------|
|Código de elección | 1|
|Código de provincia | 2|
|Código de sección/ comuna | 3|
|Día | 2|
|Hora | 2|
|Minuto | 2|
|Código de la agrupación política | 4|
|Votos a la agrupación política | 8|
|Porcentaje de votos a la agrupación política | 5|
|Tabla de 10 elementos, correspondientes a las listas propuestas por cada partido| |
|Código de lista | 4|
|Votos al lista | 8|
|Porcentaje de votos a la lista | 5|

### Archivo auxiliar de agrupaciones políticas / listas.

Contiene la relación de las agrupaciones políticas y sus listas que intervienen en el proceso.  
Archivo listas.csv

|DESCRIPCIÓN | LONGITUD|
|------------|---------|
|Código de agrupación política / lista | 4 |
|Siglas de la agrupación política / lista | 50 |
|Denominación de la agrupación política / lista | 100 |

### Archivo auxiliar de ámbitos.
Contiene la relación de los ámbitos territoriales: provincias y secciones / comunas.  
Archivo ambitos.csv

|DESCRIPCIÓN | LONGITUD|
|------------|---------|
|Código de provincia |2 |
|Código de sección/comuna | 3|
|Nombre del ámbito |40|

Con el fin de que los usuarios de este sistema puedan realizar pruebas previas, la DINE remitirá por correo electrónico a los medios que lo hayan solicitado la URL para acceder a unos ficheros de pruebas que les permitan hacer y probar sus desarrollos.  
Finalmente, días previos a la jornada electoral la DINE remitirá la URL y claves para uso del repositorio durante el recuento el día 13 de agosto.  

### Preguntas frecuentes

#### Los datos que hay en el repositorio (ámbitos, candidaturas, etc), ¿son definitivos?

Dado que las pruebas del repositorio comenzarán antes de disponer de las candidaturas
definitivas, es bastante probable que dicho repositorio no contenga todas, incluso si fuese
necesario se utilizarían candidaturas ficticias para disponer de suficientes datos de prueba.
Según se vayan recibiendo las candidaturas definitivas de las provincias se irán incorporando a
los ficheros de datos.

#### ¿Cómo puedo acceder a los datos del repositorio?
 - El acceso al repositorio estará protegido por usuario / password.  
 - El repositorio tendrá una página html llamada “descargas.htm” que indicará la fecha y hora de los datos, e incluirá un enlace html al fichero tar.gz que contendrá los datos actualizados. Este enlace siempre apuntará al fichero de datos más actual.  
- Los datos se actualizarán cada cinco minutos, si hay datos nuevos.
#### ¿Si quiero utilizar al mismo tiempo dos o más ingresos, ¿necesito solicitar más de una clave?
No, podrá utilizar la misma clave para varios ingresos.  

#### ¿Qué usuario y password tengo que utilizar?
Esta información será distribuida por la DINE.

#### Tengo el usuario y la password que me ha enviado la DINE, pero después de teclearlos obtengo un mensaje que dice “Acceso denegado”.  
De alguna manera el usuario o la password han podido ser incorrectamente introducidos. Para volver a intentarlo no basta con teclear de nuevo la dirección web. Hay que cerrar totalmente el navegador y abrirlo de nuevo, pues la sesión mantiene en memoria estos datos y no vuelve a preguntarlos.

#### ¿Cuándo podremos probar el sistema?
De momento no hay una fecha definida para las pruebas. Esta fecha será comunicada previamente por la DINE.
