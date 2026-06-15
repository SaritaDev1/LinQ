# ¿Para qué sirve LINQ en base de datos?

En base de datos, LINQ sirve para obtener y manejar información desde el código de C#, sin escribir directamente una consulta SQL en cada parte del sistema.

Por ejemplo, si existe una tabla de clientes, LINQ puede ayudar a mostrar todos los clientes, buscar uno específico, filtrar solo los clientes activos o contar cuántos clientes existen.

También se puede utilizar cuando hay tablas relacionadas. Por ejemplo, una tabla de clientes puede estar relacionada con una tabla de préstamos. En ese caso, LINQ permite consultar qué préstamos pertenecen a cada cliente.

Dentro de una arquitectura de 3 capas, LINQ se usa principalmente en la capa de acceso a datos, porque esa capa es la encargada de comunicarse con la base de datos. Después, la información obtenida puede pasar a la capa de negocio, donde se aplican reglas o validaciones antes de mostrarla al usuario.

LINQ en base de datos sirve para traer, filtrar, ordenar, agrupar y procesar información desde C# de una forma más organizada.
