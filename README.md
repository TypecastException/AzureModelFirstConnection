Connection String Template 
-------------------------------------
for Windows Azure/EF Model-First Database
-----------------------------------------------------------

Sometimes we need to develop using Entity Framework in a Model First or Database-First context. If we deploy a website using EF Model First to Windows Azure Websites, the connection string and configuration can be finicky, and it can be difficult to tell what we are doing wrong. 

The connection string pattern below can be used directly in the Azure Website Connection String Configuration settings, after replacing the bracketed items with your own values (replace the brackets too - they are not part of teh connection string). 

Name the connection string in the configuration panel to match the Model-First Connection string in your Web Application. 
<dl>
  <dt>The Azure Connection String for Model-First Connection:</dt>
  <dd>
metadata=res://*/Models.<AzureDatabaseName>.csdl|res://*/Models.<AzureDatabaseName>.ssdl|res://*/Models.<AzureDatabaseName>.msl;provider=System.Data.SqlClient;provider connection string="data source=tcp:<AzureServerName>.database.windows.net;initial catalog=<AzureDatabaseName>;Persist Security Info=True;User ID=<UserLogIn>@<AzureServerName>;Password=<UserPassword>"
  </dd>
</dl>


For more information, see the related post at:


