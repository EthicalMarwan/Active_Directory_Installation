# Active Directory Installation On A Windows Server

## Ojective
- Setting up an Active Directory domain controller using Windows Server 2022 on Oracle Virtualbox, creating a functional home lab environment for testing and learning enterprise-level directory services.

## Steps
### 1. Prepare the environment
   - Your host system should have Oracle VirtualBox (or any Virtual Machine).
   - Create a fresh virtual machine (VM) for Windows Server
   - Verify the VM satisfies systems requirements (minimum of 2GB of RAM, 1 CPU core, and 40GB of Disk space allocation).
<div>
    <img src="https://github.com/user-attachments/assets/52b21a68-1c8b-4018-b07f-7ce32a623977" />
</div>
<div>
    <img src="https://github.com/user-attachments/assets/6f676a71-a399-4462-8e20-51d64a553550" />
</div>

### 2. Install Windows Server 2022
   - Download the ISO from Microsoft's website, Deploy the ISO and proceed through the Windows Installation GUI.
   - Choose desktop experience unless you'd rather have the server core (Based on preference).
   - Set up administrative credentials and initial configuration.
<div>
    <img src="https://github.com/user-attachments/assets/855de12d-f9bd-4e0e-b305-09f5b01db46c" />
</div>

### 3. Configure networking
   - Assign a static IP address to the server.
   - Set proper DNS settings (can point to itself post-AD install).
<div>
    <img src="https://github.com/user-attachments/assets/698fc586-8943-4e27-8b84-5632df7a01c2" />
</div>

### 4. Include AD DS (Active Directory Domain Services).
   - Launch Server Manager → Add Features and Roles.
   - Select “Active Directory Domain Services.”
   - Follow prompts; install required features and then promote the server.
<div>
    <img src="https://github.com/user-attachments/assets/bd7ed816-8d10-4e45-b94a-906d8473d74f" />
</div>

### 5. Promote to Domain Controller
   - Use the AD DS Configuration Wizard.
   - Make a new domain and forest (EthicalMarwan.local for this example).
   - Set a password for the Directory Services Restore Mode (DSRM).
   - Complete the wizard and reboot.
<div>
    <img src="https://github.com/user-attachments/assets/a5fa0534-b3ce-4c4f-a8be-ff256bcc32bd" />
</div>
<div>
    <img src="https://github.com/user-attachments/assets/423d6a68-046e-4863-82f5-aceabf72b0ef" />
</div>
<div>
    <img src="https://github.com/user-attachments/assets/441776a8-56a8-4e21-b71f-6557058f4bf4" />
</div>

### 6. Verify AD installation
   - Make use of the DNS Manager and Active Directory Users and Computers management tools.
   - Check that AD domain is functioning and DNS is correctly configured.
   - Test by creating organizational units (OUs) and user accounts (as shown in this example).
<div>
    <img src="https://github.com/user-attachments/assets/7a22f1ac-72de-4792-889e-58813d010e12" />
</div>
<div>
    <img src="https://github.com/user-attachments/assets/df1bfe0c-e20d-4b84-8bf3-dc6773222af3" />
</div>

## Summary
- You’ll end up with a Windows Server 2022 VM operating as a Domain Controller in a new AD forest (EthicalMarwan.local for this example). You’ll learn to install server roles, configure DNS and static IP, and manage AD infrastructure, creating a sandbox environment perfect for experimenting with group policies, user management, and network security.


## Skills Learned
- Installing and configuring Windows Server 2022 on a Virtual Machine
- Setting up static IP and DNS for server reliability
- Installing and configuring AD DS roles
- Promoting a server to a domain controller and creating an AD forest
- Using AD management tools (Active Directory Users & Computers, DNS Manager)
- Basic AD tasks: OU/user creation, domain functionality verification
