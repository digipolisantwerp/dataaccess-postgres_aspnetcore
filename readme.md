# DataAccess.Postgres Toolbox

> Postgres data access for ASP.NET Core 1.0

## PostgresDbConfiguration

This class is used to configure Entity Framework to work with the Npgsql provider for PostgreSQL. It can be used in conjuction with the DataAccess Toolbox.

``` csharp
public class PostgresDbConfiguration : DbConfiguration
{
    public PostgresDbConfiguration()
    {
        SetDefaultConnectionFactory(new Npgsql.NpgsqlConnectionFactory());
        SetProviderFactory("Npgsql", Npgsql.NpgsqlFactory.Instance);
        SetProviderServices("Npgsql", Npgsql.NpgsqlServices.Instance);
    }
}
```  