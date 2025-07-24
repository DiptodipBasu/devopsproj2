# End-to-End Web App Deployment on Azure Using Terraform and Azure DevOps
<h2>Overview:</h2>
This project demonstrates an automated end-to-end deployment pipeline for a .NET web application hosted on a Windows Virtual Machine (VM) in Azure. It utilizes Terraform for infrastructure provisioning, PowerShell for VM configuration, and Azure DevOps for CI/CD pipeline management. The goal is to deploy a secure, scalable, and maintainable production-like environment with minimal manual effort.

<h2>Tech Stack</h2>
&nbsp;&nbsp;&nbsp;•	Terraform – Infrastructure as Code (IaC) to automate Azure resource provisioning<br>
&nbsp;&nbsp;&nbsp;•	Azure Virtual Machines – Windows-based hosting environment<br>
&nbsp;&nbsp;&nbsp;•	.NET Hosting Bundle – Runtime for ASP.NET Core apps on IIS<br>
&nbsp;&nbsp;&nbsp;•	PowerShell – VM and service configuration scripts<br>
&nbsp;&nbsp;&nbsp;•	Azure DevOps – Source control, pipeline, and deployment automation<br>
&nbsp;&nbsp;&nbsp;•	GitHub – Source code repository (imported into Azure Repos)<br>
&nbsp;&nbsp;&nbsp;•	IIS (Internet Information Services) – Windows web server for hosting the application<br>

<h2>Steps:</h2>
<h3>1.	Infrastructure Setup with Terraform</h3>
&nbsp;&nbsp;&nbsp;•	Create Resource Group<br>
&nbsp;&nbsp;&nbsp;•	Create Virtual Network and Subnet<br>
&nbsp;&nbsp;&nbsp;•	Create Windows VM with public IP<br>
&nbsp;&nbsp;&nbsp;•	Attach Network Security Group allowing RDP and HTTP<br>
&nbsp;&nbsp;&nbsp;•	Run the Terraform script in terminal<br>
<h3>2.	Set up the VM with RDP</h3>
&nbsp;&nbsp;&nbsp;•	Add Web server(IIS) under Server Roles <br>
&nbsp;&nbsp;&nbsp;•	Add .Net Framework 3.5 Features <br>
<h3>3.	Installing .NET and Hosting Bundle</h3>
<h3>4.	Importing GitHub Repo into Azure Repos</h3>
&nbsp;&nbsp;&nbsp;•	Go to Azure Devops Dashboard<br>
&nbsp;&nbsp;&nbsp;•	Go to Azure repos<br>
&nbsp;&nbsp;&nbsp;•	Click Import a repository<br>
&nbsp;&nbsp;&nbsp;•	Paste your GitHub repo URL <br>
<h3>5.	Create Deployment Group</h3>
&nbsp;&nbsp;&nbsp;•	Go to Pipelines > Deployment groups<br>
&nbsp;&nbsp;&nbsp;•	Create new group and copy the registration PowerShell script <br>
&nbsp;&nbsp;&nbsp;•	Run it on your Azure VM to register the agent <br>
<h3>6.	Create a New Pipeline</h3>
&nbsp;&nbsp;&nbsp;•	Go to Pipelines > Add Pipeline<br>
&nbsp;&nbsp;&nbsp;•	Select source as azure repos<br>
<h3>7.	Release Pipeline Configuration</h3>
&nbsp;&nbsp;&nbsp;•	Go to Pipelines > Releases and create a new release pipeline<br>
&nbsp;&nbsp;&nbsp;•	Add an artifact from the build pipeline<br>
&nbsp;&nbsp;&nbsp;•	Create Release <br>

<h2>Outcome</h2>
&nbsp;&nbsp;&nbsp;•	A Windows VM is created and configured<br>
&nbsp;&nbsp;&nbsp;•	.NET Hosting Bundle is installed<br>
&nbsp;&nbsp;&nbsp;•	Code is deployed from GitHub via Azure DevOps release pipeline<br>
&nbsp;&nbsp;&nbsp;•	IIS is hosting the deployed web app<br>

