[DevOps Getting Started](https://www.youtube.com/watch?v=j7OnxOz7YDY)

[ADO version](https://www.youtube.com/watch?v=G7H6HbzwAfs)

[Blog post](https://devblogs.microsoft.com/azure-sql/devops-for-azure-sql/)

# Project Set Up
1. SQL server and SQL DB 
    * Make Sure the SQL DB has firewall rules that allows for query access
2. Create a devops org and project
3. connect the devops org to the directory
4. create the dbt repo add in the azure pipeline yaml
5. use azure cli to handle user auth for testing
6. In the Azure DevOps Project add a Service Connection
    * Project Settings --> Service Connection
    * Hit New Service Connection Button
    * Azure Resource Manager --> Workload Identity federation (auto/recommended)
        * This will create an App Registration in the Azure Portal
        * Rename it if you wish
        * give it permissions for the sql server


### Hotfix Directory
Add macro in `macros/dbt_utils/sql/generate_surrogate_key.sql`

See [Issue 97](https://github.com/dbt-msft/tsql-utils/issues/97) and related [PR](https://github.com/dbt-msft/tsql-utils/pull/98)


