# UNIVERSIDAD TÉCNICA DE AMBATO

Nombre: Sarahi Toalombo

Asignatura: Programación Avanzada

Docente: Ing. Hernan Naranjo

# Introducción

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

# Arquitectura de 4 capas

La arquitectura de 4 capas es una forma de organizar un sistema para que el código esté separado según la función que cumple cada parte.

Las 4 capas principales son:

* Capa de presentación
* Capa de negocio
* Capa de acceso a datos
* Capa de entidades

La información normalmente funciona de esta manera:

```text
Presentación → Negocio → Acceso a Datos → Base de Datos
```

La capa de entidades se relaciona con las demás capas porque sus clases se usan para transportar la información.

Por ejemplo, en `Northwind`, la capa de acceso a datos consulta la tabla `Customers` y convierte esa información en un objeto `Customer`.

Luego, la capa de negocio recibe ese objeto `Customer` para revisarlo o aplicar reglas.

Finalmente, la capa de presentación recibe el objeto `Customer` y muestra sus datos al usuario.

```text
Base de Datos → Acceso a Datos → Negocio → Presentación
                         ↑          ↑             ↑
                      Entidades  Entidades    Entidades
```

La capa de entidades funciona como apoyo para mover los datos entre las capas de forma ordenada.

En esta arquitectura, LINQ participa principalmente en la capa de acceso a datos, porque ahí se realizan las consultas a la base de datos, como buscar clientes, listar productos o filtrar pedidos de `Northwind`.

También puede participar en la capa de negocio, pero de una forma diferente. En esa capa, LINQ no consulta directamente la base de datos, sino que puede filtrar, ordenar o revisar información que ya fue obtenida desde la capa de acceso a datos.

La capa de entidades también se relaciona con LINQ, porque las consultas trabajan con clases y objetos, como `Customer`, `Product` u `Order`.
