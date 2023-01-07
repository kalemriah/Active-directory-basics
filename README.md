# Active-Directory-Basics
Futher understanding Windows Active Directory for knowledge skillsets 

<h2>Topics</h2>
<p align="left">
-Active Directory, DHCP, DNS. This is a short summary of these topics and some examples of how they might be used.<br/>

<h2> Active Directory</h2><br/>
<p align="left">

What is an Active Directory? What can it be used for? <br/>
- An Active Directory is an essential tool/service made by microsoft that includes a ton of services, tools, and resources to admin or connect users within a network. Active Directory is a great tool/service for coprerations to promote efficientcy within their network. <br/>


What is a Domain?<br/>
- A domain is the host server. A domain is similar to how somebody hosts a party. the domain would be the party host with all the control to remove or invite people ect. and the guests would be simialr to the users. Alternativly can be though of like a Country.<br/>
What is an Orginaztional Unit?
-Basically the 'folders' of an Active Directory. Can be used to Subscriptions, Security, Permissions. Litersally used to 'Orginaize' a user or 'Unit' into its apropriate category.<br/>

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
-  Dynamic Host Control Protocol. DHCP is used to automatically assign IP addresses within a domain/network. So, for example say you have 4 different devices on a network. The DHCP will automatically assign the devices different IP addresses so that they can communicate over the network without overlapping. So, device 1's IP could be 192.168.1.1, device 2's IP = 192.168.1.2, device 3 = 192.168.1.3, device 4 = 192.168.1.4. This protocol is extremely important because without it you would have to manually configure IPs on a network. Imagine having to configure hundreds of IPs for a corporate network without DHCP and you'll begin to see how necessary this protocol is to a network.

What is a scope?<br/>
- Basically the range of IP's used for a domain server. A scope range could be between 192.1.1.0 - 192.1.1.100 for example.<br/>

What is an adress lease?<br/>
- An adress lease is the amount of time an IP has before it expires. Alternativly you can make an IP never expire if you add it to the 'Reservations'/ simply reserve the ip for it to be permanent<br/>

**IPs with a lease can be deleted because it will be leased out a new IP later. BUT an IP with a reservation should never be deleted unless intructed to specifically delete the reservation.<br/>

What is reservation?<br/>
- Kinda like a static IP. Simply reserving an IP adress to connect to the DHCP. MAC address(Physical address) used to create a reservation. For example a printer would need a reservation IP. <br/>

<h2>DNS</h2><br/>
<p align="left">

What is a DNS? What is it used for?<br/>
- Domain Name System is a protocol that turns IP addresses into 'readable' addresses. For example, nobody is going to remeber that 8.8.8.8 is the IP address for google. They're going to type in 'google.com'. This 'google.com' = 8.8.8.8 is an example of DNS in action. So, a way you would use DNS in a domain is in a situation where you have a ton of devices within a domain and you have no way of remembering all of the IP addresses so you come up with a DNS naming system to easily access the devices from the domain controller.

**useful when going through a users files. If there was no DNS setup within the domain for the user, you would have to type out the IP directly on the searh bar to get to the users files rather than just '/home/user/files'<br/>

**Within AD DNS takes place in 'Forward Lookup Zones', happens automatically within this tool<br/>

** ipconfig /flushdns flushes the dns to reset dns for a user. Do not flush dns on servers or printers or anything with a reservation basically. Does take  a mintue to refresh.<br/>
