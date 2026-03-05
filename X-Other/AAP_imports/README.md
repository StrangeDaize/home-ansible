Hosts.yml
    Include these hosts in the import


How to use these files:
Go to Inventories 
    Choose Add Inventory
        Name: The Collection hosts Name
        Description: Your Description
        Organization: Organization that can use it
        Instance Groups: Where can this execute

After saving the Inventory, 
    Go into the Inventory you created:
        Go to Sources:
             Click Add:
                Name: Name of the source (i.e. GitHub Inventory List)
                Description: Your description
                Execution Environment: What execution environment to run the jobs from
                Source: Choose Sourced from Project
                    For Source Details:
                        Credential: <LEAVE BLANK>
                        Project: <Your Git Repo of choice>
                        Inventory file: <Inventory.ini in Your Git Repo of choice>
                        Update options (optional):
                            Overwrite
                            Overwrite variables 
                            Update on launch 
                            Update on project update
                Click Save

Now run Sync if it doesn't automatically start
Confirm hosts by selecting Hosts from the Inventory header


