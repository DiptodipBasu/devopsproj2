# End-to-End Web App Deployment on Azure Using Terraform and Azure DevOps
<h2>Overview:</h2>
This project demonstrates an automated end-to-end deployment pipeline for a .NET web application hosted on a Windows Virtual Machine (VM) in Azure. It utilizes Terraform for infrastructure provisioning, PowerShell for VM configuration, and Azure DevOps for CI/CD pipeline management. The goal is to deploy a secure, scalable, and maintainable production-like environment with minimal manual effort.

<h2>Tech Stack</h2>
•	Terraform – Infrastructure as Code (IaC) to automate Azure resource provisioning
•	Azure Virtual Machines – Windows-based hosting environment
•	.NET Hosting Bundle – Runtime for ASP.NET Core apps on IIS
•	PowerShell – VM and service configuration scripts
•	Azure DevOps – Source control, pipeline, and deployment automation
•	GitHub – Source code repository (imported into Azure Repos)
•	IIS (Internet Information Services) – Windows web server for hosting the application

<h2>Steps:</h2>
<h3>1.	Infrastructure Setup with Terraform</h3>
•	Create Resource Group
•	Create Virtual Network and Subnet
•	Create Windows VM with public IP
•	Attach Network Security Group allowing RDP and HTTP
•	Run the Terraform script in terminal
<h3>2.	Set up the VM with RDP</h3>
•	Add Web server(IIS) under Server Roles 
•	Add .Net Framework 3.5 Features 
<h3>3.	Installing .NET and Hosting Bundle</h3>
<h3>4.	Importing GitHub Repo into Azure Repos</h3>
•	Go to Azure Devops Dashboard
•	Go to Azure repos
•	Click Import a repository
•	Paste your GitHub repo URL 
<h3>5.	Create Deployment Group</h3>
•	Go to Pipelines > Deployment groups
•	Create new group and copy the registration PowerShell script 
•	Run it on your Azure VM to register the agent 
<h3>6.	Create a New Pipeline</h3>
•	Go to Pipelines > Add Pipeline
•	Select source as azure repos
<h3>7.	Release Pipeline Configuration</h3>
•	Go to Pipelines > Releases and create a new release pipeline
•	Add an artifact from the build pipeline
•	Create Release 

<h2>Outcome</h2>
•	A Windows VM is created and configured
•	.NET Hosting Bundle is installed
•	Code is deployed from GitHub via Azure DevOps release pipeline
•	IIS is hosting the deployed web app

