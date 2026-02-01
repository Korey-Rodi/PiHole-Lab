# PiHole-Lab

<img width="800" height="800" alt="image" src="https://github.com/user-attachments/assets/35e379e6-ec07-4ccd-a9cd-49728e3f11cc" />

## What is PiHole?
PiHole is network wide ad and domain blocker. The service typically runs on the a rasberry Pi but in this case it was ran of an ubuntu virtual machine.

# Set up

## Step 1 (Download and install)
* download a linux distro of your choice (I recomend Ubuntu Desktop for its ease of use).
* Create a new VM using the ISO file from your distro of choice and make sure the VM is configured in bridged mode
such that your router is able to assign an ip address on your hosts computers network. Now continue with distro installation.
* Use command "ip a" and take note of the virtual machine ip address and its Mac address.

## Step 2 (Setup and configure)
* Log into your router (This can be found usually by visiting 192.168.1.1 in your browser of choice and logging in from there).
* Continue to the settings of your router titled something such as static connections. Rememeber your ip address and mac address from earlier and add them with a designated name
then press apply.

## Step 3 (Download PiHole)
* Open terminal and paste in the command
"wget -O basic-install.sh https://install.pi-hole.net
sudo bash basic-install.sh"
* Proceed with setup wizard
* after installation and setup is done use command "sudo pihole setpassword" and leave the field blank --> This isnt the best practice but in a temporary set up it is okay

## Step 4 (Visit PiHole)
* Confirm that pihole is runnung using the command "pihole status"
* Log into pihole by typing in the ip address of the pihole VM either on the host machine or the VM to visit the admin dashboard

## Step 5 (Configure)
* Use an ad blocking list either default or set up personal
* Add domains to list that you wish to not be accessible on your home network
* For a network wide configuration log back into your router and set the DNS to point to the ip address of your pihole (In this use case I do not recomend this as the uptime of your laptop or desktop is not consistent, only do this is you have a dedicated device) Otherwise on the device you wish to utilize the pihole with, visit the settings on your device and click on the details for your home network you can then set the DNS for your device to point to the pihole ip
* Create groups and limit certain clients to safe browsing
* Check the dashboard to see total number of queries and blocked ones



# Resources
https://docs.pi-hole.net/main/basic-install/
https://ubuntu.com/download/desktop
https://www.virtualbox.org/


# Pictures
## Create account
<img width="1822" height="1289" alt="image" src="https://github.com/user-attachments/assets/fdaa37f9-cea2-4723-a012-056a4fb5becf" />

## Set Static IP
<img width="1265" height="530" alt="Screenshot 2026-01-31 at 11 02 43 PM" src="https://github.com/user-attachments/assets/8293b795-2664-4f4c-8e28-97d69dd4cd04" />

## View admin Dashboard
<img width="1511" height="822" alt="Screenshot 2026-01-31 at 11 28 35 PM" src="https://github.com/user-attachments/assets/095f9f4f-d6d4-4875-bc2e-fc7e09635289" />

## Setup block list and groups
<img width="1244" height="761" alt="Screenshot 2026-01-31 at 11 24 47 PM" src="https://github.com/user-attachments/assets/68a0914d-1d07-47d5-b656-6a83f8ad8bca" />

## Set as DNS for device or network
<img width="651" height="409" alt="Screenshot 2026-01-31 at 11 21 49 PM" src="https://github.com/user-attachments/assets/2b1b9864-458f-4f82-b00b-9983f26c4e68" />



