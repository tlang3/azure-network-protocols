<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
Detailed by the tutorial below, I observed various network traffic to and from Azure Virtual Machines with Wireshark as well as experimented with Network Security Groups. <br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Create a resource group in Azure
- Create a Windows VM and a Linux VM
- Use remote Remote Desktop to connect to Windows VM
- Install Wireshark in Windows VM
- Filter by ICMP traffic in Windows VM
- Ping the private IP address of Linux VM from Windows VM
- In Windows VM, open Powershell, ping a public address, and observe traffic in Wireshark
- Initiate non-stop ping from Windows VM to Linux VM
- Open the Network Security Group that Linux VM is using and disable ICMP traffic
- Observe ICMP traffic in Wireshark
- Re-enable ICMP traffic
- Observe ICMP traffic in Wireshark again
- Filter for SSH traffic in Wireshark
- Type commands into Linux VM and observe the SSH traffic in Wireshark
- Filter for DHCP traffic in Wireshark
- Issue a new IP address in Windows VM from the command line
- Observe DHCP traffic in Wireshark
- Filter for DNS traffic in Wireshark
- Use nslookup in command line to find what the IP addresses are for a few public websites
- Observe DNS traffic in Wireshark
- Filter for RDP traffic in Wireshark
- Observe the non-stop spam of traffic
- Close Remote Desktop and delete the resource groups/VMs


<h2>Actions and Observations</h2>

1. Create a resource group in Azure

2. Create a Windows VM and a Linux VM

   ![create windows and linux vms](https://github.com/meganhoose/azure-network-protocols/assets/142938638/58582584-46c5-4775-812a-b8fe66dff767)


3.  Use remote Remote Desktop to connect to Windows VM

4.  Install Wireshark in Windows VM

   ![download and open wireshark](https://github.com/meganhoose/azure-network-protocols/assets/142938638/af9b1c93-9b12-4979-bc39-40aa0ef1f809)


5.  Filter by ICMP traffic in Windows VM

   ![filter by ICMP traffic in wireshark](https://github.com/meganhoose/azure-network-protocols/assets/142938638/ed1db93d-60f6-48f7-9d25-67dbe8cc427b)


6. Ping the private IP address of Linux VM from Windows VM

   ![ping linux vm in wireshark](https://github.com/meganhoose/azure-network-protocols/assets/142938638/8f554956-b0eb-4344-ab0f-ee0ca34ad4c1)


7. In Windows VM, open Powershell, ping a public address, and observe traffic in Wireshark

   ![ping google in wireshark](https://github.com/meganhoose/azure-network-protocols/assets/142938638/13eeb5fe-1350-4467-86ee-98d05937e178)


8. Initiate non-stop ping from Windows VM to Linux VM

![ping nonstop in wireshark](https://github.com/meganhoose/azure-network-protocols/assets/142938638/9131bc82-47c5-4bcf-ac05-a82132e36015)


9. Open the Network Security Group that Linux VM is using and disable ICMP traffic

  ![inbound security rule for icmp traffic 200](https://github.com/meganhoose/azure-network-protocols/assets/142938638/a000d980-95c2-4084-81ba-b1db98b9872a)



10.  Observe ICMP traffic in Wireshark

  ![filter by ICMP traffic in wireshark](https://github.com/meganhoose/azure-network-protocols/assets/142938638/800fe062-d59c-482c-ba60-3d16992c8347)


11.  Re-enable ICMP traffic

12.  Observe ICMP traffic in Wireshark again


13.  Filter for SSH traffic in Wireshark


![filter by ssh traffic and ssh into linux vm2](https://github.com/meganhoose/azure-network-protocols/assets/142938638/0326c00d-35d8-4609-8cb9-fcd0790c16e4)


14. Type commands into Linux VM and observe the SSH traffic in Wireshark

![commands in wireshark for vm2](https://github.com/meganhoose/azure-network-protocols/assets/142938638/2c3a58e2-3970-492e-8daa-a38e0d0bdc4a)


15. Filter for DHCP traffic in Wireshark

![filter by dhcp traffic](https://github.com/meganhoose/azure-network-protocols/assets/142938638/8799ac85-ce62-40ed-aa80-db984b325525)


16. Issue a new IP address in Windows VM from the command line


17. Observe DHCP traffic in Wireshark

![filter by dhcp traffic](https://github.com/meganhoose/azure-network-protocols/assets/142938638/7a6c0d0b-5d0e-4fd9-a7a1-0fa60f83fdb9)


18. Filter for DNS traffic in Wireshark

![filter by dns traffic and type in nslookup for google](https://github.com/meganhoose/azure-network-protocols/assets/142938638/e51ee30b-5b6a-4f4e-9471-7321a8217124)


19. Use nslookup in command line to find what the IP addresses are for a few public websites

![nslookup search cname](https://github.com/meganhoose/azure-network-protocols/assets/142938638/9ef59065-eca8-42e4-835d-2a6c96e4ca67)


20. Observe DNS traffic in Wireshark

21. Filter for RDP traffic in Wireshark

![filter by rdp traffic](https://github.com/meganhoose/azure-network-protocols/assets/142938638/8e2fe167-f931-4ae5-b927-add1fe4a50c5)


22. Observe the non-stop spam of traffic

23. Close Remote Desktop and delete the resource groups/VMs
