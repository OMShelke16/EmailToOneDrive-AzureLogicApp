# Email-to-OneDrive Automation using Azure Logic Apps

## Project Overview

This project demonstrates a cloud-based automation solution using **Azure Logic Apps**. The workflow automatically monitors an Outlook inbox and saves incoming emails as text files in Microsoft OneDrive without requiring any coding.

The solution leverages Azure's serverless workflow engine and built-in connectors to automate email backup and storage operations.

---

## Problem Statement

Manually saving important emails for backup or record-keeping is time-consuming and error-prone. Organizations and individuals often require an automated method to archive email content for future reference.

---

## Objective

* Automate email backup using cloud services.
* Detect incoming emails automatically.
* Extract email subject and body content.
* Store email information as text files in OneDrive.
* Demonstrate a no-code cloud automation workflow.

---

## Technologies Used

### Microsoft Azure

* Azure Logic Apps (Consumption Plan)
* Azure Resource Group

### Microsoft Services

* Office 365 Outlook Connector
* Microsoft OneDrive Connector

### Monitoring

* Logic App Run History

---

## Architecture

### Resource Group

| Property       | Value               |
| -------------- | ------------------- |
| Resource Group | LogicAppRG          |
| Logic App Name | EmailToOneDrive-App |
| Region         | Central India       |
| Plan Type      | Consumption         |

---

## Workflow

1. User sends an email to Outlook.
2. Outlook receives the email.
3. Azure Logic App is triggered automatically.
4. Logic App extracts:

   * Email Subject
   * Email Body
5. Logic App invokes OneDrive Connector.
6. A text file is created in OneDrive.
7. Email content is stored in the file.
8. Workflow execution is logged in Run History.

---

## Project Flow

Email Received in Outlook

↓

Azure Logic App Triggered

↓

Extract Subject & Body

↓

Create .txt File

↓

Save to OneDrive

↓

Workflow Completed Successfully

---

## Folder Structure

```text
EmailToOneDrive-AzureLogicApp
│
├── README.md
├── Screenshots
│   ├── Azure-Portal.png
│   ├── ResourceGroup.png
│   ├── LogicApp-Overview.png
│   ├── Workflow-Designer.png
│   ├── Outlook-Trigger.png
│   ├── OneDrive-Action.png
│   ├── RunHistory-Success.png
│   ├── Test-Email.png
│   ├── OneDrive-Folder.png
│   └── Output-File.png
│
├── Diagrams
│   ├── Architecture-Diagram.png
│   ├── Workflow-Diagram.png
│   ├── Sequence-Diagram.png
│   ├── DFD-Diagram.png
│   └── Azure-Service-Interaction.png
│
└── Documentation
    └── Project-Report.pdf
```

---

## Logic App Configuration

### Trigger

**When a new email arrives (V3)**

Configuration:

* Folder: Inbox
* Importance: Any
* Include Attachments: No

### Action

**Create File (OneDrive)**

Configuration:

* Folder Path: `/Documents/EmailBackups`
* File Name: `Email Subject.txt`
* File Content: Email Body

---

## Sample Execution

### Input Email

Subject:

```
TestLogicApp
```

Body:

```
Hello Logic App Test
```

### Generated File

File Name:

```
TestLogicApp.txt
```

Stored Location:

```
OneDrive/Documents/EmailBackups
```

File Content:

```
Hello Logic App Test
```

---

## Results

* Successfully detected incoming Outlook emails.
* Automatically triggered Azure Logic App workflow.
* Created text files in OneDrive.
* Stored email content without manual intervention.
* Verified successful execution through Run History.

---

## Benefits

* No coding required.
* Serverless cloud architecture.
* Automated email backup.
* Easy integration with Microsoft services.
* Scalable and cost-effective solution.

---

## Future Enhancements

* Store email attachments.
* Save emails to SharePoint.
* Generate PDF backups.
* Send notification emails after backup.
* Integrate with Microsoft Teams.
* Archive emails to Azure Blob Storage.

---

## Conclusion

This project successfully demonstrates how Azure Logic Apps can be used to automate business processes using built-in connectors. The solution automatically backs up Outlook emails to OneDrive, reducing manual effort and improving productivity through cloud automation.

---

## Author

**Om Devdatt Shelke**

Cloud Computing Project

Azure Logic Apps – Email-to-OneDrive Automation
