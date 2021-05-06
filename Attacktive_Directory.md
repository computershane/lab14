#TryHackMe

<img src="Attacktive_directory.png"
     alt="Attacktive_directory_icon"
     style="float: left; margin-right: 10px;" />
     
#Task 1  Intro Deploy The Machine
Connected VPN

#Task 2  Intro Setup

Installing Impacket:

Whether you're on the Kali 2019.3 or Kali 2021.1, Impacket can be a pain to install  correctly. Here's some instructions that may help you install it correctly!

First, you will need to clone the Impacket Github repo onto your box. The following command will clone Impacket into /opt/impacket:

Ran commands ```sudo git clone https://github.com/SecureAuthCorp/impacket.git /opt/impacket```

After the repo is cloned, you will notice several install related files, requirements.txt, and setup.py. A commonly skipped file during the installation is setup.py, this actually installs Impacket onto your system so you can use it and not have to worry about any dependencies.

To install the Python requirements for Impacket:

Ran commands>>
```sudo pip3 install -r /opt/impacket/requirements.txt```
```cd /opt/impacket/ && sudo python3 ./setup.py install```

Installing Bloodhound and Neo4j

Bloodhound is another tool that we'll be utilizing while attacking Attacktive Directory. We'll cover specifcs of the 
tool later, but for now, we need to install two packages with Apt, those being bloodhound and neo4j. You can install 
it with the following command:

```sudo apt install bloodhound neo4j```

#Task 3  Enumeration Welcome to Attacktive Directory

Welcome to Attacktive Directory

Welcome Dear User!

Thank you for doing my first room. I originally created this room for my final project in my Cyber Security degree
program back in 2019. Since then, I've gone on to make several other rooms, even a Network for THM. In March 2021,
I made the decision to renovate this room and make it more guided and less challenge based so there are more
learning opportunities for others. I hope you enjoy it.

Love,

Spooks



Enumeration

Basic enumeration starts out with an nmap scan. Nmap is a relatively complex utility that has been refined over the
years to detect what ports are open on a device, what services are running, and even detect what operating system is
running. It's important to note that not all services may be deteted correctly and not enumerated to it's fullest 
potential. Despite nmap being an overly complex utility, it cannot enumerate everything. Therefore after an initial
nmap scan we'll be using other utilities to help us enumerate the services running on the device.

For more information on nmap, check out the nmap room.



Notes: Flags for each user account are available for submission. You can retrieve the flags for user accounts via
RDP (Note: the login format is spookysec.local\User at the Window's login prompt) and Administrator via Evil-WinRM.
