# UNIVERSIDAD TÉCNICA DE AMBATO

Nombre: Sarahi Toalombo

Asignatura: Programación Avanzada

Docente: Ing. Hernan Naranjo

# Introduccion

Este documento tiene como finalidad explicar de una manera sencilla qué es LINQ y cómo se puede utilizar en un sistema que trabaja con base de datos. La idea no es memorizar código, sino entender para qué sirve y en qué parte del sistema se puede usar.

Muchas veces, cuando se trabaja con una base de datos, se usan consultas SQL para buscar, filtrar o mostrar información. LINQ permite hacer algo parecido, pero dentro del lenguaje C#. Por eso es útil cuando se desarrolla un sistema por capas, ya que ayuda a manejar los datos de una forma más ordenada.

LINQ puede participar principalmente cuando el sistema necesita consultar, filtrar, ordenar o buscar información. Por eso es importante entender cómo se relaciona con la base de datos y cómo puede usarse dentro de la capa de acceso a datos y también dentro de la capa de negocio.

# Objetivo

Explicar de forma clara y sencilla el uso de LINQ a nivel de base de datos, tomando en cuenta su aplicación en la capa de acceso a datos y en la capa de negocio dentro de una arquitectura en 3 capas.

# ¿Qué es LINQ?

LINQ significa Language Integrated Query, que en español se puede entender como consulta integrada en el lenguaje.

LINQ es una herramienta de C# que permite realizar consultas sobre diferentes tipos de datos desde el mismo código del programa. Estos datos pueden estar en listas, arreglos, colecciones de objetos o también venir desde una base de datos.

Una forma sencilla de entender LINQ es pensar que permite hacer preguntas a los datos. Por ejemplo, se puede preguntar qué clientes están activos, qué empleados pertenecen a un área o cuántos registros existen.

LINQ ayuda a trabajar con información de una forma más clara dentro de C#, usando clases, objetos y propiedades del sistema.

# ¿Para qué sirve LINQ en base de datos?

En base de datos, LINQ sirve para obtener y manejar información desde el código de C#, sin escribir directamente una consulta SQL en cada parte del sistema.

Por ejemplo, si existe una tabla de clientes, LINQ puede ayudar a mostrar todos los clientes, buscar uno específico, filtrar solo los clientes activos o contar cuántos clientes existen.

También se puede utilizar cuando hay tablas relacionadas. Por ejemplo, una tabla de clientes puede estar relacionada con una tabla de préstamos. En ese caso, LINQ permite consultar qué préstamos pertenecen a cada cliente.

Dentro de una arquitectura de 3 capas, LINQ se usa principalmente en la capa de acceso a datos, porque esa capa es la encargada de comunicarse con la base de datos. Después, la información obtenida puede pasar a la capa de negocio, donde se aplican reglas o validaciones antes de mostrarla al usuario.

LINQ en base de datos sirve para traer, filtrar, ordenar, agrupar y procesar información desde C# de una forma más organizada.

# Arquitectura en 3 capas

La arquitectura en 3 capas es una forma de organizar un sistema para que el código esté separado según su función.

En un sistema, no es recomendable colocar todo el código en un solo lugar, porque después se vuelve difícil de entender, corregir o modificar. Por eso se divide en capas.

Las capas principales son:

Capa de presentación

Capa de negocio

Capa de acceso a datos

Además, en muchos proyectos también se utiliza una capa de entidades, que ayuda a representar los datos de la base de datos mediante clases.

La información normalmente trabaja de esta manera:

Presentación → Negocio → Acceso a Datos → Base de Datos
