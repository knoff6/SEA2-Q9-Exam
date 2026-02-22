# SEA2 Q9 — Troubleshooting Exam Topology (Final)

Two-router network (R1–R2) with VPCS endpoints (PC1, PC2) and Ethernet switches. Topology has ONE intentional misconfiguration — PC1 cannot ping PC2. Students must identify and fix the error using show commands. Default routing is used. Do NOT modify this project before the exam. Start all devices and wait 60 seconds for routers to boot before attempting. Uses Cisco 1700 router appliance.

## Troubleshooting Import Issues
### ❌ "Cannot connect to compute 'Remote' with request POST /projects"
This commonly occurs when importing on GNS3 v3 (Windows). The GNS3 client is trying to reach a Remote compute (GNS3 VM) that isn't running or reachable.
Fix:  

Open GNS3 (without importing anything)  
Go to Edit → Preferences → Controller → Remote Computes  
Disable or remove the Remote compute entry  
Wait for the green light in the bottom-left corner (server connected)  
Try importing again  
  
### ❌ "The image 'c1700-adventerprisek9-mz.124-25d.image' is missing"  
The target machine doesn't have the Cisco c1700 IOS image that was used to build the topology.  
Fix:  
  
This project uses the Cisco c1700 image (`c1700-adventerprisek9-mz.124-25d.image`). Download it from [here](https://github.com/hegdepavankumar/Cisco-Images-for-GNS3-and-EVE-NG).


Install the image in GNS3: Edit → Preferences → Dynamips → IOS Routers → New → browse to the image → complete the wizard
Try importing the project again  


Tip: Ensure all lab machines have the same IOS image installed before exam day.
