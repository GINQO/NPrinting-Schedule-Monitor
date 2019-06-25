# GINQO NPrinting Schedule Monitor
This App shows information about NPrinting tasks and schedules and give a calendar overview of task scheduled. It loads the information from the NPrinting Repository Database and runs a specific Failed Task NPrinting Report when there are 1 or more failed NPrinting taks. 

![](demo.gif)

# Prerequisites
Qlik Sense >= November 2018 
Data Connection to NPrinting Repository Database

# Installation
1. Download this Qlik Sense app in a zip file using the 'Clone or Download' button
2. Extract the qvf file from the zip
2. Navigate to 'Apps' under the QMC (Qlik Management Console)
3. Import the qvf file

# Getting Started
1. Navigate to the Data Load Editor
2. Create a Data Connection to the REST API for GET and POST and to the NPrinting Repository Database
3. Navigate to the Set Variables tab
4. Add the created connection names to the variables for vAPIConnectionNameForGET, vAPIConnectionNameForPOST and vNPRepoConnection
5. Set the correct servers in the vNPrintingServer and vQlikSenseServer
6. Set the NPrinting Publish Task Name in vNPrintingPublishTaskName if you created a NPrinting report and Publish task for Failed reports
7. In the CALL NP API tab there is a check to validate if there are Failed Tasks, if so the report get's send out.

# NPrinting Report Template	
1. Create a NPrinting app called NPrinting Schedule Monitor
2. Create a connection to the Qlik Sense Schedule Monitor app in Qlik Sense
3. Navigate to Reports in NPrinting and press import report and choose the NPrinting Schedule Monitor App
4. Import the zip file NPrinting Daily Failed Task Report Template.zip by browsing to the zip file
5. Press Next
6. Give the Report a title or use the existing title and press Next
7. Choose connection you created and press Next
8. In the Filters screen press Next
9. In the Summary screen validate the choices made and press Confirm

# Reload the app
1. Open Qlik Sense and navigate to the Schedule Monitor app.
2. Run a manual reload to see if everything works
3. Schedule the reload of this app in the QMC Task Scheduler
4. If a NPrinting task has failed the NPrinting Report will be send out


# Authors
GINQO

# Change Log

# Known Issues and Limitations