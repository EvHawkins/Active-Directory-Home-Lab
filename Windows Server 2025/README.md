# Windows Server 2025 Setup

## Objectives

Begin the intial setup of Windowns Server 2025, rename the server, enable remote management, and install active directory

## Table of Contents
- [Step 1: Rename Server](#step-1-rename-server)
- [Step 2: Enable Remote Management](#step-2-enable-remote-management)
- [Step 3: Install Active Directory](#step-3-install-active-directory)

## Step 1: Rename Server

Windows typically assigns the computer a long and complicated device name. This can be hard to remember when trying to find the server so it's best to create a new simple and appropriate name for the server.

- Start by opening file explorer and right clicking on "This PC" and then select properties

<img width="1120" height="585" alt="Rename 1" src="https://github.com/user-attachments/assets/0f62c604-24a7-4a7b-8532-d5200bfadcee" />


- On the next screen click on "Advanced system settings"

<img width="1013" height="490" alt="Rename 2" src="https://github.com/user-attachments/assets/01bf7f8c-e351-4999-b793-e4b8ad51485e" />

- At the topleft side of the screen find the  "Computer Name" tab and click on it

- Click "Change" Next to where it says "To rename this computer its domain or workgroup"

<img width="399" height="459" alt="Rename 4" src="https://github.com/user-attachments/assets/3ba67445-0a12-412b-b15f-3df54b1fdd56" />

- Now rename server something that's easy to find and remember

<img width="401" height="462" alt="Rename 5" src="https://github.com/user-attachments/assets/84777f75-f208-413f-9e7a-24e01fcd54f6" />

- You can verify the new server name by going to the command prompt and inputting "hostname"

<img width="679" height="361" alt="Rename 6" src="https://github.com/user-attachments/assets/42abea66-edc1-41b7-a2f1-659f56aa30a1" />

## Step 2: Enable Remote Management
- Open up Server Manager and click "Local Server"
- From here make sure remote management is enabled

<img width="808" height="458" alt="AD Setup 3 copy" src="https://github.com/user-attachments/assets/5699303e-ebcd-434b-96ce-d4bc93ea7125" />

<img width="642" height="328" alt="AD Setup 2" src="https://github.com/user-attachments/assets/2f6f6c3a-b91e-4620-8696-8a0a84b8e3fa" />

## Step 3: Install Active Directory

- Open Server Manager and at the top right of the screen click on "Manage" followed by "Add Roles and Features"
<img width="1422" height="800" alt="AD Setup 3" src="https://github.com/user-attachments/assets/b98c830f-c949-457c-8704-6da585f8d056" />

- Review the information and make sure all steps have been completed, then click "Next"
<img width="780" height="553" alt="AD Setup 4" src="https://github.com/user-attachments/assets/8d68ae4a-d7ab-4002-88cc-70d86bd3c5ba" />

- Under Roles find "Active Directory Domain Services", select it, and the click "Add Features"
<img width="764" height="431" alt="AD Setup 6" src="https://github.com/user-attachments/assets/41b9abdd-1ad0-4edf-a83f-3093c19971c6" />

- Now the intsallation process will begin but it's very important not to close the window after the install is done
<img width="781" height="555" alt="AD Setup 7" src="https://github.com/user-attachments/assets/e409037a-11b9-4e65-91c0-53baf69463bf" />

- Once the installation is done we will promote the serve into a domain controller. This is why it is important not to close the installation wizard after the install.
<img width="592" height="362" alt="AD Setup 8" src="https://github.com/user-attachments/assets/2c8ef466-ea5e-4a9f-887c-1809ccc84cdb" />

- Click on "Add a new forest" and select a domin name for your server
<img width="755" height="559" alt="Ad setup 9" src="https://github.com/user-attachments/assets/2ab6ca11-f154-4045-8737-f0650ba92628" />

- Make sure all the information is correct and put in your password
 <img width="755" height="557" alt="AD setup 10" src="https://github.com/user-attachments/assets/bf432245-08db-41a2-a5e5-1e268cdbeac1" />

- Click through DNS options, Additional Options, and Review options. Nothing here needs to be changed, just make sure everything is correct. You will now find yourself at the prerequisite check menu. You may have to press "Previous" a few times while the check is being done. Once you see a green check mark, you're ready to click "Install"
<img width="757" height="554" alt="AD setup 15" src="https://github.com/user-attachments/assets/f48fcaec-f019-4646-ad6f-a1aeeca8a086" />

- Your system will reboot and at the login screen you can now see your domain name at login
<img width="613" height="509" alt="AD1 copy" src="https://github.com/user-attachments/assets/4ec68a8c-bda9-408e-9ab9-bc775d4efd92" />

- After you login go to Control Panel > System and Security > Windows Tools and make sure everything was installed correctly 
<img width="1118" height="584" alt="AD setup 16" src="https://github.com/user-attachments/assets/d942f5fd-32ee-483c-9716-25a7028cc514" />




 






  







