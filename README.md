# **Actividad Cuaderno UD1**
---
## UNIDAD 1
---
## Qué es un Lenguaje de marcas
#
#### Un lenguaje de marcas se refiere a la forma de escribir el codigo de un documento.Es una manera de definir la estructura del texto o su presentación incorporando etiquetas o marcas que contienen información adicional.
#
## Evolución de los Lenguaje de marcas
- GML: Los lenguages de marcas aparecieron por la necesidad empresarial de guardar una gran cantidad de temas de multitud de temas, y seria IBM, con esa necesidad de guardar datos que acabaria creando GML, un lenguaje que le permitia solucionar ese problema, dandoles la posivilidad de poder clasificar y escribir cualquier documento. Etonces esto seria vito por ISO, los cuales en ese momento se encargaban de normalizar procesos, que cogeria esta idea y acabaria creando SMGL, es decir, su version "standart"
- SGML: Es ub lenguaje de marcas bien trabajado, que al ser capaz de adaptarse a una gran cantidad de trabajos, a trabes de el se han realizado otros programas como STML, 
## Características de los lenguajes de marcas
  - Independencia: Los lenguajes de marcas no podra depender de que su lectura solo se pueda realizar con un software o hardware especifico
  - Almacenados en Texto Plano: Los lenguajes deveran estar formado por texto plano
  - Flexibilidad. El lenguaje de marcas debera tener la capacidad de adaptarse a diferentes usos
  - Compatibilidad: Las marcas y los contenidos del documento podran estar en el mismo archivo
  - Facilidad de procesamiento: El formato que coja el documento debera permitir una lectura sencilla y automatica
## Características y ejemplos de los siguientes lenguajes de marcas:
- XML
  - Los documentos XML tendran sienprer una etiqueta de apertura con la forma --> < y >
  - Las etiquetas que hayan sido habierta tendra que ser cerradas por su etiqueta que contendran el mismo texto pero se diferenciaran porque tendran que añadirle una /, con la forma --> </ y >.
  - Un archivo XML podra estyar formado por un texto o por otros elementos 
  - EN el archivo solo podra haber un elemento raiz
  - Un atributo los atributsos tendran la forma --> <nombre="valor">
  - Un elemnto podra no tener atrubutos o contar con varios de ellos
  - Ejemplo:
    ```
    <Persona>
      <nombre> Manolin </nombre>
      <apellidos>Manzano Olea</apellidos>
    </persona>
    ```
- HTML
  - Es facil de usar y entender
  - Es utilizado para crear paginas webs
  - Se puede ver lso archivos tanto en movil como en ordenador
  - Todos los elementos contaran con una etiqueta de inico, el texto y otra etiqueta de cierre
  - Sus archuvos se puede leer en cualquier buscador
  - Ejemplo:
    ```
    <DOCTYPE html>
    <html lang="es-ES">
      <head>
      <title>Ejemplo de html</title>
      </head>
      <body>
        <p>Este es el primer parafo</p>
        <p>Este es el segundo y ultimo parrafo</p>
      </body>
    ```
- JSON
  - Es un lenguaje modelador de datos
  - Se trata de un lenguaje codificado por "clave-valor"
  - Los valores pueden ser cadenas, numeros o conjuntos boleanos
  - Es un lenguage ligero y que no es complicarlo de trasnmitir
  - Ejemplo:
    ```
    {
    "tipo"="class",
    }
    ```
- YAML
  - Para describir los contenidos de YALM se usara o UTF-8 o UTF-16
  - La estructura se irá denotando con espacios en blanco
  - Tienen un lenguaje mu sencillo y de facil lectura
  - Tiene u lenguaje que se asemeja al XML
## Webgrafia
- https://desarrolloweb.com/articulos/450.php
- https://www.gmlplus.es/que-es-un-gml/
- https://www.nextu.com/blog/que-es-html-rc22/
- https://desarrolloweb.com/home/json
---
## UNIDAD 2
---
## Documentos XML, estructura:
- Declaración o prólogo
  - *version*, version de la espicificacion del documento xml, el cual por defecto vienen asignado como 1.0, aunque puedes utilizar el 1.1, el cuan viene con funcionalidades añadidas
  - *encouding*, codificacion en la que esta escrito el documento, como UFT-8
  - *standalone*, indica si el documento contiene un DTD, si lo contiene aparecera (yes,), en caso de que no contenga umo aparecerá (no)
