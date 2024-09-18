# HTML_Metasploit
A metasploit console simulator in HTML (Hyper Text Makeup Language).


## Usage

### Basic Meterpreter Commands

 sysinfo : This command is used to retrieve basic information about the target system, including the OS version, architecture, hostname, and uptime.


ps : This command is used to list all the running processes on the target system. It is a useful tool for understanding the state of the target system and identifying potentially interesting processes that could be exploited.
ps

sessions : This command is used to list all the active meterpreter sessions. It is useful for managing multiple sessions and switching between them.
sessions

shell : This command is used to spawn a shell in the target system. It is a powerful tool for executing commands in the target system and interacting with the underlying operating system.
shell

migrate : This command is used to move the meterpreter session from one process to another. It is used to evade detection and ensure persistence in the target system.
migrate

getpid : This command is used to retrieve the process ID of the current meterpreter session. It is a useful tool for understanding the state of the session and determining the best process to migrate to.
getpid

getsystem : This command is used to elevate the current meterpreter session to SYSTEM-level privileges. It is a powerful tool for gaining complete control over the target system.
getsystem1

## File System Commands


ls- This command lists the contents of the current directory on the target system.
ls

cd- This command changes the current directory on the target system.
cd

pwd- This command displays the current directory on the target system.
meterpreter > cd c:\windows
 meterpreter > pwd
 c:\windows

cat- This command allows an attacker to view the contents of a file on the target system.
meterpreter > cat edit.txt
  What you talkin' about Willis

upload : This command allows an attacker to upload a file from their local system to the target system.
upload

Download- This command allows an attacker to download a file from the target system to their local system.
 meterpreter > download c:\\boot.ini
  [*] downloading: c:\boot.ini -> c:\boot.ini
  [*] downloaded : c:\boot.ini -> c:\boot.ini/boot.ini

rm : This command allows an attacker to delete a file on the target system.
rm

## Network Commands

portfwd : This command allows the tester to forward traffic from one port on the target system to another port on the local system or another system on the network.
portfwd

route : This command allows the tester to add, modify, or delete routes on the target system's routing table. This can be useful for routing network traffic through the target system or for redirecting traffic from one network to another.
msf6 post(multi/manage/autoroute) > route

IPv4 Active Routing Table
=========================

   Subnet             Netmask            Gateway
   ------             -------            -------
   169.254.0.0        255.255.0.0        Session 1
   172.19.176.0       255.255.240.0      Session 1

[*] There are currently no IPv6 routes defined.
msf6 post(multi/manage/autoroute) >

arp_scanner : This command allows the tester to perform an ARP scan of the target network, which can be useful for discovering other systems on the network and their IP addresses.
arp_scanner

ping : This command allows the tester to send a ping to another system on the network, which can be useful for checking network connectivity and determining the latency of network communications.
ping

traceroute : This command allows the tester to trace the route that network packets take from the target system to another system on the network, which can be useful for understanding the routing of network traffic and identifying potential points of failure or compromise.
netstat : This command allows the tester to view information about the target system's network connections, including the status of active connections, listening ports, and routing information.
Advanced Meterpreter Commands
Advanced Meterpreter commands are a set of commands used in the Meterpreter tool for performing more complex and sophisticated penetration testing tasks. These commands can provide information and execute actions that go beyond basic system and network manipulation.

Some of the commonly used advanced Meterpreter commands include:

migrate : This command is used to migrate the Meterpreter payload from one process to another, which can be useful in cases where the initial process is terminated.
migrate

keylogrecorder : This command is used to record keystrokes on the target system.
persistence : This command allows the attacker to persist the Meterpreter session on the target system even after it has been rebooted, making it easier to regain access to the system later.
screengrab : This command takes a screenshot of the target system, providing valuable information to the attacker.
getsystem : This command is used to escalate the attacker's privilege level on the target system to that of an administrator.
webcam_snap : This command is used to take a snapshot from the target system's webcam, which can be useful for capturing images of the target user.
meterpreter > webcam_snap -h
  Usage: webcam_snap [options]
  Grab a frame from the specified webcam.
  
  ## OPTIONS:
  
  -h      Help Banner
  -I The index of the webcam to use (Default: 1)
  -p   The JPEG image path (Default: 'gnFjTnzi.jpeg')
  -q   The JPEG image quality (Default: '50')
  -v   Automatically view the JPEG image (Default: 'true')

webcam_stream : This command is used to stream the target system's webcam feed, which can be useful for monitoring the target user's activities.
hashdump : This command is used to dump the password hashes from the target system, which can be useful for cracking the passwords and gaining further access to the system
