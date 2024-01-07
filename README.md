# Setting-up-MFA-and-Protecting-RDP-using-Cisco-Duo-Security
---
---
In cybersecurity, fortifying the defenses of Remote Desktop Services is really important. This project makes an effort to elevate security measures by implementing Multi-Factor Authentication using Cisco Duo Security. As organizations increasingly rely on remote access solutions, ensuring the integrity of these connections becomes a crucial aspect of safeguarding sensitive information.

The objective of this project is to guide through the process of setting up a virtual machine on Microsoft Azure, configuring a server environment, and integrating Cisco Duo for robust MFA. The focus will be on securing the Remote Desktop Protocol (RDP) through a systematic approach, providing a comprehensive understanding of the steps involved.

By the end of this project, the aim is to establish a secure foundation for Remote Desktop Services, introducing an additional layer of protection that goes beyond traditional username and password authentication. This proactive approach aligns with the best practices in modern cybersecurity, addressing the ever-growing challenges posed by potential security threats in remote access scenarios.

So in this lab I will attempt to add that layer of security. So I will create a Virtual Machine, setup MFA on it and then test the MFA
---
1.
I create a Virtual Machine in Azure. I enter my login credentials for Microsoft Azure website and then I am re-directed to the Azure Portal Interface. So click on Virtual Machine and I will be given the option to “Create” . I will click on it, and I will be taken the Default Directory.

