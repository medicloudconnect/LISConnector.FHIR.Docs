# Connect a Database

You can use an existing `Azure SQL database` or create a new SQL database for the applications. An **install script** is provided to create the tables in the database. You will also need to configure the connection string in the Web App to connect to the database. You can refer to the relevant Microsoft Azure documentation to learn more about the Azure SQL databases.

### Create the database tables

Open your Azure SQL database, and click on the `Query editor`, enter your credentials to access your database.

![](../.gitbook/assets/query_editor.PNG)

You will get the sql scripts on Git Hub in the relevant API solution in a project called `LISConnectorMigrationsProduction` in the solution. All the API solutions will contain a project with the same name.

![](../.gitbook/assets/sqlscript_project-1.PNG)

Copy the script from the sql script file in the `InstallScript` folder as shown below.

![](../.gitbook/assets/sqlscript.PNG)

{% hint style="info" %}
Please copy the sql script from the most recent 'release' branch and not 'master' to get the most stable script for the database.
{% endhint %}

Paste the sql script in the `Query editor` and click the `Run` icon. The database tables will be created.

![](../.gitbook/assets/sqlscript_runquery.PNG)

You can view the tables in the `Tables` folder.

![](../.gitbook/assets/sqlscript_tables.PNG)

### Get the database connection string

Open the database in the portal and click on `Connection strings`, then copy the connection string. Edit the connection string to include your 'User Id' and 'Password' to connect to the database.

![](../.gitbook/assets/dbconnstr.PNG)

Open the Web App and click on the `Application settings`, create a settings named: `ConnectionStrings:Database` , and set it value to the connection string you acquired in the last step.

![](../.gitbook/assets/webapp_dbconnstr.PNG)

{% hint style="info" %}
Ensure you enter the connection string in the `Application settings` section and not the `Connection strings` section
{% endhint %}



