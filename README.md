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

## References

## Demo
