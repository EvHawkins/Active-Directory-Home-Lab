# Active Directory Services

## Objective
- Create a windows client
- Join the client to the domain
- Create Organizational Units(OU's) and users

## Table of Contents
- [Step 1: Set Up Static IP Address and DNS on the Domain Controller](#step-1-set-up-static-ip-address-and-dns-on-the-domain-controller)
- [Step 2: Create OU's and Groups](#step-2-create-ous-and-groups)



## Step 1: Set Up Static IP Address and DNS on the Domain Controller
- Once you've logged into your server go to the command prompt and enter "ipconfig". Here you'll see the IP address assigned to the server once it was created. This is the address that we will assign as the static IP address for the server.
<img width="666" height="447" alt="AD2" src="https://github.com/user-attachments/assets/604aa124-c8fa-4651-b5c1-e7723124e0e0" />

- Now from the settings menu, go to "Network & Internet" then "Ethernet. You can see here that the "IP assignment" is set to Automatic (DHCP).
<img width="1020" height="792" alt="AD3" src="https://github.com/user-attachments/assets/2ebf1d6f-33bf-4236-9920-6875efe2b180" />

- Click edit and fill in the IP address, subnet mask, and default gateway addresses we got from our ipconfig output earlier. Double check and make sure everything is correct.
<img width="1014" height="785" alt="AD4" src="https://github.com/user-attachments/assets/6a76c165-35de-43e4-afe3-219e1f822386" />

## Step 2: Create OU's and Groups
