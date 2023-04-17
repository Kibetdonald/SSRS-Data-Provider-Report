# SSRS-Data-Provider-Report
This project is a sample implementation of a SSRS Data Provider Report in Dynamics 365 Finance and Operations. The report retrieves data from the Sales Agreement Header table and displays it in a table format.


## Requirements:
1. New SSRS Report with precision design
2. Data Provider Class: will provide three data sets for the SSRS Report
3. Data Contract Class: will define and carry the values of the report parameters
4. Three temporary tables: will define and carry the report data
5. Controller class: Will handle the report dialog form
6. Menu item: Will open the report in the viewer

## Process
Step 1: Create the report temporary tables
The three data sets include:

  - DocAgreementHeader – used for a sales agreement’s header data.
  - DocAgreementLine – used for a sales agreement’s lines data.
  - DocAgreementContact – used for a sales agreement’s customer contact data
   
**POV: Set the table type properties to Inmemory and add fields to the tables**

Step 2: Create the controller class
 - It orchestrates the report execution

Step 3: Create the Data Contract Class
 - It defines and stores the values of the report parameters. 

Step 4: Create the Data Provoider Class
 - It extends the SRSReportDataProviderBase and implements the processReport method. The processMethod is used to fetch the report data and fill the temporary tables

Step 5: Set the report data source to ta Data Provider class
 - Add a data set to the report and set its Data Source Type property to Report Data Provider. 

Step 6: Create the report design
 - Add a new precision design

Step 7: Create the report menu items
 - Create an extension for the SalesAgreement menu and add the output mene items onto it.
 
Step 8: Execute the report

Overall that is brief implementation of SSRS Data Provider Report
