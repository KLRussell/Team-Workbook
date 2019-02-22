*******************************************************************************************************************************************
-------------------------------------------------------------------------------------------------------------------------------------------
-----                                                     CAT Operations Project                                                      -----
-----                                                        By Kevin Russell                                                         -----
-------------------------------------------------------------------------------------------------------------------------------------------
*******************************************************************************************************************************************

Hello All,

This project corresponds to Python-Vacuum-Automation on GitHub.com and precedes project PowerShell-Vacuum-Automation. Let me explain this
project and how this all interacts together.

At my current position, I work on a team that categorized in five sub-teams, Audit, DART, CARP, PFA, and CDA. Each sub-teams specialize in
different aspects in the Cost Assurance Team. The issue is that each team perform daily tasks that can be very time consuming and repetitive.

To address this issue, our team developed several workbooks to tackle these process. One for auditing, a second for filing billing
disputes, a third for updating disputes, and a fourth to place notes on disputes. Each workbook was a very manual process, and it isn't
efficient for minimizing cost for Granite.

To fix this, we developed a PowerShell script, years ago, to automate auditing. However, the other workbooks were manual and tedious to
accomplish. Additionally, we have alot of overlap and redundancies in each individual process.

These issues are addressed in this current project CAT Operations. In this project, all workbooks are combined into one workbook. This
Workbook can be found in 03_Source_Code/03_CNR_Workbook/. Additionally, the workbook performs common validation and required field checks.
When users upload updates, the workbook will cut the updates into XML within 4 possible directories within 01_Updates.

As soon as these XML spreadsheets populate into the directory, a Python script that is running continuously in the background will process
each xml file. The python script will parse the XML, validate the information for errors, and will process the updates in Granite's SQL
Server. Currently, this project is on-going and is incomplete. The most up to date source files for the python automation is found on my
GitHub website. These files should be placed in the 03_Source_Code folder.

To use this project in its entirety, you will need to fill in the necessary variables in Vacuum_Settings.xml and ensure that the tables
exist in your SQL Server database with data.

Please see the Updates_Flowchart.jpg to see how this system process updates.