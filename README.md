PowerBI workspace template for Microsoft LaaS OpenEdx installations
=====

This is a template for reporting student activity on OpenEdx.

HOWTO
=====

Configure app.powerbi.com workspace with permissive gateway:

### 1. Authorization in Power BI Gateway on Windows Server

- Connect to Windows server via RDP with additionally provided credentials
- Run Power BI Gateway
- Click "Sign in", enter your Office365 email and password
- Go to "Network" in right menu bar, check connection by "Check now" button
- Don't close Gateway window and terminate RDP session

### 2. Configure Gateway connection and Data Source Settings
- Sign in into https://app.powerbi.com
- Choose workspace you need
- Go to "Settings" menu, choose "Manage gateways"

![manage gateways screenshot](doc/images/manage_gateways.png)

- Power BI Web Application will detect your Gateway
- Add "Data Source" with additionally provided MySQL credentials and settings, configure Advanced settings and Users, if you need

![data source settings](doc/images/data_source_settings.png)

- Press "Test all connections" button.

### 3. Add and configure a report template
- Download the report template from [GitHub](LaaSOpenEdx.pbix)
- Go to "Get data" in bottom of your management panel 
- Import downloaded .pbix file from local storage

![template import screenshot](doc/images/import.png)

- Go to "Settings" and choose "Datasets" 

![databases settings screenshot](doc/images/databases_settings.png)

- Gateway connection must look like this in when all is okay

![gateway connection](doc/images/gateway_connection.png)

- Configure you Scheduled refresher and apply the changes

![scheduler](doc/images/scheduler.png)

- Go to your Workspace, Datasets column, click on "Refresh now" in Action column

![dataset refresh](doc/images/datasets_refresh.png)

- Choose your report in Reports, it must be with your data now.  
