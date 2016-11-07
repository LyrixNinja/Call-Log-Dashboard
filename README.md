# Call-Log-Dashboard
A repository for all aspects of the call log dashboard

The CallLogDashboard covers all of the code to support the data of 2020 Legal incoming calls, ResourceTap Incoming calls and the ResourceTap database entries. This includes:

  1. Introduction (this readme file)
  2. Data ETL processes
  3. Tableau dashboard files
  
1. Introduction:
This data management process will monitor the data for our incoming calls (2020 Legal and ResponseTap) to ensure that we are answering all calls that come in from ResponseTap and that we are not losing any data along the way.

2. Data ETL Processes

2.1 Every week, IT (Stephen White) extracts a file from our telephone system that shows all calls received for the previous week. The file is stored in the following directory: "\\CAMPSRV04\Shared\Support\Call Lists Exported". This file needs to be uploaded into the [CAMPSQL02].[Marketing].[dbo].[CallLog2020_External] table - the import job for this is stored in the same directory and is called [Call Log import - 2020 Legal]. Ideally this job will become automated, but for now is a manual task to be run every Monday morning once the file is available

2.2 Every day, we need to extract the call log from the ResponseTap website. This process will become a scheduled FTP process, but  (Stephen White) extracts a file from our telephone system that shows all calls received for the previous week. The file is stored in the following directory: "\\CAMPSRV04\Shared\Support\Call Lists Exported". This file needs to be uploaded into the [CAMPSQL02].[Marketing].[dbo].[CallLog2020_External] table - the import job for this is stored in the same directory and is called [Call Log import - 2020 Legal]. Ideally this job will become automated, but for now is a manual task to be run every Monday morning once the file is available
