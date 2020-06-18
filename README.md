# Q-Rapids Dashboard Jaspersoft Reports

Some templates of Jaspersoft Reports, which can be used with a new reporting functionality of Q-Rapids Dashboard.

## Pre-requisites

In order to work with reports, you need to have install [Jaspersoft Studio](https://community.jaspersoft.com/project/jaspersoft-studio/releases) and [JasperReports Server](https://community.jaspersoft.com/project/jasperreports-server/releases).

## How to work with Jaspersoft Reports

In short, Jaspersoft Studio is used to create and publish reports on JasperReports Server to which one is conecting Q-Rapids Dashboard for generate reports with data.

To configure all, you should follow the next steps:

* **Step 1**. Unzip the "Reports code" zip file from this repository.
* **Step 2**. Import this folder as _Existing Projects into Workspace_ to Jaspersoft Studio.

![import_folder](https://user-images.githubusercontent.com/48628943/85055516-f8c71580-b19d-11ea-8bf3-8e3e17991aa6.png)

* **Step 3**. Configure JasperReports Server connection from _Repository Explover_ tab, right click on _Server_ section and then chose _Create JasperReports Server Connection_ option.

![jasperreports_server_connection](https://user-images.githubusercontent.com/48628943/85054833-f4e6c380-b19c-11ea-8c25-9eece1bdbf00.png)

* **Step 4**. Now reports can be published on Jaspersoft Server. For do it you have to open some report book from _Project Explorer_ and than click on _Publish file to JasperReports Server_ button.

![publish_report](https://user-images.githubusercontent.com/48628943/85056064-dda8d580-b19e-11ea-9582-42af2e982a92.png)

After selecting the directory on publish report (it's important that this directory have to be in another directory named Q-Rapids), you have to choose _Publish Strategy_  for all  _Resources_ as Overwrite.

![publish_report_2](https://user-images.githubusercontent.com/48628943/85058040-d3d4a180-b1a1-11ea-9a8c-efebc236ceb0.png)

* **Step 5**. Finally report is published on JasperReports Server, so now it's possible to use it on Q-Rapids Dashboard. More information about how to use the reporting functionality is available in the corresponding User Guide section [How to manage Jaspersoft reports](https://github.com/q-rapids/qrapids-dashboard/wiki/How-to-manage-Jaspersoft-reports) and in the release [qrapids-dashboard v1.4](https://github.com/q-rapids/qrapids-dashboard/releases/tag/v.1.4).
