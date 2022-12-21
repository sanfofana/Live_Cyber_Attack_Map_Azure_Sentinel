# Live_Cyber_Attack_Map_Azure_Sentinel

<img src="https://github.com/sanfofana/Live_Cyber_Attack_Map_Azure_Sentinel/blob/main/Azure_Sentinel_Map.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />


## Step by Step procedures:

1. Create a Windows virtual machines from Azure portal.


2. Access the Virtual machine using Remote desktop client.

    - Set up the edge in the VM as it will be needed later on in the project.
    - On the honeypot VM make sure that ICMP is enabled to allow ping.
        - Go to the firewall and dmake sure it is disabled is the easy way. 
            - You can also make do this in the firewall advance setting.
            
3. Download the the script file and run it on your honeypot VM.
        - Note: The role of this script is to automatically take failled login attempts from windows EVENT VIEWER.
        - Run the script.
        
4. Create a custom inside Azure log Analytic workspace.
        - Note: This custom log will import a custom log with GO data inside.
        - Go the honeypot VM, in PROGRAMDATA directory to access failed logs
        - export the failed logs in the custom log analytics.
        - After export, it may take few minutes for the log analytics to sync with HoneypotVM and create logs.
      
      
5. Setting MAP in Sentinel.
        - In Azure Access Sentinel
        - On the left panel, click on workbook,and add new.
        - Add a query in the new workbook
        - Click on visualization and select MAP.
        - Select your custom field with the coordonnate sets.

<img src="https://github.com/sanfofana/Live_Cyber_Attack_Map_Azure_Sentinel/blob/main/Azure%20Sentinel%20Siem.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>










