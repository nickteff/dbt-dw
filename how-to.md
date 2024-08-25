# DevOps for Azure SQL and dbt Project Setup

## Resources
- [DevOps Getting Started (Video)](https://www.youtube.com/watch?v=j7OnxOz7YDY)
- [Azure DevOps Version (Video)](https://www.youtube.com/watch?v=G7H6HbzwAfs)
- [Microsoft Blog Post](https://devblogs.microsoft.com/azure-sql/devops-for-azure-sql/)

## Project Setup Steps

1. **Azure SQL Setup**
   - Create SQL Server and SQL Database
   - Configure firewall rules to allow query access

2. **Azure DevOps Configuration**
   - Create a DevOps organization and project
   - Connect the organization to your Azure Active Directory

3. **dbt Repository Preparation**
   - Create a dbt repository in Azure DevOps
   - Add Azure Pipelines YAML file to the repository

4. **Authentication Setup**
   - Use Azure CLI for user authentication during testing

5. **Service Connection Configuration**
   - In Azure DevOps Project: Project Settings > Service Connections
   - Create a new "Azure Resource Manager" connection with Workload Identity Federation
   - This process:
     - Creates an App Registration in Azure Portal
     - Allows renaming of the App Registration (optional)
     - Requires granting necessary permissions for SQL Server to the App Registration

## Additional Configuration

### Hotfix for Surrogate Key Generation
- Add macro in `tsql_utils/macros/dbt_utils/sql/generate_surrogate_key.sql`
- Reference: [Issue 97](https://github.com/dbt-msft/tsql-utils/issues/97) and [PR 98](https://github.com/dbt-msft/tsql-utils/pull/98)

## Static Documentation Generation

### Creating a Static `index.html` for dbt Docs
1. Add the `docs_to_spa.py` script to your project
2. Run the script to generate a static `index.html`
   - This combines content from two JSON files into a single HTML file
   - Allows hosting as a static website (e.g., on GitHub Pages)

### Resources for Static Documentation
- [Deploying dbt Docs to GitHub Pages](https://medium.com/@connormcshane/how-to-deploy-dbt-docs-to-github-pages-using-github-actions-4f1774680155)
- [Generate dbt Doc in One Static HTML File](https://data-banana.github.io/dbt-generate-doc-in-one-static-html-file.html)