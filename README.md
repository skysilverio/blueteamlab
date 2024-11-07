<h1>Blue Team Lab</h1>



<body>
  <h2>Description</h2>
  <p>This project involves creating a Blue Team lab environment. The initial components of the lab are listed below, and more will be added as the project progresses. The lab will serve as a foundation for gaining hands-on experience in cybersecurity. Each part of the home lab will be detailed in separate sections. This page will include a summary of each component along with a link to the detailed steps taken to create it.</p>
  <ul>
    <li>Firewall</li>
    <li>Malware Analysis (MA) VMs (one for Linux and one for Windows)</li>
    <li>Windows 7 host</li>
    <li>Windows 10 host</li>
    <li>Windows Server AD</li>
    <li>Linux Server(s)</li>
    <li>Kali Linux</li>
    <li>DFIR</li>
    <li>SIEM</li>
    <li>Vulnerability Scanner</li>
  </ul>
</body>

<br />


<h2>Tools Used</h2>

- <b>Oracle VirtualBox</b> 
- <b>Powershell</b>
- <b>pfSense</b>
- <b>Tsurugi</b>
- <b>REMnux</b>
- <b>Kali Linux</b>

<h2>Environments Used</h2>

- <b>Windows 10</b>
- <b>Windows 7</b>
- <b>Windows Server 2019</b>

<h2>Part 1 - Network Topology</h2>
<p>Below is the network topology of the lab environment. Since I will be using Oracle VirtualBox, I will also need to create separate VLANs and subnets. I color-coded and labeled each VLAN to show the separate roles and functions for each VLAN.</p>

<img src="https://github.com/skysilverio/blueteamlab/blob/main/Network%20Topology.png" alt="Network Topology" style="width:100%; height:auto;">

<h2>Part 2 - Deploying a Firewall</h2>
<p>I used pfSense as the main firewall for my homelab. Since Virtualbox only allows you to add 4 Network Adapters on its UI, I needed to run PowerShell scripts to add 2 additional Network Adapters to the Virtual Machine. Below is a screen capture of all the Network Adapters connected to the firewall. Lastly, I created rules and permissions for each VLAN.</p>

<img src="https://github.com/skysilverio/blueteamlab/blob/main/pfSense_cmd.png" alt="pfSense cmd" style="width:100%; height:auto;">

<h2>Part 3 - DFIR </h2>
<p>I decided to use <a href="https://tsurugi-linux.org">Tsurugi Linux</a> as the DFIR VM. It is a pretty straight forward download. I detailed a few more points on implementation in the full DFIR section.</p>

<img src="https://github.com/skysilverio/blueteamlab/blob/main/Tsurugi-Linux%20Desktop.png" alt="TsurugiVM" style="width:100%; height:auto;">

<h2>Part 4 - Malware Analysis</h2>
