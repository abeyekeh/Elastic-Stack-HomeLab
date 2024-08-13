# Elastic SIEM HomeLab
In this lab i created an Elastic Stack SIEM using Virtual Box, Kali Linux VM and Elastic Web portal. I configured Elestic agents on  Kali VM to generate security events, transport date in the SIEM, and query to find any malicious activities. Utilizing Kibana i previsioned an visual dashboard to monitor security threats.

# Step 1: Set up Virtual Environment
- I used Virtualbox to create an isolated     environment
- Download Kali Linux VM and install on Virtualbox
- Power on kali vm and open terminal 

# Step 2: Set up Elastic Cloud account
- Click Log into Elastic Cloud console or create an free account
- Select Create a Deployment

# Step 3: Configured Elestic Agents on you host
- Click Added an intergration
- Select or search for "Elastic Defend"
- Install Elastic Defend
- select the platform and paste the clipboard into the kali terminal
- Successfully install Elastic Agent
- Confirmed Agent enrollment

# Step 4: Start Generating Security Events
- Scane and identify services running the ports using nmap
- Scan all ports (nmap -p- target)
- Ran aggressive scan ("nmap -A target)
- Conduct UDP Scan (nmap -sU target)

# Step 5: Querying and Analyzing Security Events 
- Click Observability than click logs
- Use the search bar to query "nmap scans"
- Exacuted Event action and Process args (process.args_count)
- Investigated malicious events

# Step 6: Create Visual Dashboard to Monitor Events
- Click Analytic than Dashboard in Elastic
- Select "Create dashboard" than click "create Visualization"
- First dashboard created using Bar Vertical Stacked-horizontal-timestamp and verticle use count

# Step 7: Create Alerts
- Click Security from the menu and select Security than Alerts
- Created an Alert to monitor logs from nmap scan to notify when is detected.
- click create new rule, select custom query
created an "event.action: "nmap_scan"
- Selected email as a connector

# Conclusion
I set up an Home Cybersecurity lap using Elastic SIEM and Kali Linux. Generated Events logs on kali as an endpoint using nmap and Transported date from kali to Elistic SIEM using Eestic Agents. Created Alerts to detect specific events, Queried, analyzed events.