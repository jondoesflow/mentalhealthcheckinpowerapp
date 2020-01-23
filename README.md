# mentalhealthcheckinpowerapp
This is a mental health check in application built in Microsoft PowerApps and Power Automate

Import the Power App ZIP file - MentalHealthCheckInAreyouOKPowerApp_20200123162853.zip

Uploading and creating the Resources by Topic Area list:

1. Open the "resources by topic title.iqy" file and save as an XLSX document
2. Open IE as an administrator
3. Go to your sharepoint site
4. Go to Site Contents
5. Go to Settings Cog
6. Click Add an App
7. Search for "spreadsheet"
8. Click Import Spreadsheet
9. Name: "Resources by Topic Area" or Name: "Mental Health"
10. Choose file: resources by topic title.xlsx or mental health.xlsx
11. In the selcted range drop down select the only option avaialble
12. Click Import
13. The list will have been uploaded.

Do steps 1 - 13 above for "mental health.iqy" file

Go to your Data Sources in the Power App

1. Remove the current Resources by Topic Area sharepoint connection
2. Click Connectors to expand
3. Click Sharepoint
4. Choose the Sharepoint connector for your tenant
5. Chose your Sharepoint in your tenant
6. Click the check box on "Resources by Topic Area"
7. Click Connect

Go to the FurtherInformation page

1. Click on the 1st dropdown control "DropdownTopic" ensure Items object is set to "Sort(Distinct(ColResources,'Topic Name'),Result)"
2. Click on the 2nd dropdown control "DropdownOrganisation" ensure Items object is set to "Filter(ColResources,'Topic Name'=DropdownTopic.Selected.Result)"


THIS COMPLETES THE POWER APP SETUP

Power Automate:

1. Go to the Are you ok main flow
2. Select the Sharepoint site address for your tenant
3. Choose "Mental Health" for the list name
4. Associate the variables with the list columns

In the App Start config, remember to change the phone numbers for your Occupational Health and Third Party Support (if you have one.  They are currently set to 111111.


TEST THE POWER APP
