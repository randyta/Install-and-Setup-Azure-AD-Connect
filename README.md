<properties
	pageTitle="Azure AD Connect: Getting Started using express settings | Microsoft Azure"
	description="Learn how to download, install and run the setup wizard for Azure AD Connect."
	services="active-directory"
	documentationCenter=""
	authors="billmath"
	manager="stevenpo"
	editor="curtand"/>

<tags
	ms.service="active-directory"
	ms.workload="identity"
	ms.tgt_pltfrm="na"
	ms.devlang="na"
	ms.topic="article"
	ms.date="10/13/2015"
	ms.author="billmath;andkjell"/>

# Getting started with Azure AD Connect using express settings
The following documentation will help you get started with Azure Active Directory Connect. This documentation deals with using the express installation for Azure AD Connect.  

## Related documentation
If you did not read the documentation on [Integrating your on-premises identities with Azure Active Directory](active-directory-aadconnect.md), the following table provides links to related topics. The first two topics in bold are required before you start the installation.

| Topic |  |
| --------- | --------- |
| **Download Azure AD Connect** | [Download Azure AD Connect](http://go.microsoft.com/fwlink/?LinkId=615771) |
| **Hardware and prerequisites** | [Azure AD Connect: Hardware and prerequisites](active-directory-aadconnect-prerequisites.md) |
| Install using customized settings | [Custom installation of Azure AD Connect](active-directory-aadconnect-get-started-custom.md) |
| Upgrade from DirSync | [Upgrade from Azure AD sync tool (DirSync)](active-directory-aadconnect-dirsync-upgrade-get-started.md) |
| After installation | [Verify the installation and assign licenses ](active-directory-aadconnect-whats-next.md) |
| Accounts used for installation | [More about Azure AD Connect accounts and permissions](active-directory-aadconnect-accounts-permissions.md) |


## Express installation of Azure AD Connect
Selecting Express Settings is the default option and is one of the most common scenarios. When doing this, Azure AD Connect deploys sync with the password sync option. This is for a single forest only and allows your users to use their on-premises password to sign-in to the cloud. Using the Express Settings will automatically kick off a synchronization once the installation is complete (though you can choose not to do this). With this option there are only a few short clicks to extending your on-premises directory to the cloud.

![welcome](https://github.com/user-attachments/assets/a6424a06-c4c2-48ad-a7d8-0415161ecd71)
)
)

### To install Azure AD Connect using express settings

1. Login to the server you wish to install Azure AD Connect on a local Administrator.  This should be the server you wish to be the sync server.
2. Navigate to and double-click on AzureADConnect.msi
3. On the Welcome screen, select the box agreeing to the licensing terms and click **Continue**.
4. On the Express settings screen, click **Use express settings**.
(![express](https://github.com/user-attachments/assets/c74ae65b-f5b3-4a7f-b309-3383ae733666)
)
5. On the Connect to Azure AD screen, enter the username and password of an Azure global administrator for your Azure AD. Click **Next**.
6. On the Connect to AD DS screen enter the username and password for an enterprise admin account.  Click **Next**.
(![install4](https://github.com/user-attachments/assets/2311fe33-2240-45b5-ab9f-d43444214d3b)
)
7. On the Ready to configure screen, click **Install**.
	- Optionally on the Ready to Configure page, you can un-check the “**Start the synchronization process as soon as configuration completes**” checkbox.  If you do this, the wizard will configure sync but will leave the task disabled so it will not run until you enable it manually in the Task Scheduler.  Once the task is enabled, synchronization will run every three hours.
	- Also optionally you can choose to configure sync services for **Exchange Hybrid deployment** by checking the corresponding checkbox.  If you don’t plan to have Exchange mailboxes both in the cloud and on premises, you do not need this.
( <img width="300" alt="readyinstall" src="https://github.com/user-attachments/assets/343d1978-a471-48b2-9ae2-8cfd50800aed">
)<br>
8. Once the installation completes, click **Exit**.
9. After the installation has completed, Logoff and Login again before you use Synchronization Service Manager or Synchronization Rule Editor.

<br>
<br>

