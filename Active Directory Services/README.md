# Active Directory Services

## Objective
- Create Organizational Units(OU's) and users
- Create a Domain Admin
- Create a Windows 11 client 
- Add the client to the domain
  
## Table of Contents
- [Step 1: Set Up Static IP Address and DNS on the Domain Controller](#step-1-set-up-static-ip-address-and-dns-on-the-domain-controller)
- [Step 2: Create OU's and Groups](#step-2-create-ous-and-groups)
- [Step 3: Create a Domain Admin](#step-3-create-a-domain-admin)
- [Step 4: Add Windows 11 Client to Domain](#step-4-add-windows-11-client-to-domain)

## Step 1: Set Up Static IP Address and DNS on the Domain Controller
- Once you've logged into your server go to the command prompt and enter "ipconfig". Here you'll see the IP address assigned to the server once it was created. This is the address that we will assign as the static IP address for the server.
<img width="666" height="447" alt="AD2" src="https://github.com/user-attachments/assets/604aa124-c8fa-4651-b5c1-e7723124e0e0" />

- Now from the settings menu, go to "Network & Internet" then "Ethernet. You can see here that the "IP assignment" is set to Automatic (DHCP).
<img width="1020" height="792" alt="AD3" src="https://github.com/user-attachments/assets/2ebf1d6f-33bf-4236-9920-6875efe2b180" />

- Click edit and fill in the IP address, subnet mask, and default gateway addresses we got from our ipconfig output earlier. Double check and make sure everything is correct.
<img width="1014" height="785" alt="AD4" src="https://github.com/user-attachments/assets/6a76c165-35de-43e4-afe3-219e1f822386" />

## Step 2: Create OU's and Groups
- Open up Active Directory Users and Computers. Here we'll be able to see our domain "MyHomeLab.local" on the lefthand side.
<img width="750" height="524" alt="A1" src="https://github.com/user-attachments/assets/1e25aa49-b603-4bb3-8ac7-19d5bd871069" />

- Now we will create Organizational Units otherwise known as OU's. We'll start by right clicking out domain, selecting New, then selecting Organizational Unit.
<img width="751" height="516" alt="A3" src="https://github.com/user-attachments/assets/fc798380-6283-4cce-8788-0bccce22bdca" />

- Now we can name our OU. I'll make a "USA office" for this example.
<img width="430" height="374" alt="A4" src="https://github.com/user-attachments/assets/66175ec0-3748-4559-a160-62d28e3fde2d" />

- Next we'll make a few more OU's inside "USA". These will represent different departments and computers.
<img width="747" height="521" alt="A6" src="https://github.com/user-attachments/assets/8c879ede-42e0-471a-9cd4-a7cacd5f8702" />

## Step 3: Create a Domain Admin
- We'll start by right clicking our department (in this case it will be IT), selecting new, then selecting user.
- The reason for making a Domain Admin is that they have the power to add new users to our domain.
<img width="456" height="316" alt="A7" src="https://github.com/user-attachments/assets/54e18b0e-4446-4426-9bc4-29717e0249e1" />

- Fill in the users information as well as their account/logon name.
<img width="432" height="374" alt="A8" src="https://github.com/user-attachments/assets/07acafb6-66ca-43e4-87fb-541ca5c36a7a" />

- Create a password for the user. We'll set this password to never expire.
<img width="432" height="369" alt="A9" src="https://github.com/user-attachments/assets/4e521122-fc70-4703-acf4-36c2220f71b4" />

- You can now see that a new user was created in the IT department.
<img width="748" height="520" alt="A10" src="https://github.com/user-attachments/assets/7efe395d-98ea-4ca7-8f37-2ad92d763267" />

- From here we'll right click the the user and go to "Properties". Inside "Properties" select the "Member Of" tab and click "Add".
<img width="406" height="523" alt="A12" src="https://github.com/user-attachments/assets/24f048ef-3674-47bd-b2d9-9ce8effb849f" />

- In the "Enter the object names..." box, type in "Domain Admins" and click "Check Names". This should underline "Domain Admins" signaling that we've found the correct group name. Now click ok.
<img width="454" height="244" alt="A13" src="https://github.com/user-attachments/assets/54c0ea06-bbf6-4efb-be07-75e14e5eaea0" />

- We can now confirm that the user has been added to the Domain Admins group. Click "Apply" followed by "Ok".
<img width="406" height="529" alt="A14" src="https://github.com/user-attachments/assets/6619c4e8-2105-4361-8d2b-8a0f55c57dc7" />

- Lastly we'll follow the same steps as above and create a new user in the HR department that we'll use as our Windows 11 client.

<img width="750" height="518" alt="A15" src="https://github.com/user-attachments/assets/8fd0b390-86bd-46bc-9d38-ed7c313a9a61" />

## Step 4: Add Windows 11 Client to Domain

- Login to your client computer using the admin account we created. Go to Settings > Network & Internet > Ethernet. Scroll down to "DNS server assignment" and click edit.

<img width="784" height="616" alt="C1 copy" src="https://github.com/user-attachments/assets/bda6a727-e9e5-4050-884f-72900c9282b1" />

- Now select "Manual"
<img width="495" height="213" alt="C2" src="https://github.com/user-attachments/assets/33eb83cf-1562-46d7-9029-7cd539506c23" />

- Toggle on IPv4 and under "Preferred DNS" we are going to put in the IP address of our windows server.
<img width="493" height="681" alt="C4" src="https://github.com/user-attachments/assets/78df0e65-4c6d-45b8-9fb9-77fd8c6e5606" />

- To verify that things are working correctly we can ping our windows server from the commandpromt.
<img width="567" height="405" alt="C5" src="https://github.com/user-attachments/assets/e7dfb337-3636-4749-9d2d-6c81d4ff2e3c" />

- Next go to file explorer and right click on this PC. Select properties. Scroll down until you see "Domain or workgroup" and click on that.
<img width="1021" height="787" alt="Screenshot 2026-04-09 103148" src="https://github.com/user-attachments/assets/614e79e9-0426-4bf3-9da4-575d0ed6ff08" />

- From here go to the "Computer Name" tab and click on the change button.
<img width="412" height="463" alt="Screenshot 2026-04-09 105957" src="https://github.com/user-attachments/assets/ee9a4069-d89b-41ed-8548-253be8801c77" />

- Select "Domain" under the "Memeber Of" section and fill in the domain name of our server, "MyHomeLab.local".
<img width="321" height="386" alt="Screenshot 2026-04-09 110500" src="https://github.com/user-attachments/assets/15f5dff7-4c60-4cf2-b04c-081c15689b1a" />

- Now this PC is a memeber of the domain.
<img width="305" height="145" alt="C11" src="https://github.com/user-attachments/assets/ac0c9e52-af5a-4b4c-9d27-5c34ce6ffa29" />

- To verify everything is working correctly we'll log in under the user account Jane Doe that we created earlier.
<img width="529" height="579" alt="C12" src="https://github.com/user-attachments/assets/03e71368-618f-44be-a3bc-916f509b4188" />

<img width="633" height="188" alt="C13" src="https://github.com/user-attachments/assets/31577bc1-2f9a-4930-92cf-c565d6a970df" />


- Lastly we will do a little house keeping and move our client PC to its appropriate group in Active Directory. To do this, open Active Directory select the default "Computers" group then right click on our "HomeLabPC" and select the move option.
<img width="747" height="519" alt="C15" src="https://github.com/user-attachments/assets/bc59831c-2676-44d2-b8a6-bbfd9475a11a" />

- From the "Move" screen select the "Computers" under our "USA" group and click ok.
<img width="316" height="326" alt="C16" src="https://github.com/user-attachments/assets/e4ece07e-d862-4b8f-9950-404904e0d403" />

- Now our "HomeLabPC" was moved into its correct place.
<img width="459" height="523" alt="C18" src="https://github.com/user-attachments/assets/a0fc1513-25dc-4c2f-8dd4-7705aa4ba22a" />

- We can also add a description to our computer so it's easy to tell which user it belongs to by right clicking our computer, selecting properties, and filling out the description under the "General" tab.
<img width="459" height="523" alt="C18" src="https://github.com/user-attachments/assets/be0d8040-77fd-4353-aec9-1b7845d471c4" />



