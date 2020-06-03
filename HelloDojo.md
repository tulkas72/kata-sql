# EPFL Dojo - consultas SQL

El objetivo es tener un ejercicio para practicar consultas SQL en
tablas predefinidas.


## Concepto

Usted es responsable de la comunicación del club nocturno "HelloDojo"
que pronto abrirá sus puertas. Ha recuperado listas de personas en
formato SQL y para ejercer sus habilidades de marketing, necesita
extraer información relevante.

Para que otros hagan lo mismo, debe tener en cuenta todos los pasos en
el archivo HowTo.md . ¡En un mundo ideal, ha clonado el depósito y,
por lo tanto, también podrá ver los pasos dados por sus colegas y
beneficiarse de ellos!

La documentación oficial de MySQL se puede encontrar [aquí](https://dev.mysql.com/doc/refman/8.0/en/) y también se
puede utilizar la página [StackOverflow](https://stackoverflow.com/tags/mysql/info).


## Pasos


## Prepararación

En primer lugar, debes importar los datos en un sistema de
administración de bases de datos (DBMS) como mysql. También debes crea
un esquema.jpg (también vale un esquema creado con MySQL Workbench) de
la base de datos.


## Información a recolectar


### General

1.  Para comenzar, desea saber la cantidad de personas que tiene en
    su base de datos ( people).
2.  ¿Hay duplicados?
3.  ¿Cómo ordenarlos en orden alfabético ascendente por apellido?
4.  ¿Hay alguna forma de limitar el número de resultados, por
    ejemplo, mostrando solo los primeros 5, siempre ordenados por
    apellido?
5.  ¿Cómo encontrar personas que tengan un nombre o un apellido que
    contenga *ojo*?
6.  ¿Quiénes son las 5 personas más jóvenes? ¿Y los mayores? Cuidado
    con las personas que aún no han nacido ...
7.  ¿Cómo encontrar la edad, en años, de las personas?
8.  ¿Cómo podemos encontrar la edad promedio de las personas en la
    tabla?
9.  Su diseñador trabaja con las tarjetas de socio y necesita saber
    quién tiene el nombre y el nombre más largos.
10. Sin saber aún exactamente cómo se organizará el diseño de las
    tarjetas de socio, también le gustaría saber quiénes son las 3
    personas que tienen apellido + nombre más largo.


### Invitaciones

1.  Para la apertura, le gustaría incluir a todos los miembros:
    -   mayores de 18 años,
    -   y menores de 60 años,
    -   que tienen una dirección de correo electrónico válida
2.  Para que sea más fácil de leer, agrega una columna *age* (edad)
    en la consulta.
3.  Con estos miembros, le gustaría hacer una lista en el siguiente
    formato Nombre Apellido < email@provider.com >;para poder copiarla
    y pegarla en su cliente de correo electrónico.
4.  Con la información en la tabla people, ¿podríamos aproximar el
    número de personas que viven en Suiza?


### Países

1.  Para un futuro formulario de inscripción en un sitio web, desea
    avanzar tareas en su trabajo preparando los datos del país para
    las opciones de un *select*. Preparar la consulta que ofrece la
    lista de opciones en el formato:'\<option value="XXX"\>XXX\</option\>'.
2.  ¿Cuál sería una solución para tener esta lista disponible en
    francés e inglés cuando se traduzca el sitio?


### Joins

1.  Usando la tabla de unión en countries\_people.sql, enumere a las
    personas que viven en Suiza.
2.  Del mismo modo, enumere a las personas que no viven en Suiza.
3.  ¿Cómo enumerar a las personas que viven en los países
    fronterizos con Suiza? (es decir, Francia, Alemania, Italia,
    Austria, Lischenchtein)
4.  Desea saber cuántas personas hay por país, para saber cuanta
    gente de Suiza hay en la tabla *people* y cuántas personas son
    extranjeras.
5.  ¿Qué países no tienen gente (en la tabla)?
6.  ¿Hay personas vinculadas a más de un país?
7.  ¿Hay personas que no están vinculadas a ningún país?
8.  ¿Cómo podríamos mostrar los porcentajes de personas por país?


### Procedimientos

1.  La tabla en countries.sql contiene una columna **tld** (Top-level
    domain, Dominio de nivel superior). Encuentre una manera de
    mostrar el nombre del país en inglés según el **tld** de la
    dirección de correo electrónico de la persona.
2.  ¿Podríamos mostrar "País desconocido" si el correo electrónico
    está vacío o el tld no coincide con ningún país?
3.  ¿Cómo podríamos tener acceso a un mecanismo que encuentre
    automáticamente el **tld** de las direcciones de correo
    electrónico?


### Vistas

1.  Para facilitar consultas futuras, cree una vista HelloDojo que
    contenga las siguientes columnas:
    -   Toda la información de la tabla people;
    -   Una columna age;
    -   Una columna formateada con Nombre Apellido(mayúsculas ic);
    -   Una columna con el nombre del país en francés. (Si alguien
        quiere traducirlos...)


### Finanzas

1.  Para la apertura, el director ya ha comprado cajas
    registradoras. También sabes que se pueden comprar abonos y
    tarjetas de socio en el sitio web. Modifique la base de datos
    existente agregando una tabla *expenses* que permitirá ir
    añadiendo los gastos de cada miembro.
2.  Modifique la vista *HelloDojopara* agregar los gastos totales por
    miembro.