![141](https://imgur.com/YhRlBgk.png)

---
2. 
When in the default directory of the Virtual Machine, I click on create one more time to be taken to the configurations page.


![142](https://imgur.com/2jvU41Q.png)


---
3.
Once I am in the configurations page, I want to use a server so I will name the Virtual machine “Server2019”.

![143](https://imgur.com/iv7i3Pq.png)


---
4. 
I scroll down to the “Administrator Account” section and create a Username and Password

![144](https://imgur.com/nU8QPEd.png)

---
5. 
I am now done with the VM so I navigate to the “Review+Create”  and click on “Create” at the bottom of my screen.

![145](https://imgur.com/09sorW5.png)


---
6.
My Virtual Machine’s Deployment is now in Progress.

![146](https://imgur.com/I7Zda88.png)

---
7. 
I will now show how to enable MFA for Remote Desktop Protocol because if you have a server and you have no type of layer of security then It is not secured and it will be easy for attackers to get to your device.

So I will go to Cisco DUO Security and enter my credentials and login. 

Once logged in, I will navigate to the left pane and click on “Users”, and once clicked on, the tab expands for more options. I will click on “Add Users”


![147](https://imgur.com/529WAC0.png)

---
8.
Now that I am in the “Add Users” directory, I will enter the username of the account that I created in the 4th step which was “Helpdesk” and it will be used to login to the Remote Desktop. So after I type in the Username, I click on “Add User” 

![149](https://imgur.com/O3zwB6C.png)

---
9.
 I am redirected to the next page that asks for more information and more configurations and MFA add ons I can put on the account such as adding “Security Keys”, “Bypass Codes”,  and “Hardware Tokens” . The user has now been added successfully as seen at the top of screen. 

I will fill in the information as needed.  


In the “Status” part I click on “Active” to require multi-factor auth.

And then click on “Save Changes”.

![150](https://imgur.com/a1Urexj.png)
![151](https://imgur.com/Wdji3p8.png)
![153](https://imgur.com/jJxrlGR.png)

---
10.
I am now going to navigate back to the top and click on “Send Enrollment Email” and what that means is that  I want to set up “Helpdesk” at the login.

![154](https://imgur.com/RhqZi08.png)

---
11. 
I go to my Email and find the like that the Duo Security website sent me and click on it.

![155](https://imgur.com/DuXSA4w.png)


---
12.
After clicking the link I am redirected to this page. I click on Next

![156](https://imgur.com/pfDFRjS.png)

--
13.
I click on mobile phone s my MFA option. 

As seen, Duo offers a lot of MFA options that range from fingerprints, Duo Mobile app, a security key, and a phone number

**Note to self** : I can use Duo Mobile app but I don’t want to download apps on my phone for storage space purposes and I’ll try the “security Key” option potentially later.

![157](https://imgur.com/0TKkxRH.png)

---
14. 
I enter my phone number and click on continue

![158](https://imgur.com/yJquXiq.png)

---
15.
Confirm that the number is correct and click “Yes, it’s correct”.

![159](https://imgur.com/SH9zx8x.png)

---
16.
Now I have added text message, so I can no log in with Duo using text messages. Click on continue

![160](https://imgur.com/kzUUoi2.png)

---
17.
It will then ask me to add another way to log in, and I don’t have space for duo mobile so I will just click on “skip for now”.

![161](https://imgur.com/0W5GEMW.png)

---
18. 
Now my set up is finally complete. 



![162](https://imgur.com/XYpsLFE.png)

---
19.
So now I navigate back to my virtual machine in azure and see that my Virtual Machine deployment is complete so I will now click on “Download”.

![163](https://imgur.com/gDSZXeA.png)

---
20.
Then I go to the main Azure Portal home page. And click on Virtual machines to be redirected to the default directory.

![164](https://imgur.com/Co6e7uS.png)

---
21.
I click on “server2019”

![165](https://imgur.com/NXenCYV.png)

---
22.
The “Server2019” VM information pops up on the right side of my screen. I search for “Connect”.

![166](https://imgur.com/2mAf9wH.png)


---
23. 
Once I am in the “Connect” directory, I am given a public IP address. So I’m gonna download the RDP file  

![167](https://imgur.com/hGK8ob7.png)

---
24. 
Once downloaded, a pop of my recent download history appears on my top right corner of my screen, I will click in the rdp file that I just downloaded. 

![168](https://imgur.com/caWFx1k.png)

---
25. 
When I click on it, the Windows Remote Desktop connection application pops up on my screen with the public IP address of my VM, giving  me options to “Connect” to my VM or “cANCEL”, I will click on Connect.

![169](https://imgur.com/tQwMsZL.png)

---
26.
Once I click on connect, I see another pop up page asking me to enter the password I created for this VM. I enter the password into the entry field then click Ok

![170](https://imgur.com/18zypsG.png)

---
27.
I am now connected to my VM and now will setup my second layer of Security that I mentioned which is  “MFA” because I don’t want to have issues with security because it is a security vulnerability. And I normally do this at my company. This isn’t something that is out of the ordinary but it is something that you can set up in your environment(company/employer)

![171](https://imgur.com/FaEH6L8.png)


---
28. 
I now navigate to Microsoft edge in my virtual machine.

![172](https://imgur.com/Xq1sGKS.png)

---
29.
I will enter duo admin login  in my web browser and enter my details/credentials on the site and log in

![173](https://imgur.com/EHYQb5x.png)

---
30. 
It will then ask for my MFA passcode sent to my phone and then I enter it

![174](https://imgur.com/EHYQb5x.png)

---
31. 
Once I am inside of my account. I navigate to Applications on the left pane


![175](https://imgur.com/omkXzwX.png)

---
32. 
I will then click on “Protect an Application” on the right corner of the web application

![176](https://imgur.com/9wgsE9k.png)


---
33. 
I will type in RDP in the entry field, and click on the “Microsoftt RDP” section on the left where it says “Protect”

![177](https://imgur.com/rHT1Fdf.png)


---
34.
I am now navigated to the configuration page of Microsoft RDP. And as you can see at the top, I have added Microsoft RDP to the protected applications. 

As seen on the screen, I now have the Integration key, The secret key, and the API hostname. 


![178](https://imgur.com/CQzBRT4.png)

---
35.
 I am going to click on, RDP documentation right above on my mouse 

![179](https://imgur.com/LnTGe69.png)

---
36.
I read through the whole documentation to get a better understanding of the duo authentication Windows Logon and RDP.

Navigate to first steps on the left pane 

Go to step number 6 and download “Duo Authentication for Windows Logon Installer Package”

![180](https://imgur.com/fzHv0wc.png)

---
37.
When finished downloading, click on the download to open file

![181](https://imgur.com/IDtdd59.png)


---
38.
Once clicked on,  it will begin installing

![182](https://imgur.com/NdIfCNJ.png)

---
39. 
An Introduction page from the Installer package  then pops up, and I click on next.

![183](https://imgur.com/AyTmvpj.png)

---
40. 
In the “API hostname” entry, I navigate back to the Admin portal of my duo security in a different tab and retrieve that information

![14](https://imgur.com/P034lfb.png)


---
41.
I now enter the security key and the integration key.

![15](https://imgur.com/bUhvUH0.png)

---
42.
I will keep the Bypass duo when offline “checked” as well as the “Use auto push to authenticate enabled. Keep both of those checked. I will leave the “Only Prompt for Duo Authentication when logging in via RDP” unchecked simply because it does not require MFA approval.


![16](https://imgur.com/Lon072i.png)


---
43. 
Now I click install.

![17](https://imgur.com/lgRY9oB.png)

---
44.
I wait for the install to finish

![18](https://imgur.com/LuIEx2m.png)

---
45.
Now I click “Finish” . Now I am all set to use the Duo Authentication whenever I log on to this machine virtually. I am now going to test it to see if it works. So I exit out of my VM entirely and reopen it back up. 

![19](https://imgur.com/c35QMCd.png)


---

After opening up, the process of enforcing Cisco Duo MFA is officially a success. Once anyone enters into the VM, they will be faced ny the first layer of security which is the MFA. Unless someone has a tool that can intercept my SMS messages in a man-in-the-middle attack, or has my secret key, or has my account information on the Duo Mobile App, it'll be pretty tough to get into the VM.

![184](https://imgur.com/smoI8xj.png)



----
In conclusion, this project aimed to enhance security measures for Remote Desktop Services by implementing Multi-Factor Authentication (MFA) using Cisco Duo Security. The process involved setting up a virtual machine on Microsoft Azure, configuring the server, and integrating Cisco Duo for MFA. This project covered creating a VM, enrolling users in Cisco Duo, and securing the Remote Desktop Protocol (RDP) with MFA.

The deployment of the virtual machine, coupled with the addition of MFA through Cisco Duo, adds an extra layer of protection to the Remote Desktop environment. By enforcing MFA, the project ensures that unauthorized access is significantly mitigated, enhancing overall security posture. The stepwise approach, including Azure VM setup, Cisco Duo integration, and RDP protection, serves as a comprehensive guide for implementing advanced security measures in a practical IT environment. The successful implementation of Cisco Duo MFA demonstrates a proactive approach to safeguarding access to critical systems and aligns with best practices in cybersecurity.





