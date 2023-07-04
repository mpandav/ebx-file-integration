# EBX (MDM) File based Integration between Target System(s) [Salesforce & Jira]

This will demonstrate the File based integration between MDM System (EBX) and Target Systems likes of Salesforce or JIRA. The same methodology can be applied with other target systems as well, Ex. SAP Systems, DBs, etc. - The EBX (MDM) System export the required Company Data in form of .csv in shared directory where BusinessWorks is watching over through file poller. It will poll the file(s) at every 5 sec and subsequently process the received files.


## Usecase
We will have below usecases covered in this demonstration:
- The EBX (MDM) System export the required Company Data in form of .csv in shared directory
- TIBCO BusinessWorks is watching over through file poller and poll the file(s) at every 5 sec
- Once file is received, processed the files based on control flags to decide which target (saleforce/jira) to select.
- Based on received & processed data, create the records:
  -  in Salesforce using SF plugin
  - in JIRA System using ReST APIs

## Solution Architecture

The Solution architecture depicts the working mechanism of the solution. How data will be travelled end-to-end from source to the target system. 

![image](https://github.com/mpandav/ebx-file-integration/assets/38240734/d1bd8cf9-42ab-4856-8710-3b548b1b5a4f)

## How to setup or run?
- Download the repo to some directory /tmp/
- Import the application into BusinessStudio
- Check the Application properties and update them according your enviroment. Important App properties are as below:
  - SharedLib Properties: contains shared resources config info (HTTP, Salesforce)- Update them accordingly.
  - FileHandler App Module: contains properties:
    - FileMetaData: FileName and location
    - Controllers: These will controll the behavior of the Main process and decide which branch to execute; salesforce_update or jira_update or none.
    - DataOps: It will decide how many records, needs to be read from file at once. Default value is 5.
- Once corrected the App properties, your application is ready to run.
- Go to Debug/Run configuraion > select all the processes > click Debug/Run

## Demo
Short demo video showing working on the solution.

https://github.com/mpandav/ebx-file-integration/assets/38240734/87165ffe-a69e-4976-8461-77b563995e77

