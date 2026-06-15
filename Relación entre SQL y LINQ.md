# 4. Relación entre SQL y LINQ

SQL y LINQ sirven para consultar información, pero se escriben de diferente manera.

SQL trabaja directamente con tablas y columnas de la base de datos.

LINQ trabaja dentro de C#, usando clases, objetos y propiedades.

Ejemplo en SQL:

```sql
SELECT *
FROM Customers
WHERE Country = 'Germany';
```

Ejemplo en LINQ:

```csharp
var consulta = from c in db.Customers
               where c.Country == "Germany"
               select c;
```

Las dos consultas buscan clientes de `Germany`.

En una arquitectura de 3 capas, LINQ participa principalmente en la capa de acceso a datos, porque ahí consulta la base de datos.

También puede participar en la capa de negocio, cuando se necesita filtrar, ordenar o agrupar datos que ya fueron obtenidos.

En resumen, LINQ permite hacer consultas parecidas a SQL, pero dentro del código de C#.
