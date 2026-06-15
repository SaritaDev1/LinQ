# Capa de entidades

La capa de entidades es la parte del sistema donde se crean las clases que representan la información de la base de datos.

Para entenderlo de forma sencilla, una entidad es como una copia en C# de una tabla de la base de datos. Es decir, si en la base de datos existe una tabla llamada Clientes, en la capa de entidades se puede crear una clase llamada Cliente.

Cada columna de la tabla se convierte en una propiedad dentro de la clase.

Por ejemplo, si la tabla Clientes tiene los campos IdCliente, Nombre, Apellido y Estado, la clase puede quedar así:

public class Cliente
```csharp
{
    public int IdCliente { get; set; }
    public string Nombre { get; set; }
    public string Apellido { get; set; }
    public string Estado { get; set; }
}
```

Esta capa es importante porque permite transportar la información entre las demás capas del sistema. Por ejemplo, la capa de acceso a datos puede obtener un cliente desde la base de datos y enviarlo a la capa de negocio usando la clase Cliente.

La capa de entidades sirve para representar las tablas de la base de datos mediante clases de C#. Esto ayuda a que el sistema trabaje con objetos y no con datos sueltos.
