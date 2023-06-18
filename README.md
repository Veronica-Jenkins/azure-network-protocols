

<h1>Preforming Activities & Inspecting Network Protocols</h1>
This tutorial will show how we'll test some network activity<br />



</br><h2>Environments & Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Wireshark
- PowerShell

<h2>Operating Systems Used </h2>

- Windows 10 (22H2)
- Linux (Ubuntu Server)
</br>

<h2>Looking Under the Hood with Network Connectivity</h2>

<p>
<img src="https://i.imgur.com/V0iDDdU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/BiFcCwv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/Gw7J8yP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now that we're logged into VM1 we can download Wireshark (a program used to inspect network traffic). Go to the Wireshark website and download Wireshark <b><i>Windows Installer 64-bit</i></b>. Accept all the prompts. Once Wireshark is installed, open the program and select <b><i>ethernet adapter pack</i></b> - the network traffic is now displayed.
</p>
<br />
<p>
<img src="https://i.imgur.com/IIJsPez.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/xCrnsof.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To test connectivity between VM1 and VM2 we'll use a command called 'ping'. Go to the bottom left-hand corner of the screen and in the search bar type in <b><i>PowerShell</i></b>. This is similar to the Command Line for typing in prompts for the computer's response. Copy VM2's private IP Address and paste it after typing ping and hit enter. VM2 sends a response. Try the command ping 10.0.0.5 -t. This causes an endless spamming of traffic.     
</p>
<br />
<p>
<img src="https://i.imgur.com/MHtnty9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/vmha0er.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/0O9897c.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To stop the endless spamming we'll need to go to VM2's Network Security Group (NSG) - which is Azure's version of a firewall. Select VM2 NSG then go to <b><i>Inbound Security Rules</i></b>  VM2 Sec Group – inbound security rules- click add
Use commands in screenshot – select – icmp – select deny – name deny-icmp-from-anywhere
VM1 pings have timed out
    
</p>
<br />
<p>
<img src="https://i.imgur.com/fYtDOrT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/EA3T8Fo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/ZtAl194.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/7ukZlVk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/CRncKhi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
