![image](https://github.com/Loughton03/soc-authentication/assets/78968473/fa2aef64-01b0-4007-87b0-36bebb4c568e)<p align="center">
<img src="https://i.imgur.com/8I0YcgP.png" alt="Azure logo"/>
</p>

<h1>Precursor to Security Operations (Failed Authentication and Log Observation)</h1>
We will create a virtual computer in the cloud, and this computer will be the one we pretend to attack. Our main goal for this lab is to carefully look at the records or logs and determine if something is a false negative, false positive, true positive, or true negative.<br />



<h2>Actions and Observations</h2>

<p>
1. Create an attack VM in a different region to simulate a threat against our Windows VM. You can create a new resoursse group for this vm since we are simulating the attack somewhere other than your geographical region. Name the VNet "Lab-VNet-Attacker."
</p>

<p>
<img src="https://i.imgur.com/4MIsqE1.png" height="80%" width="80%" alt="Resource Group Setup"/>
</p>

<p>
<img src="https://i.imgur.com/YmOparo.png" height="80%" width="80%" alt="Resource Group Setup"/>
</p>

<p>
2. Obtain the public IP address of the attack VM and use the Remote Desktop Connection to access it.
</p>
<br />

<p>
<img src="https://i.imgur.com/LqQN8wu.png" height="80%" width="80%" alt="Virtual Machine Setup"/>
</p>
<p>

<p>
3. Open remote Desktop Protocol (RDP) from inside the attack VM and input the windows vm IP address.
</p>

<p>
<img src="https://i.imgur.com/JcgdjK5.png" height="80%" width="80%" alt="Public IP Address"/>
</p>
<br />

 
3. We will now initiate five failed Remote Desktop Protocol (RDP) login attempts from the attacker VM to the Windows VM.
</p>
<br />

<p>
<img src="https://i.imgur.com/s6B0UE8.png" height="80%" width="80%" alt="Public IP Address"/>
</p>



<p>
5. Install SQL Server Management Studio (SSMS) on the attack VM and generate five failed MS SQL Authentication logs against the Windows VM.
</p>

<p>
<img src="https://i.imgur.com/36WEPAK.png" height="80%" width="80%" alt="Public IP Address"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/VvJPiCD.png" height="80%" width="80%" alt="Public IP Address"/>
</p>
<br />


<p>
6. Now we will open remote Desktop Protocol (RDP) from inside the attack VM and input the linux vm IP address. We will now initiate five failed Remote Desktop Protocol (RDP) login attempts from the attacker VM to the linux VM.
</p>

<p>
<img src="https://i.imgur.com/iVjszTW.png" height="80%" width="80%" alt="Public IP Address"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/kjdXTEx.png" height="80%" width="80%" alt="Public IP Address"/>
</p>
<br />


<p>
7. Reconnect to the Windows VM via RDP from our computer, log into event viewer, Analyze successful and unsuccessful login events, paying attention to EventIDs, messages, source IP addresses, and other relevant information in the Security log for RDP and the Application log for SQL.
</p>

<p>
<img src="https://i.imgur.com/sK0GkJa.png" height="80%" width="80%" alt="Public IP Address"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/2Iv1Go1.png" height="80%" width="80%" alt="Public IP Address"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/5YTu3qy.png" height="80%" width="80%" alt="Public IP Address"/>
</p>
<br />


8. From our computer we will login to the linux VM and take a look at the failed logs.
</p>

<p>
<img src="https://i.imgur.com/M3zTwaV.png" height="80%" width="80%" alt="Public IP Address"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/tjl6lhh.png" height="80%" width="80%" alt="Public IP Address"/>
</p>
<br />