- Elementos: los documentos x,l. contienen elementos que pueden estar unos dentro de otros. Estos elementos presentean las sigiuentes caracteristicas
  - Un elemento tiene un nombre que se diferencian entre mayúsculas y minúsculas. Además, el nombre puede empezar por _ y por un carácter.
  - Comienza por <nombre> y acaba con </nombre>. Los cuales deben ser por pares.
  - Debe haber un único elemento inicial llamado raíz.
  - Dentro de un elemento, puede contener más elementos o un texto.
  - Cuando un elemento está vacío, se pone con la siguiente notación <nombre/>
  - Ejemplo:
```
<books>
   <book>
      <title>titulo</title>
      <author>autor</author>
      <year>2023</year>
   </book>
</books>
```
  #### Ademas, todos los elementos xml tienen una serie de relaciones:
  - Un único elemento Raíz.
  - Cada uno de los elementos descendientes de otro elemento, se les llama hijos(children).
  - El elemento ascendente de otro elemento se le llama padre (parent).
  - Los elementos con un padre común se les llama hermanos (sibling).
- Atributos: Los atributos, se necuentran dentro de la etiqueta de apertura de los elementos y nos aportan informacion adicional de este. Los atributos poseen las siguientes caracteristicas.
  - Pueden comenzar por guion bajo _ o por un carácter, además su nombre no puede contener espacios.
  - Deben tener un valor, que puede ir entre comillas ya sean dobles o simples; pero se recomienda el uso de dobles.
  - Pueden ser opcionales su aparición y siempre deben de estar dentro de un elemento.
  - Siempre deben aparecer en la etiqueta de apertura de un elemento; nunca en la de cierre.
  - Ejemplo:
```
<books>
   <book isbn="123123123"><!--ISBN es un atributo -->
   </book>
</books>
```
- Comentarios: Un comentario, es una linea de codigo,que no sera leida por el documento, y que nos permite escribir explicaciones u informacion adiuicional. Tiene el siguiente formato
  ```
   <!-- Esto es un comentario -->
  ```
- Espacios de Nombres: Un espacio de nombres o namespace, permite distinguir etiquetas que pueden ser ambiguas. Para ello, se puede usar un atributo especial llamado xmlns seguido de dos puntos y el nombre del prefijo a utilizar. Después en el valor del atributo, se establece la URI donde esta definido el DTD de dicho espacio de nombres.
```
<b:books xmlns:b="http://example.com/books">
```
En este ejemplo, vemos como se esta cargando el espacio de nombres para las etiquetas relacionados con los libros y que tendrá el prefijo b.
- Entidades:Las entidades, son fragmentos de información predefinidos que nos van a permitir incluir dicha información sin necesidad de repetir dicha información o utilizar caracteres especiales. Estas entidades presentan las siguientes caracteristicas:
  - Para utilizar una entidad se comienza con el carácter & y se termina con ;.
  - Pueden estar definidas en el DTD o que sean externas.
  - Se pueden clasificar en:
    - Generales: Forma parte del documento
      - Internas: Están definidas en el propio documentos
      - Externas: Están definidas en un documento externo.
    - Entidades por parámetros: permite transformarlas en un DTD.
  - Además, XML incluye unas entidades internas predefinidas:
  ```
    - &lt;      	Menor que	        <
    - &gt;	     Mayor que	        >
    - &amp;      	Ampersand	        &
    - &apos;	   Comilla simple   	'
    - &quot;    	Comilla doble	        "
  ```
- CDATA: El elemento CDATA, es un fragmento de información que no será procesador por el analizador; sin embargo, si que se almacenará su información, a diferencia de los comentarios.
```
<book>
    <description>
           <![CDATA[  <html>
                                <head>
                                </head>
                                <body>
                                     <h1> Encabezado</h1>
                               </body>
                           </html>
           ]]>
    </description>
</book>
```
#### En el codigo anterior, se puede ver un ejemplo, donde se aprecia como sera la estructura de un CDATA, comenzando por un " <![CDATA ", dentro los los dos corchetes, estara el mensage que queremos poner " [aqui se mete el mensaje] ", y el CDATA se cerara de la siguiente manera" ]> "
---
## Validación de documentos:
---
## DTD
#### El DTD (Document Type Definition), son unas series de reglas que nos van a poder permitir comprovar si la estructura de el documento es válido. Ejemplo
```
<book isbn="123131">
  <title>titulo</title>
  <author>autor</author>
  <year>2023</year>
</book>
```
Está seria la estructura del xml que vamos a comprovar.
```
<!DOCTYPE book[
     <!ATTLIST book isbn CDATA #REQUIRED>
     <!ELEMENT title (#CDATA)>
     <!ELEMENT author (#CDATA)>
     <!ELEMENT year (#CDATA)>
]>
```
Y esta seria el DTD que valida esa estructura.
### Entidades: 
#### El DTD, nos permite definir entidades que no esten definidas en el xml
  - Internas. Están dentro del propio DTD. Estas se definen de la siguiente forma:
