---
title: DevOps with Visual Studio Team Services for Java - Hands-on-Labs 
layout: page
sidebar: java
permalink: /labs/java/index.html
folder: /labs/java/
comments: true
---
![](images/all_logo.png)

[Visual Studio Team Services (VSTS)](https://www.visualstudio.com/products/visual-studio-team-services-vs) and [Team Foundation Server (TFS)](https://www.visualstudio.com/tfs/) provide an integrated set of services and tools to manage your software projects, from planning and development through testing and deployment to speed the development and delivery of your software applications across platforms, including iOS, Android, Java, Linux or Windows. 

## Overview  of the Java Hands-on-Lab

DevOps for Java teams with Microsoft Visual Studio Team Services hands-on-lab is provided to give you a first-hand, technical experience on how you can leverage the Microsoft DevOps platform for Java development. The labs cover 
  * Creating a new VSTS account
  * Using the Agile  tools to plan and track work items  
  * Using VSTS with your Eclipse and IntelliJ
  * Running Junit tests and analyzing code coverage with Jacoco and Cobertura
  * Continuous Integration with Team Build or Jenkins
  * Managing Technical Debt with SonarQube 
  * Deploying Docker containers to Azure with an Automated delivery pipeline 
          
 ## VSTS for Java on Ubuntu Virtual Machine Virtual Machine
      
<img src="images/nwc_logo.png"  align="bottom" />

Courtesy of our partner NorthWest Cadence, we have a pre-built virtual machine image that is pre-configured with all the software you require to run through the labs. The "Creating the VM" section below has instructions on how you can run a copy of this image in your own Azure subscription.

## Target Audience

The image and the accompanying hand-on-labs is for technical audience. As such, familiarity with Visual Studio Team Services, Java and Linux operating system would be preferred although it is not a strict prerequisite.

## Hands on Labs

The labs should be followed in the following order, though there are some equivalent labs that allow you a "choose your adventure" experience:

1. [Setting up a new project on VSTS](creatingvstsaccount.html)
1. [Set up a Docker build agent](builddocker.html)
1. Either:
    1. [Cloning a VSTS Repo - IntelliJ](intellij-vsts.html) **OR**
    1. [Cloning a VSTS Repo - Eclipse](eclipse-vsts.html)
1. Either:
    1. [Maven Package Management with VSTS and Jenkins](maven-jenkins.html) **OR**
    1. [Maven Package Management with VSTS Team Build](maven-vsts.html)
1. [Build Docker containers with VSTS](builddocker.html)
1. (Optional) [Managing Technical Debt with SonarQube and VSTS Team Build](techdebt.html)
1. [Release Management with VSTS](deploy.html)
1. Either:
    1. [End to End Workflow - IntelliJ](intellij.html)
    1. [End to End Workflow - Eclipse](eclipsee2e.html)

## Creating the VM

1. Create the VM and dependent resources.
    
    Simply click the Deploy to Azure button below and follow the wizard to create the resources. You will need to log in to the Azure Portal.
                                                                     
	<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fnwcadence%2Fjava-dev-vsts%2Fmaster%2Fenv%2FJavaDevVSTS.json" target="_blank">
		<img src="http://azuredeploy.net/deploybutton.png"/>
	</a>
	<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Fnwcadence%2Fjava-dev-vsts%2Fmaster%2Fenv%2FJavaDevVSTS.json" target="_blank">
		<img src="http://armviz.io/visualizebutton.png"/>
	</a>

    The resources will be deployed to a Resource Group. You can delete the resource group in order to remove all the created resources at any time.

	The VM will take a few minutes (~20) to complete. The VM is installing required software and configuring the environment for the labs.

If you require assistance with these labs, you can contact Northwest Cadence through their [website](http://nwcadence.com).

## Start the Labs
Once the VM has been provisioned, remote desktop to the machine and log in. You can then [start the labs](labs/readme.md).

1. Get the IP address/DNS name of the machine.

In the Azure portal, select the VM to view details about it in the Overview panel and copy the Public IP address (optionally, copy the DNS name instead).

<img src ="images/azure-copy-ipaddress.png">

1. Remote into the machine in Windows.

If accessing the VM from a Windows machine, paste in the IP address/DNS name into a Remote Desktop Connection window followed by a colon and the 3389 port. This will allow you to view the GUI of the Linux VM desktop.

<img src ="images/rdp-connect-vm.png">

In the RDP session, you will need to put your credentials set earlier to log into the machine. 

## Troubleshooting

If you see the older xrdp client when logging onto the virtual machine for the first time (see below image), restart the virtual machine through the Azure portal to apply the recent configuration updates from the ARM template deployment. A newer client should appear to log into.  

<img src ="images/xrdp.png">
