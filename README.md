# End-to-End Web App Deployment on Azure Using Terraform and Azure DevOps
<h2>Overview:</h2>
This project demonstrates an automated end-to-end deployment pipeline for a .NET web application hosted on a Windows Virtual Machine (VM) in Azure. It utilizes Terraform for infrastructure provisioning, PowerShell for VM configuration, and Azure DevOps for CI/CD pipeline management. The goal is to deploy a secure, scalable, and maintainable production-like environment with minimal manual effort.

<h2>Tech Stack</h2>
&nbsp;&nbsp;&nbsp;•	Terraform – Infrastructure as Code (IaC) to automate Azure resource provisioning
&nbsp;&nbsp;&nbsp;•	Azure Virtual Machines – Windows-based hosting environment
&nbsp;&nbsp;&nbsp;•	.NET Hosting Bundle – Runtime for ASP.NET Core apps on IIS
&nbsp;&nbsp;&nbsp;•	PowerShell – VM and service configuration scripts
&nbsp;&nbsp;&nbsp;•	Azure DevOps – Source control, pipeline, and deployment automation
&nbsp;&nbsp;&nbsp;•	GitHub – Source code repository (imported into Azure Repos)
&nbsp;&nbsp;&nbsp;•	IIS (Internet Information Services) – Windows web server for hosting the application

<h2>Steps:</h2>
<h3>1.	Infrastructure Setup with Terraform</h3>
&nbsp;&nbsp;&nbsp;•	Create Resource Group
&nbsp;&nbsp;&nbsp;•	Create Virtual Network and Subnet
&nbsp;&nbsp;&nbsp;•	Create Windows VM with public IP
&nbsp;&nbsp;&nbsp;•	Attach Network Security Group allowing RDP and HTTP
&nbsp;&nbsp;&nbsp;•	Run the Terraform script in terminal
<h3>2.	Set up the VM with RDP</h3>
&nbsp;&nbsp;&nbsp;•	Add Web server(IIS) under Server Roles 
&nbsp;&nbsp;&nbsp;•	Add .Net Framework 3.5 Features 
<h3>3.	Installing .NET and Hosting Bundle</h3>
<h3>4.	Importing GitHub Repo into Azure Repos</h3>
&nbsp;&nbsp;&nbsp;•	Go to Azure Devops Dashboard
&nbsp;&nbsp;&nbsp;•	Go to Azure repos
&nbsp;&nbsp;&nbsp;•	Click Import a repository
&nbsp;&nbsp;&nbsp;•	Paste your GitHub repo URL 
<h3>5.	Create Deployment Group</h3>
&nbsp;&nbsp;&nbsp;•	Go to Pipelines > Deployment groups
&nbsp;&nbsp;&nbsp;•	Create new group and copy the registration PowerShell script 
&nbsp;&nbsp;&nbsp;•	Run it on your Azure VM to register the agent 
<h3>6.	Create a New Pipeline</h3>
&nbsp;&nbsp;&nbsp;•	Go to Pipelines > Add Pipeline
&nbsp;&nbsp;&nbsp;•	Select source as azure repos
<h3>7.	Release Pipeline Configuration</h3>
&nbsp;&nbsp;&nbsp;•	Go to Pipelines > Releases and create a new release pipeline
&nbsp;&nbsp;&nbsp;•	Add an artifact from the build pipeline
&nbsp;&nbsp;&nbsp;•	Create Release 

<h2>Outcome</h2>
&nbsp;&nbsp;&nbsp;•	A Windows VM is created and configured
&nbsp;&nbsp;&nbsp;•	.NET Hosting Bundle is installed
&nbsp;&nbsp;&nbsp;•	Code is deployed from GitHub via Azure DevOps release pipeline
&nbsp;&nbsp;&nbsp;•	IIS is hosting the deployed web app

