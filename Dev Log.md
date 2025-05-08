>"Anyone who has never made a mistake has never tried anything new" :Albert Einstein<br>
<br>
<h1>Dev Log</h1>
<p>
  This is to document the progress for my mini Home Lab server rack project.<br>
  Author:JoshuaB99<br>
  08/05/2025
</p>
<br>
<br>
<br>
<p>
<h3>----Objective----</h3>
Create a small network environment where I can develop my networking skills and host VMs for various projects and game servers.<br>
<br>
<h3>----planned features----</h3>
  <ul>
    <li>Pihole DNS server for add blocking</li>
    <li>5x Pi5 cluster hosting Proxmox</li>
    <li>NAS with 1TB SSD Raid 1 disk mirroring</li>
    <li>Wazuh SIEM</li>
    <li>2x Layer 2 8 port gigabit switches with POE</li>
    <li>UPS 480W 230V 850VA</li>
    <li>RADIUS server to authorise devices and for user activity logging</li>
</ul>
<h3> ----Possible future features---- </h3>
- VPN server for remote connection when away from home
</p>
<br>
<br>
<br>
warning! ahead are the sleep deprived ramblings of someone pretending to be a network engineer<br>
you have been warned<br>
<br>
<h2>Dev Log 1 - 08/05/2025 22:55</h2>
<p>
  The plan build a small server rack to have some fun with, this will be my first proper networking project outside of messing with my home router and connecting to a raspberry pi via SSH.
  I'm planning to use a DeskPi RackMate T1 which is a small 10 inch 8U mini server rack made for people in my situation who don't want a full 19 inch server rack.
  
  In this server rack I'm going to have a Raspberry Pi cluster so I can run some virtual machines on it and also some network access storage to store all the files for the VM's. I'm
  planning to power the whole thing with a small uninterrupted power supply to protect the hardware and a power over Ethernet switch to make it easier to power the whole thing (spoiler it
  doesn't). So my current internet access is a bit of a predicament as the accommodation I'm living in does not give me direct access to the router connected to the internet or the wireless
  access point I connect to, for the time being I probably wont be able to connect to the server from outside the network oh well.

  The router I'm using is the GL.iNet GL-SFT1200 which is small travel router running of OpenWrt which is quite a popular open source router OS that can be installed on many devices and has
  tons of configuration options. I should also mention I have no Ethernet ports in my accommodation and can only connect via a wireless connection which is one of the reasons I chose this
  router as it can connect to other networks such as hotel Wi-Fi etc. I also need to put my devices MAC address in to access the internet the amount of devices I can connect and the speed I
  get depends on how much I pay, so this might be a bit tricky to get working but I have confidence and hours of free time.

  Got the router connected to the internet and got it working by cloning my laptops mac address on the router so the ISP thinks its my laptop connecting to the network, however the router
  itself has internet access but the devices connected to the router have no internet connection, after running some trouble shooting I found when connected to the router I can ping DNS
  servers like 8.8.8.8 or 1.1.1.1 but my devices DNS query's don't get through. it seems to be because the devices connected don't get the correct DNS server address from the router this
  could be a problem with the NAT but is most likely my ISPs router can tell what I'm trying to do as I have tried so many different things to try and get it working.

  The router has a feature to connect to a VPN for added security using this feature I can hide the network traffic from my ISP so they cannot tell how many devices are connected to the 
  internet this works and the devices connected to the router get internet access finally, However I am only getting a connection speed of around 50mbs this will not do! I am paying for 
  more and would like to use all of it.(note the max I can get is like 250mbs) Turns out the reason is the hardware in the router it self, the VPN I'm using uses wire guard which is the 
  fastest VPN protocol available but the router has a max speed of 65mbs even with wire guard and 10mbs with open VPN protocol. I have decided I'm going to send the router back and upgrade 
  it to the GL.iNet GL-AXT1800 which has a max speed of 550mbs on wire guard VPN clients and has a few more features in general but it was twice the cost of the first router. Success I am 
  getting the full speed I am paying for.
</p>
<br>
<h2>Dev Log 2 - 09/05/2025 ##:##</h2>
<br>
<br>
<p>
  
</p>
