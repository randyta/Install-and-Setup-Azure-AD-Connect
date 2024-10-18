Getting started with Azure AD Connect using express settings
The following documentation will help you get started with Azure Active Directory Connect. This documentation deals with using the express installation for Azure AD Connect.

Related documentation
If you did not read the documentation on Integrating your on-premises identities with Azure Active Directory, the following table provides links to related topics. The first two topics in bold are required before you start the installation.

Topic	
Download Azure AD Connect	Download Azure AD Connect
Hardware and prerequisites	Azure AD Connect: Hardware and prerequisites
Install using customized settings	Custom installation of Azure AD Connect
Upgrade from DirSync	Upgrade from Azure AD sync tool (DirSync)
After installation	Verify the installation and assign licenses
Accounts used for installation	More about Azure AD Connect accounts and permissions
Express installation of Azure AD Connect
Selecting Express Settings is the default option and is one of the most common scenarios. When doing this, Azure AD Connect deploys sync with the password sync option. This is for a single forest only and allows your users to use their on-premises password to sign-in to the cloud. Using the Express Settings will automatically kick off a synchronization once the installation is complete (though you can choose not to do this). With this option there are only a few short clicks to extending your on-premises directory to the cloud.

Welcome to Azure AD Connect

To install Azure AD Connect using express settings
Login to the server you wish to install Azure AD Connect on a local Administrator. This should be the server you wish to be the sync server.
Navigate to and double-click on AzureADConnect.msi
On the Welcome screen, select the box agreeing to the licensing terms and click Continue.
On the Express settings screen, click Use express settings. Welcome to Azure AD Connect
On the Connect to Azure AD screen, enter the username and password of an Azure global administrator for your Azure AD. Click Next.
On the Connect to AD DS screen enter the username and password for an enterprise admin account. Click Next. Welcome to Azure AD Connect
On the Ready to configure screen, click Install.
Optionally on the Ready to Configure page, you can un-check the “Start the synchronization process as soon as configuration completes” checkbox. If you do this, the wizard will configure sync but will leave the task disabled so it will not run until you enable it manually in the Task Scheduler. Once the task is enabled, synchronization will run every three hours.
Also optionally you can choose to configure sync services for Exchange Hybrid deployment by checking the corresponding checkbox. If you don’t plan to have Exchange mailboxes both in the cloud and on premises, you do not need this. Welcome to Azure AD Connect
Once the installation completes, click Exit.
After the installation has completed, Logoff and Login again before you use Synchronization Service Manager or Synchronization Rule Editor.
