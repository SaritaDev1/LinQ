# UNIVERSIDAD TÉCNICA DE AMBATO

Nombre: Sarahi Toalombo

Asignatura: Programación Avanzada

Docente: Ing. Hernán Naranjo

# Índice

- [Introducción](#introducción)
- [Objetivo](#objetivo)
- [¿Qué es LINQ?](#qué-es-linq)
- [Arquitectura de 4 capas](#arquitectura-de-4-capas)
- [Capa de presentación](./1.Capa%20de%20presentación.html)
- [Capa de negocio](./2.Capa%20de%20negocio.html)
- [Capa de acceso a datos](./3.Capa%20de%20acceso%20a%20datos.html)
- [Capa de entidades](./4.Capa%20de%20entidades.html)
- [Relación entre SQL y LINQ](./5.Relación%20entre%20SQL%20y%20LINQ.html)

# Introducción

Este documento tiene como finalidad explicar de una manera sencilla qué es LINQ y cómo se puede utilizar en un sistema que trabaja con base de datos. La idea no es memorizar código, sino entender para qué sirve y en qué parte del sistema se puede usar.

Muchas veces, cuando se trabaja con una base de datos, se usan consultas SQL para buscar, filtrar o mostrar información. LINQ permite hacer algo parecido, pero dentro del lenguaje C#. Por eso es útil cuando se desarrolla un sistema por capas, ya que ayuda a manejar los datos de una forma más ordenada.

LINQ puede participar principalmente cuando el sistema necesita consultar, filtrar, ordenar o buscar información. Por eso es importante entender cómo se relaciona con la base de datos y cómo puede usarse dentro de la capa de acceso a datos y también dentro de la capa de negocio.

# Objetivo

Explicar de forma clara y sencilla el uso de LINQ a nivel de base de datos, tomando en cuenta su aplicación en la capa de acceso a datos y en la capa de negocio dentro de una arquitectura de 4 capas.

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
Presentación → Negocio → Acceso a Datos → Base de Datos
      ↑            ↑             ↑
  Entidades    Entidades     Entidades
```

La capa de entidades funciona como apoyo para representar y mover los datos entre las capas de forma ordenada.

En esta arquitectura, LINQ participa principalmente en la capa de acceso a datos, porque ahí se realizan las consultas a la base de datos, como buscar clientes, listar productos o filtrar pedidos de `Northwind`.

También puede participar en la capa de negocio, pero de una forma diferente. En esa capa, LINQ no consulta directamente la base de datos, sino que puede filtrar, ordenar o revisar información que ya fue obtenida desde la capa de acceso a datos.

La capa de entidades también se relaciona con LINQ, porque LINQ trabaja con clases y objetos, como `Customer`, `Product` u `Order`, para consultar y manejar la información de forma ordenada.

# Ejemplo de relación de tablas en Northwind

Para este manual se toma como ejemplo la base de datos `Northwind`, porque contiene varias tablas relacionadas entre sí. Esto permite entender mejor cómo LINQ puede consultar información desde una base de datos real.

En `Northwind` existen tablas como `Customers`, `Orders`, `Order Details`, `Products`, `Categories`, `Suppliers`, `Employees` y `Shippers`.

Estas tablas se relacionan de la siguiente manera:

```text
Customers → Orders
Orders → Order Details
Order Details → Products
Products → Categories
Products → Suppliers
Employees → Orders
Shippers → Orders
```
<img width="1226" height="799" alt="Diagrama de relaciones de Northwind" src="https://github.com/user-attachments/assets/764c65f6-fed3-4ff2-aa78-70e7ced9bba4" />