```
<!ENTITY nombreEntidad "Valor">
```
  - Externas. Se definen en un fichero externo. Pudiendo ser
    - Pública:
``` <!ENTITY nombreEntidad PUBLIC "id_publico" "URI"> ```
    - Privada:
``` <!ENTITY nombreEntidad SYSTEM "URI"> ```
### Anotaciones: 
#### Una alotacion, es un componente que define un formato de un valor, concretamente que no se utilizaran como una entidad XML, como puede ser el caso del valor de un atributo. Se pueden definir como:
- Anotación pública
```
<!NOTATION nombre PUBLIC “id_publico”>
<!NOTATION nombre PUBLIC “Id_publico” “URI”>
```
- Anotación privada
```
<!NOTATION nombre SYSTEM “URI”>
```
### Elementos 
#### Paara definir elementos utilizamos la siguiente estructura
```
<!ELEMENT nombreElemento (contenido)>
```
Donde el "contenido" puede ser:
- EMPTY: Vacío.
- ANY: Cualquier valor.
- (#PCDATA): Elemento de tipo carácter.
- (NombreElemento): Elemento Hijo.
- (NombreElemento1,NombreElemento2,...): Lista de elementos hijos.
### Atributos
#### Para definir atributos utilizamos la siguiente estructura:
```
<!ATTLIST nombreElemento nombreAtributo tipoAtributo "valorAtributo">
```
Donde el "tipoAtributo" puede ser:
- CDATA: Cadena de caracteres.
- (Valor1|Valor2): Lista de valores.
- ID: Identificador único.
- IDREF: Referencia a un identificador de otro elemento.
- IDREFS: Lista de identificadores de otro elemento.
- NMTOKEN: Nombre XML válido.
- NMTOKENS: Lista de Nombres XML válidos.
- ENTITY: Referencia a una entidad.
- ENTITIES: Referencia a un conjunto de entidades.
- NOTATION: Nombre de una anotación.
- xml:lang: Idioma del documento.
- xml:space: Indica si se han de respetar espacios tabulaciones y retornos de carro múltiples.
#### Ademas, "el valorAtributo" puede ser:
- valor: valor o lista de valores(separados por |) que puede tomar el atributo.
- #REQUIRED: atributo obligatorio.
- #IMPLIED: Indica que el valor es opcional.
- #FIXED valor: indica un valor fijo
## XMLSchema
#### XMLSchema, es un DTD, que soluciona algunos prolemas de este. Algunas funcionalidades son:
- Permite determinar qué elementos y atributos admite un XML.
- Permite determinar los tipos de datos que contienen tanto elementos como atributos(Cadena, números, fecha...).
- Permite asignar valores por defecto.
- Permite determinar cardinalidades más precisas, orden de los elementos u opcionalidad.
- XMLSchema esta escrito en XML a diferencia de DTD.
#### Para enlazar un fichero XSD, tenemos en primer lugar que añadir el espacio de nombres para usar XMLSChema y establecer un esquema por defecto. Si hubiese más, se pueden establecer utilizando otros espacios de nombres.
```<mensaje xmlns:xs="http://w3.org/2001/XMLSchema-instance"
                xs:noNamespaceSchemaLocation="mensaje.xsd">
```
Como vemos en el fragmento anterior, el fichero xsd, puede estar en un fichero Local, o usando una URL externa.
Una vez enlazado el fichero XSD, podemos definirlo usando como raiz el siguiente elemento:
```
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
```
Dentro del elemento xs:schema añadiremos toda la definición del esquema.
--- 
### XSD
---
### Dentro de un XSD, puede haber los siguientes elementos:
#### Elementos: Los elementos pueden ser:
- Locales: Hijos de los elementos que no son el elemento raíz y  sólo se usan una vez.
- Globales: Hijos del elemento raíz y pueden ser reutilizados.
#### Donde la estructura es la siguiente:
```
<xs:element name="" type="" default="" fixed="" minOccurs="0" maxOccurs="0" />
```
#### Cada parte nos da la siguiente informacion:
- name: Nombre del elemento.
- type: Tipo de dato que contiene.
- default: Valor por defecto.
- Fixed: Valor del atributo en caso de que exista.
- minOccurs: número de veces mínimo que puede aparecer. Por defecto 1.
- maxOccurs: número de veces máximo que puede aparecer. Por defecto 1.
#### Atributos: Un atributo, puede estar dentro de un elemento simple o complejo; tiene la siguiente sintaxis:
```
<xs:attribute name="" type="" use="required" default="" fixed=""/>
```
- El atributo tiene las siguientes propiedades:
  - name: Nombre del atributo.
  - type: Tipo de dato.
  - use: Indica su obligatoriedad. Tiene los siguientes valores:
  - required: obligatorio.
  - optional: Opcional.
  - prohibited: No se puede utilizar el dicho elemento.
  - default: Permite asignar un valor por defecto.
  - fixed: Determina el valor del atributo en caso de que exista.
#### Restricciones: Para establecer una restricción, su sintaxis es:
```
<xs:restriction base="xs:integer">
</xs:restriction>
```
- Donde base, es el tipo de dato del que se inicia. Dentro de la restricción, se establecen facetas que establecen los tipos de valores a utilizar. Existen los siguientes:
  - xs:length Longitud Fija
  - xs:minLength	Longitud Mínima
  - xs:maxLength	Longitud Máxima
  - xs:totalDigits	Total Dígitos de un número
  - xs:fractionDigits	Total digitos Decimales de un número
  - xs:minExclusive	Valor mínimo que puede tomar.
  - xs:maxEclusive	Valor máximo que puede tomar.
  - xs:minInclusive	Valor que debe ser mayor o igual
  - xs:maxInclusive	Valor que debe ser menor o igual
  - xs:enumeration	Lista de posibles valores (String)
  - xs:whiteSpace	Determina como tratar los espacios en blanco.
  - xs:pattern	Fija un patrón de caracteres permitidos.
#### Tipos de datos: Disponenemos de los siguientes tipos de datos:
  - xs:string	Cadena de caracteres
  - xs:integer	Número Entero
  - xs:decimal	Número decimal separando por ".".
  - xs:boolean	Valor Booleano "true" para verdadero o "false" para falso.
  - xs:date	fecha con formato AAAA-MM-DD
  - xs:time	Hora con formato hh:mm:ss
  - xs:durantion	Duración de tiempo con formato "PnYMnDTnHnMns".
#### Comentarios:Estos comentarios se utilizan como documentación del propio esquema y ayuda a quienes lo utilizan a comprenderlo. Estos comentarios NO son lo mismo que los comentarios XML que se pueden seguir utilizando de igual forma que para los propios documentos XML. Tienen la siguiente estructura:
```
<xs:element name="mensaje">
        <xs:annotation>
            <xs:appinfo>Información del mensaje</xs:appinfo>
            <xs:documentation>Mensaje a enviar</xs:documentation>
        </xs:annotation>
</xs:element>
```
Donde podemos ver:

- appInfo: Información del elemento o atributo.
- documentation: Documentación en detalle del elemento o atributo.

### Ejemplo de SCHEMA
```
<?xml version="1.0" encoding="UTF-8"?>
<books
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xsi:noNamespaceSchemaLocation="books.xsd">
    <book ref="111111A">
        <title>Desarrollo Homebrew para 16 bits</title>
        <author>V. Suarez Garcia</author>
        <year>2023</year>
    </book>
</books>
```
Este es el documento que vamos a validar con SCHEMA
```
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
    <xs:element name="books">
        <xs:complexType>
            <xs:all>
                <xs:element name="book">
                    <xs:complexType>
                        <xs:sequence>
                            <xs:element name="title" type="xs:string"/>
                            <xs:element name="author" type="xs:string"/>
                            <xs:element name="year">
                                <xs:simpleType>
                                    <xs:restriction base="xs:integer">
                                        <xs:minInclusive value="1970"/>
                                    </xs:restriction>
                                </xs:simpleType>
                            </xs:element>
                        </xs:sequence>
                        <xs:attribute name="ref">
                            <xs:simpleType>
                                <xs:restriction base="xs:string">
                                    <xs:pattern value="[0-9]{6}[A-Z]"></xs:pattern>
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:attribute>
                    </xs:complexType>
                </xs:element>
            </xs:all>
        </xs:complexType>
    </xs:element>
</xs:schema>
```
Y esta es su validacion usando la estructura de SCHEMA
