# Azure-Automation-Account-Restart-Virtual-Machine

We have several solutions to start and stop the virtual machines from the Azure Automation account, but what if we want to restart the virtual machine from the Azure Automation account? 

Well, we have a solution for that. Azure automation account - Custom runbook. 

In this article, we will see how we can configure an Azure VM restart at the scheduled time with Azure Automation Account.

The main purpose of the task is to automate the task and save the engineer's manual work and perform the activity at scheduled times.

To view the PowerShell script and step-by-step process, see the GitHub repository link below.
(Click the link below for the PowerShell script.)
https://github.com/prasad-metkar/Azure-Automation-Account-Restart-Virtual-Machine


***Step by Step process of Azure Automation Account Runbook configuration for Restart Virtual Machine:***

**Step 1:**
Login to your Microsoft Azure portal.

<img src="Images/Image 1.png" alt="Alt text" title="Optional title">
 

**Step 2:**
Open the “Automation Accounts” service

<img src="Images/Image 2.png" alt="Alt text" title="Optional title">

Here, I have already created an Automation account, and this is the overview page of my Automation account. (If you don’t have an Automation account, first create an automation account.)<br/>

Note: In this Automation account makes sure “Run as accounts” is configured.<br/>

Required RBAC permission: Subscription Admins role and co-administrator of the subscription.<br/>

How to create an automation account - https://learn.microsoft.com/en-us/azure/automation/quickstarts/create-azure-automation-account-portal

<img src="Images/Image 3.png" alt="Alt text" title="Optional title">
 
**Step 3:**
Open “Runbook” and click on “Create a runbook”

<img src="Images/Image 4.png" alt="Alt text" title="Optional title"> 


**Step 4:**
Enter Runbook name, Runbook type select PowerShell, Runtime version select 5.1<br/>
Once all required details are entered. Click on Create

<img src="Images/Image 5.png" alt="Alt text" title="Optional title"> 

After clicking on Create, the below page will be open. 
Here you need to add a PowerShell script.

PowerShell script you can find in my GitHub repository folder. Folder name: PowerShell Script

In the PowerShell script change your _“Virtual machine Resource Group name”_ and _“Virtual machine name”_<br/>

Click on “Save” and “Publish”

<img src="Images/Image 6.png" alt="Alt text" title="Optional title">

**Step 5:**
**Add ‘Schedule”**

On the Overview page of the Runbook. Click on “Link to schedule”

<img src="Images/Image 7.png" alt="Alt text" title="Optional title"> 

**Step 6:**


Click on “Link a schedule to your runbook”

<img src="Images/Image 8.png" alt="Alt text" title="Optional title">
 
 Add the details as per your requirement – Name of Schedule, Starts, Time zone, Recurrence<br/>
Once all details are entered click on “Create”

<img src="Images/Image 9.png" alt="Alt text" title="Optional title"> 

In the “Configure parameters and run settings” add – Target Virtual machine Resource group name and “Virtual machine name” and click on “Ok”

<img src="Images/Image 10.png" alt="Alt text" title="Optional title">

Once the “Schedule” and “Parameters and run settings” details are entered.<br/> 
Click on “OK”

<img src="Images/Image 11.png" alt="Alt text" title="Optional title">

*To start creating an automation account Runbook. Click on “Start” on the Overview page of Runbook.*

<img src="Images/Image 12.png" alt="Alt text" title="Optional title">

Step
**To test the configured runbook.<br/>
Click on “Edit” → “test Pane” → “Start”**

<img src="Images/Image 13.png" alt="Alt text" title="Optional title">

<img src="Images/Image 14.png" alt="Alt text" title="Optional title">

<img src="Images/Image 15.png" alt="Alt text" title="Optional title">
