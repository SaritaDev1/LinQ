# Capa de acceso a datos

La capa de acceso a datos es la parte del sistema que se encarga de comunicarse con la base de datos.

Esta capa permite realizar operaciones como consultar, guardar, modificar o eliminar información. Por ejemplo, desde aquí se puede buscar un cliente, listar empleados, registrar un préstamo o actualizar los datos de una tabla.

Su función principal es evitar que la capa de presentación trabaje directamente con la base de datos. Esto hace que el sistema sea más ordenado y más fácil de mantener.

En esta capa se crean métodos que devuelven la información según lo que se necesite. No siempre se devuelve una lista, porque depende del resultado que se espera obtener.

Por ejemplo:

Si se necesitan varios registros, se puede devolver una lista.

Si se necesita un solo registro, se puede devolver una entidad.

Si se necesita contar registros, se puede devolver un número.

Si se necesita saber si algo existe, se puede devolver verdadero o falso.

Un ejemplo de método para listar clientes sería:

```csharp
public List<Cliente> ListarClientes()
{
    var consulta = from c in db.Clientes
                   select c;

    return consulta.ToList();
}
```

En este caso se usa List<Cliente> porque se espera obtener varios clientes de la base de datos.

La capa de acceso a datos funciona como un puente entre el sistema y la base de datos. Su trabajo es obtener o modificar la información y enviarla a la capa de negocio para que allí se apliquen las reglas necesarias.
