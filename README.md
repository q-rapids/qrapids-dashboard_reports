# Q-Rapids Dashboard Jaspersoft Reports

Some templates of Jaspersoft Reports, which can be used with a new reporting functionality of Q-Rapids Dashboard.

## Pre-requisites

In order to work with reports, you need to have installed [Jaspersoft Studio](https://community.jaspersoft.com/project/jaspersoft-studio/releases) and [JasperReports Server](https://community.jaspersoft.com/project/jasperreports-server/releases).

## How to work with Jaspersoft Reports

In short, Jaspersoft Studio is used to create and publish reports on JasperReports Server to which one is conecting Q-Rapids Dashboard for generate reports with data.

To configure all, you should follow the next steps:

* **Step 1**. Unzip the "Reports code" zip file from this repository.
* **Step 2**. Import this folder as _Existing Projects into Workspace_ to Jaspersoft Studio.

![import_folder](https://user-images.githubusercontent.com/48628943/85055516-f8c71580-b19d-11ea-8bf3-8e3e17991aa6.png)

* **Step 3**. In _Project Explorer_ tab (inside of _Reports code_), you need to open _QRapids Data Adapters_ folder and update all **xml** files. Write the correct datasource url, especifing the connection to the corresponding ([dashboard RESTful service](https://q-rapids.github.io/qrapids-dashboard/) providing the data you want to use in the report.

![data_adapters_configuration](https://user-images.githubusercontent.com/48628943/85123298-4e480480-b228-11ea-980c-a3f1e47a0d01.png)

* **Step 4**. Configure JasperReports Server connection from _Repository Explover_ tab, you need to right click on _Server_ section and then chose _Create JasperReports Server Connection_ option.

![jasperreports_server_connection](https://user-images.githubusercontent.com/48628943/85054833-f4e6c380-b19c-11ea-8c25-9eece1bdbf00.png)

* **Step 5**. Now reports are ready to be published on Jaspersoft Server. For publishing reports, you have to open the report **jxml** file (from _Project Explorer_ tab, inside of _Reports code_ folder) and then click on _Publish file to JasperReports Server_ button.

![publish_report](https://user-images.githubusercontent.com/48628943/85124931-04145280-b22b-11ea-978d-57d3c2e62e8a.png)

After selecting the folder where the report will be published, you have to choose _Publish Strategy_  for all  _Resources_ as Overwrite.

**Important**: All the reports and folders need to be published inside a folder named **Q-Rapids**. Only the reports and folders inside the folder **Q-Rapids** will be available from the dashboard.

![publish_report_2](https://user-images.githubusercontent.com/48628943/85058040-d3d4a180-b1a1-11ea-9a8c-efebc236ceb0.png)

* **Step 6**. Finally reports are published on JasperReports Server, so now you have to configure Q-Rapids Dashboard to be able to access to them from the dashboard. Modify the dashboard configuration file (`application.properties`) adding the following fields:

    **jasperServer.url=**`<JASPER SERVICE URL>` <br/>
    **jasperserver.user=**`<JASPER SERVER USERNAME>` <br/>
    **jasperserver.password=**`<JASPER SERVER PASSWORD>` <br/>

For more information about dashboard configuration file consult [Configuration File](https://github.com/q-rapids/qrapids-dashboard/wiki/Configuration-File).

* **Step 7**. The configuration is finished, so now you can generate reports on Q-Rapids Dashboard. 

More information about how to use the reporting functionality from the dashboard is available in the[Reporting](https://github.com/q-rapids/qrapids-dashboard/wiki/Reporting) User Guide section.
