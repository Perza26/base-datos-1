# TAREA-3

Pablo Peraza
2019249721

# Estándar MySQL


# Índice

-  [Entidades](#entidades)

-  [Atributos](#atributos)

-  [Tipos de datos](#tipos_de_datos)

-  [Llaves foráneas](#llaves_foraneas)

-  [Llaves primarias](#llaves_primarias)

-  [Índices](#indices)

# Introducción

A continuación se presentaran los objetos que se utilizan en las bases de datos, tales como entidades, atributos, índices, los cuales son en gran medida una parte muy importante en las bases de datos, por lo que es indispensable entender como están representados en las bases de datos. Ya que cuando se gestiona una base de datos muy desarrollada es necesario manejar un formato estándar para facilitar la comprensión de la misma y el trabajo de los desarrolladores a la hora de programar y realizar modificaciones, por esta razón si no se utilizara el formato estándar los nombres tenderían a confundir. Existen distintos estándares de programación, sin embargo para esta tarea se tomara como referencia el estándar de  programación orientado a MySQL 8.0 con  el set de caracteres `utf8mb4`  y la colación `utf8mb4_0900_ai_ci`.


<a name = "entidades" ></a>
## Entidades

Para nombrar las entidades  se deben tomar en cuenta algunas normal como que los nombres deben ser concisos y claros, además deben estar completos, no obstante, estos deben ser breves, por lo que hay que evitar utilizar mas caracteres de los necesarios, en el caso de que hubiera algún inicialismo, lo mejor sería utilizarlo, otra buena practica es evitar el uso de la comilla doble. Asimismo es necesario consolidar un estilo de escritura, para que se vea ordenado, por ejemplo el PascalCase o el  SNAKE_CASE, si bien ambos estilos son permitidos, lo ideal es solo utilizar uno a lo largo del proyecto, asimismo se aconseja utilizar mayusculas.

### Excepciones

En el caso de que existan acrónimos que sean reconocidos se permite utilizarlo para abreviar el nombre. Tanto en MySQL como en muchos otros lenguajes el se debe evitar  el uso de palabras reservadas.

### Ejemplos

- Utilizar `Estudiante` en vez de `estudiante`.

- Utilizar `Profesor` en vez de `”Profesor”`.

- Utilizar `"Curso_Estudiante"` en vez de ` Curso del estudiante ` en el estilo SNAKE_CASE. 

- Utilizar `"CursoEstudiante"` en vez de ` Curso del estudiante ` en el estilo PascalCase. 

- Utilizar `ICE` en vez de `Instituto_Costarricense_de_Electricidad`.


<a name = "atributos" ></a>
## Atributos

Las reglas definidas para las entidades también suelen ser empleados para los atributos, por lo que no es posible utilizar las comillas dobles y se recomienda escribir sin mayúsculas, con el fin de ser sumamente específicos se solicita que las palabras se escriban completas .

### Excepciones

Las excepciones son básicamente las mismas que con las entidades, no se permiten usar palabras reservadas, y en el caso de que exista un acrónimo reconocido, se puede utilizar para abreviar.

### Ejemplos

- Utilizar `escuela` en vez de `”escuela”`.

- Utilizar `telefono_casa` en vez de TelefonoDeLaCasa`.

- Utilizar `id_app` identificador `IdentificadorAplicacion`.


<a name = "tipos_de_datos" ></a>
## Tipos de datos

Al igual que las palabras reservadas en los lenguajes de programación, los tipos de datos no se deben utilizar en los nombres de las entidades y atributos, para no crear confusiones.

### Excepciones

Al ser los tipos de datos un estándar universal, estos no tienen excepciones.

### Ejemplos


- Utilizar `numero_telefono` en vez de `telefono_entero`.

- Utilizar `carnet` en vez de `carnet_entero`.

<a name = "llaves_primarias" ></a>
## Llaves primarias

  
es el identificador principal y único de una tabla, no se recomienda utilizar prefijos para hacer alusión a la tabla de esta manera evitar confusiones en las llaves  foráneas, ya que estás si necesitan que en sus nombres se utilice el nombre de la tablao algún prefijo

### Excepciones

No existen excepciones, ya que este estándar se aplica de forma universal.


### Ejemplos

- Utilizar "id  "en vez de "id_estudiante” en caso de que la tabla se llame Estudiante



<a name = "llaves_foraneas" ></a>
## Llaves foráneas

Se debe incluir en el nombre de la llave, el nombre o un prefijo de la tabla al que pertenece.

### Excepciones

Al igual que en las llaves primarias, al ser un estándar universal, no existen excepciones.

### Ejemplo

en caso de que la relación sea entre la tabla  Departamento con llave primaria id y la tabla Curso con llave primaria id

- Utilizar id­_departamento y id_curso 


<a name = "indices" ></a>
## Índices

En la base de datos los punteros de los registros se analizan los índices por lo que se recomienda que en los nombres de los índices se agregue el nombre la tabla con las respectivas columnas.

### Excepciones

Al igual que algunos los demás objetos al ser un estándar universal no posee excepciones 

### Ejemplo

CREATE TABLE Clientes(

id int PRIMARY KEY,

nombre text,

apellido text );

CREATE INDEXCliente_nombre ON Estudiante(nombre);
