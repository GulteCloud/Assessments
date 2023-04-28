# WAF Security Optimization Workbook

As part of this assessment, the WAF Cost Optimization workbook has to be deployed.

## Workbook Pre-requisites

The following Azure resource providers must be registered on the in-scope subscriptions:

- Microsoft.Advisor  
- Microsoft.ResourceHealth  
- Microsoft.Security  

A cloud account with Built-in Reader role assigned to all in-scope subscriptions, or their parent management group.  

* [Optional] The RBAC role Monitor Contributor is required to save workbook.

## Workbook Deployment Guide

The following resources can be used to deploy the workbook into Azure monitor:

- [JSON Deployment guide](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/workbooks-automate#azure-resource-manager-template-for-deploying-a-workbook-in) - A guide to create workbooks using a **JSON Template**.

- [ARM Template Deploy Guide](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/workbooks-automate#azure-resource-manager-template-for-deploying-a-workbook-instance) - A guide to deploy the workbook as an **ARM Template**.

- [Security WorkBook.json](https://microsoft.sharepoint.com/teams/ASDIPRelease/IP%20Release/Forms/AllItems.aspx?viewid=971b6985%2D5ac6%2D47e5%2Da6dc%2D5c0664b149a9&id=%2Fteams%2FASDIPRelease%2FIP%20Release%2FSecure%20Infrastructure%2FAssessment%20Program%2FWell%2DArchitected%20Security%20Assessment%2F4%2DDelivery%20Artifacts%2F1%2DAzureMonitorWorkbook) - This workbook will present various security related details from Azure Security Center and Azure Advisor.
