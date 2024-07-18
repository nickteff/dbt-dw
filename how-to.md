[DevOps Getting Started](https://www.youtube.com/watch?v=j7OnxOz7YDY)

[ADO version](https://www.youtube.com/watch?v=G7H6HbzwAfs)

[Blog post](https://devblogs.microsoft.com/azure-sql/devops-for-azure-sql/)

SQL server and SQL DB that can be queried 
Create a devops org and project
connect the devops org to the directory
create the dbt repo add in the azure pipeline yaml
use azure cli to handle user auth for testing
add managed identity to the devops org and sql server

### Hotfix Directory
Add macro in `macros/dbt_utils/sql/generate_surrogate_key.sql`

See [Issue 97](https://github.com/dbt-msft/tsql-utils/issues/97) and related [PR](https://github.com/dbt-msft/tsql-utils/pull/98)

