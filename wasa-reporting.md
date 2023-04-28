# Reporting

## Create a program in Services Hub

Services Hub programs are a digital improvement plan customers can use to track progress on execution of improvement actions.  Visit the Services Hub docs page for more details on [how to use Programs](https://docs.microsoft.com/en-us/services-hub/programs).

## Create Top Findings improvement plan

1. Navigate to Programs under IT Health and select _Create new program_.

2. Select Custom program

3. Provide Name, Description, Outcome.

4. Add the top 3-5 recommendations from the survey and/or data insights, and supporting details.

> [!NOTE]
> The intent of identifying 3-5 top recommendations is for it to be a manageable set of improvement tasks that are highly actionable and will drive meaningful and measurable improvements in the security of the scoped workload. It is not meant to be a _hard_ limit.

## Report generation script and import recommendations scripts

The scripts utilized are now under the WARP reporting script.  The repository can be found [here.](https://github.com/Azure/WellArchitected-Tools/tree/main/WARP/devops)  
PowerShell 7 is recommended for these scripts.  Installation instructions can be found at the [PowerShell Documentation](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.2) site.  

1. Open a PowerShell terminal and run the following commands from within a new or existing directory:

    $installUri = "https://raw.githubusercontent.com/Azure/WellArchitected-Tools/main/WARP/devops/install-WARP-tools.ps1"  
    Invoke-WebRequest $installUri -OutFile "install-WARP-tools.ps1"  
    .\install-WARP-tools.ps1  

2. Running the install-WARP-tools.ps1 will download all the files required for report generation / importing recommendation scripts. 

> [!NOTE]
> The install-WARP-tools.ps1 will also update existing scripts in the same location.


## Build the Recommendations and Optimizations Executive Summary presentation

To generate the Executive Summary presentation and export the recommendation tasks to Azure DevOps or GitHub actions you will need to download and run the reporting scripts.

1. Download the csv report of the completed assessment.

2. Open an instance of PowerShell 7 and open the run [install-WARP-tools.ps1](https://raw.githubusercontent.com/Azure/WellArchitected-Tools/main/WARP/devops/install-WARP-tools.ps1) to obtain the latest version.

3. Run the script `GenerateWAFReport.ps1`.

4. The script will prompt you to select the csv report that was downloaded.

5. After the script completes, close the PowerPoint and PowerShell windows and locate the generated PPT in the working directory with the current timestamp.

>[!NOTE]
>6. Merge relevant slides from the generated PPT into the delivery artifact `Well-Architected Security Assessment  - Recommendations and Optimizations Executive Summary` and populate the deck with the TOP 3-5 recommendations, the recommendation roadmap (30/60/90), and any additional slides you want to include in the final presentation, e.g.: Microsoft Cybersecurity Reference Architectures, Enterprise Scale, etc. 

7. You can use the [WAF Cost Assessment](https://microsoft.sharepoint.com/teams/ASDIPRelease/IP%20Release/Forms/AllItems.aspx?csf=1&web=1&e=ylspCS&cid=45d992d5%2D97a2%2D47b4%2D8f16%2D3363ba3d91ac&FolderCTID=0x012000F569B1CB3A2B2D499B8B6646AC5C92E3&id=%2Fteams%2FASDIPRelease%2FIP%20Release%2FSecure%20Infrastructure%2FAssessment%20Program%2FWell%2DArchitected%20Cost%20Optimization%20Assessment%2F4%2DDelivery%20Artifacts%2F3%2DWorkbook&viewid=971b6985%2D5ac6%2D47e5%2Da6dc%2D5c0664b149a9) workbook to generate a map displaying the Azure locations of the customers resources.

## Import recommendations into task tracking tool

Ask the customer if they have experience or preference for tracking remediation tasks/projects using Azure DevOps or GitHub.  Take the time to demonstrate both platforms if needed. Have customer select which tool they prefer and import the recommendations accordingly per the below guidance.

> [!NOTE]
> The customer can do the import themselves by following this [guide](https://github.com/Azure/WellArchitected-Tools/tree/main/WARP/devops).

### Import recommendations to Azure DevOps

[!include[Import Recommendation Scripts](~/articles/articles_pnp/pnp_devops.md)]

### Import recommendations to GitHub

1. Run [install-WARP-tools.ps1](https://raw.githubusercontent.com/Azure/WellArchitected-Tools/main/WARP/devops/install-WARP-tools.ps1) to obtain the latest version and required files.

2. [If you don't already have one, create a GitHub account.](https://github.com/).

3. [Create a new GitHub Repository if one does not exist.](https://docs.github.com/github/getting-started-with-github/create-a-repo).

4. [Acquire a personal access token (PAT) with write access to create issues (Full control of private repositories).](https://docs.github.com/github/authenticating-to-github/creating-a-personal-access-token) Make sure you use a short expiration time for the PAT.

5. Ensure the Category Descriptions file exists in the working directory path before attempting to run this script.

6. Open an instance of PowerShell 7.

7. Running the PnP-Github.ps1 script requires the following command line parameters:

    pat  
    csv  
    uri  
    name  

    Usage example: PnP-Github.ps1 -pat PAT_FROM_GITHUB -csv ./waf_review.csv -uri https://dev.github.com/demo-org/demo-repo -name WAF-Assessment-x


8. Run the PowerShell script and wait for the execution to complete.

9. Seeing some exceptions while running the script is expected. Please validate GitHub - As long as milestones and Issues are populated, you should be good to proceed.

10. After running the script, navigate to Issues in the GitHub repository that was created. You can also visualize the issues categorized as milestones or through labels in this view.

11. Now you can go into Projects and create a new project. Give your project an appropriate name and select the Basic Kanban project template.

12. Based on your prioritization conversation with the customer, you can show the customer how they can move their open issues from the WAF Assessment into one of the to-do, in-progress or done states by creating projects in GitHub.
