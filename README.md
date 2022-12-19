# Active-Directory-Basics-Deep-Dive
Futher understanding Windows Active Directory for work/knowledge skillsets 

<h2>Prerequisites </h2> 
<p align="left">
- Microsoft Azure - One resource group running two diffrent VMs. One VM will be a Windows Server. The other VM will be a Windows user on that server.<br/>
- Remote Desktop Protocol will need to be open on these VMs.<br/>
- Windows Remote Desktop Connection App will be needed to virtually use this computers.<br/>

<h2>Topics</h2>
<p align="left">
- I will be briefly explaining my understanding of Active Directory, DHCP, DNS<br/>

<h2> Active Directory</h2><br/>
<p align="left">
What is an Active Directory? What can it be used for? <br/>
  - An Active Directory is an essential tool/service made by microsoft that includes a ton of services, tools, and resources to admin or connect users within a network. Active Directory is a great tool/service for coprerations to promote efficientcy within their network. <br/>

1.)Install Windows Adminastrative tools to remotely control the AD from user machine

What is a Domain?<br/>
- A domain is the host server. A domain is similar to how somebody hosts a party. the domain would be the party host with all the control to remove or invite people ect. and the guests would be simialr to the users. Alternativly can be though of like a Country.<br/>
What is an Orginaztional Unit?
-Basically the 'folders' of an Active Directory. Can be used to Subscriptions, Security, Permissions. Litersally used to 'Orginaize' a user or 'Unit' into its apropriate category.<br/>

2.) Add/Create within domain a User by right clicking and adding a host into the 'Computers' OU.<br/>
	-On users PC go to system advance setting and rename the PC and add to domain. then from the domain refresh and check for the PC.<br/>
	-Can be tested with 'ipconfig /all', Check the host name and the DNS<br/>

How would you manage a user's acccount?<br/>
- Right clicking on the user's host name will allow an admin to use Computer Management tools such as Task Schedueler, Event Viewer, Windows logs, View Folders, Check Performane and more.<br/>

How would you find a users' account ?<br/>
- Right clicking the domain name and serach for the specific username/hostname of that users PC.<br/>

How would you promote a user?<br/>
- Right clicking a users hostname and directring to 'properties' then directing to to 'Members Of' and then finally adding them to the specific 'Group Policy' or 'Security Group'.<br/>

How would you add software to a large group of users or specific set of users?<br/>
- You can create a 'Group Policy' with that software installed and add users with the 'Members Of' tool to add the software remotely.<br/>

How would you create a user from the domain?<br/>
- Under the 'Users' OU right click and add a new user.<br/>

**On a local level a user cannot change Security Group setting(editing Local Users and Groups(Local)), Need to be changed from the admin server.<br/>

<h2>DHCP</h2><br/>
<p align="left">
What is a DHCP? What can it be used for?<br/>
-

**Within the DHCP tool > domain name > contains the scopes of the IPv4 and IPv6 names.<br/>

What is a scope?<br/>
- Basically the range of IP's used for a domain server. A scope range could be between 192.1.1.0 - 192.1.1.100 for example.<br/>

What is an adress lease?<br/>
- An adress lease is the amount of time an IP has before it expires. Alternativly you can make an IP never expire if you add it to the 'Reservations'/ simply reserve the ip for it to be permanent<br/>

**IPs with a lease can be deleted because it will be leased out a new IP later. BUT an IP with a reservation should never be deleted unless intructed to specifically delete the reservation.<br/>

What is reservation?<br/>
- Kinda like a static IP. Simply reserving an IP adress to connect to the DHCP. MAC address(Physical address) used to create a reservation. For example a printer would need a reservation IP. <br/>

1.) Creating a Reservation for a printer<br/>
	-Right click on reservations and click add. Type printer for name and use an IP within the Adress pool. i.e 192.1.1.50. Then type the printers MAC address(no spaces or dashes). Type description of 'Printer's IP Adress'.<br/>

<h2>DNS</h2><br/>
<p align="left">
What is a DNS? What is it used for?<br/>
-

**useful when going through a users files. If there was no DNS setup within the domain for the user, you would have to type out the IP directly on the searh bar to get to the users files rather than just '/home/user/files'<br/>

**Within AD DNS takes place in 'Forwar Lookup Zones', happens automatically within this tool<br/>

** ipconfig /flushdns flushes the dns to reset dns for a user. Do not flush dns on servers or printers or anything with a reservation basically. Does take  a mintue to refresh.<br/>
