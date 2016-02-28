##Knock Knock walk-through##

### 1. Setting the lab configuration.
> First of all we need to open your Visualization client in order to import the .ova which was given. In my case I will be using VMware Workstation 12 Pro.

>Now you can import the ova file.
>> Go-to **File -> Open -> Browse for your Knock Knock .ova and Click Import**.

>Now we have to start the KnockKnock box and Kali box. Then change the network adapter to the same network. I have put mine as **"Host Only Network"**.

#### 2. Finding out the KnockKnock Vms IP.
> When you booted up the knocknock vm you will be prompt to enter the username and the password to the system. This is not known to us. So we might need to use some other method to find out the IP address of the knockknock VM.

##### 2.1 Finding the IP address of the Kali machine
> Finding the IP adress can be done via typing the **""ifconfig"** command in the command prompt.
> 
> ![](http://i.imgur.com/XmX4P2r.png)

> Now we know that our IP is **192.168.117.130** Now we need to perform a network scan to see what are the other machines which are in my network.

##### 2.2 Scanning the network

>Now we need to use **NMAP** to map the network. To-do that,
>> In the Terminal type **nmap IP/Prefix**. in my case **"nmap 192.168.177.130/24"**
>![](http://i.imgur.com/jJ0GPnX.png)

>now we have scaned the network and findout that there are 4 hosts in the network 
>192.168.177.1 is the default gateway.
>192.168.177.130 is my machine
>192.168.177.129 might be the knock knock machine lets try to scan that again

