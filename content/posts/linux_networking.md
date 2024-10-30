---
title: "Linux networking"
date: 2024-10-29T09:20:42-06:00
description: ""
summary: ""
categories:
draft: false
categories: [""]
tags: [""]
keywords: [""]

---

# linux_networking

This is a recopilation of commands and its executiong based on the book `THE GORILLA GUIDE TO LINUX
NETWORKING 101`

## Chapter 2

```bash
❯ ssh cumulus@192.168.1.107
cumulus@192.168.1.107's password: ********
Welcome to Cumulus VX (TM)
Cumulus VX (TM) is a community supported virtual 
appliance designed for experiencing, testing, and 
prototyping Cumulus Networks' latest technology.
For any questions or technical support, visit our 
community site at: http://community.cumulusnetworks.com
The registered trademark Linux ® is used pursuant to a 
sublicense from LMI, the exclusive licensee of 

```

```bash
❯ uname -a
Linux e-pc 5.15.0-124-generic #134~20.04.1-Ubuntu SMP Tue Oct 1 15:27:33 UTC 2024 x86_64 x86_64 x86_64 GNU/Linux

```

Show the type of operating system 

```bash
❯ uname -a
Linux e-pc 5.15.0-124-generic #134~20.04.1-Ubuntu SMP Tue Oct 1 15:27:33 UTC 2024 x86_64 x86_64 x86_64 GNU/Linux

```

Show host info and other data
```bash
❯ hostnamectl
   Static hostname: e-pc
         Icon name: computer-laptop
           Chassis: laptop 💻
        Machine ID: 34a383e3a4c9492584d9b5fee7932a04
           Boot ID: be0e8ac233fa4734b7721b398d184026
  Operating System: Ubuntu 20.04.6 LTS
    OS Support End: -
OS Support Expired: 54y 9month 4w
            Kernel: Linux 5.15.0-124-generic
      Architecture: x86-64
```

Print working directory

```bash
❯ pwd
/home/erick

```
List files that are present in the folder
```bash
❯ ls
'2022-12-19 15-36-29.mkv'  '2023-03-06 14-03-44.mkv'  '2023-03-23 14-05-14.mkv'  '2024-04-15 14-35-45.mkv'   binaries_installs/             Downloads/              proyects/
'2022-12-20 15-34-27.mkv'  '2023-03-07 14-01-59.mkv'  '2023-04-03 14-03-15.mkv'  '2024-04-15 14-38-27.mkv'   blog/                          examenTecuan/           Public/
'2023-01-02 18-39-41.mkv'  '2023-03-07 16-01-11.mkv'  '2023-04-19 17-37-25.mkv'  '2024-04-15 14-39-07.mkv'   CLionProjects/                 ExpanDrive/             SmartBear/
'2023-02-13 14-25-11.mkv'  '2023-03-07 16-08-41.mkv'  '2023-11-01 22-27-37.mkv'  '2024-04-15 14-43-40.mp4'   code/                          Firefox_wallpaper.png   snap/
'2023-02-14 14-23-23.mkv'  '2023-03-07 16-10-51.mkv'  '2023-11-07 09-52-49.mkv'  '2024-04-15 14-44-26.mp4'   conf_vim.md                    geb_scrip.groovy        Templates/
'2023-02-14 14-34-04.mkv'  '2023-03-07 16-11-40.mkv'  '2023-11-08 09-45-05.mkv'  '2024-04-20 06-36-22.mp4'   cultivos.mp4                   IdeaProjects/           tmp/
'2023-02-16 14-09-09.mkv'  '2023-03-07 16-14-50.mkv'  '2023-11-17 12-06-38.mkv'  '2024-04-20 06-37-49.mp4'   cultivos.osp                   IdeaSnapshots/          uni/
'2023-02-20 13-59-04.mkv'  '2023-03-07 16-14-52.mkv'  '2023-11-17 18-06-01.mkv'  '2024-04-30 12-40-12.mp4'   cumple                         logs/                   Videos/
'2023-02-27 14-00-50.mkv'  '2023-03-07 16-15-57.mkv'  '2023-11-21 13-55-35.mkv'  '2024-05-08 10-56-58.mp4'   default-soapui-workspace.xml   Music/                 'VirtualBox VMs'/
'2023-02-28 14-02-55.mkv'  '2023-03-13 14-03-40.mkv'  '2024-04-15 14-33-51.mkv'  '2024-06-03 17-33-55.mp4'   Desktop/                       NetBeansProjects/       vite_grep.log
'2023-03-02 14-06-31.mkv'  '2023-03-22 14-00-11.mkv'  '2024-04-15 14-35-34.mkv'  '2024-06-06 09-58-58.mp4'   Documents/                     Pictures/               zblockChain/

```
Change directory
```bash
❯ cd /home/erick/.config/

```
Remove files
```bash
❯ rm aFile

```
Make and remove folders
```bash
❯ mkdir folder
❯ rmdir emptyFolder

```
### Executing programs
Print path variable 

```bash
❯ echo $PATH
/home/linuxbrew/.linuxbrew/bin /home/linuxbrew/.linuxbrew/sbin /home/erick/.asdf/shims /home/erick/.asdf/bin /home/erick/uni/webServices/pomm/apache-maven-3.9.9/bin /home/linuxbrew/.linuxbrew/opt/postgresql@11/bin /home/erick/.foundry/bin /home/erick/.sdkman/candidates/java/current/bin /home/erick/.sdkman/candidates/groovy/current/bin /home/erick/.sdkman/candidates/gradle/current/bin /home/erick/.cargo/bin /home/erick/.local/bin /usr/local/sbin /usr/local/bin /usr/sbin /usr/bin /sbin /bin /usr/games /usr/local/games /snap/bin
```
List installed packages
```bash
❯ apt list --installed
Listing...
accountsservice/focal-updates,focal-security,now 0.6.55-0ubuntu12~20.04.7 amd64 [installed,automatic]
acl/focal,now 2.2.53-6 amd64 [installed,automatic]
acpi-support/focal,now 0.143 amd64 [installed]
acpid/focal,now 1:2.0.32-1ubuntu1 amd64 [installed,automatic]
adduser/focal,focal,now 3.118ubuntu2 all [installed,automatic]
adwaita-icon-theme-full/focal-updates,focal-updates,now 3.36.1-2ubuntu0.20.04.2 all [installed,automatic]
.
.
.
```
Pipin, direct the outpu of a  command to another command
```bash
❯ ls -al | less
```
### Installing appplications
How do I install applications
```bash
❯ sudo apt update
❯ sudo apt install package_to_install
```
Verify installation
```bash
❯ apt show installed_package
```
### Getting help
Getting help
```bash
❯ man ls
LS(1)                                                                                  User Commands                                                                                  LS(1)

NAME
       ls - list directory contents

SYNOPSIS
       ls [OPTION]... [FILE]...

DESCRIPTION
       List information about the FILEs (the current directory by default).  Sort entries alphabetically if none of -cftuvSUX nor --sort is specified.

       Mandatory arguments to long options are mandatory for short options too.

       -a, --all
              do not ignore entries starting with .
```
### Linux proceses
List running proceses
```bash
❯ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 18:19 ?        00:00:01 /sbin/init splash
root           2       0  0 18:19 ?        00:00:00 [kthreadd]
root           3       2  0 18:19 ?        00:00:00 [rcu_gp]
root           4       2  0 18:19 ?        00:00:00 [rcu_par_gp]
root           5       2  0 18:19 ?        00:00:00 [slub_flushwq]
root           6       2  0 18:19 ?        00:00:00 [netns]
root           8       2  0 18:19 ?        00:00:00 [kworker/0:0H-events_highpri]


```
Start, stop, or check status of services.
```bash
❯ systemctl status rabbitmq-server
● rabbitmq-server.service - RabbitMQ broker
     Loaded: loaded (8;;file://e-pc/lib/systemd/system/rabbitmq-server.service^G/lib/systemd/system/rabbitmq-server.service8;;^G; enabled; preset: enabled)
     Active: active (running) since Wed 2024-10-30 00:20:05 UTC; 46min ago
   Main PID: 1017 (beam.smp)
      Tasks: 39 (limit: 18697)
     Memory: 164.5M
     CGroup: /system.slice/rabbitmq-server.service
             ├─1017 /usr/lib/erlang/erts-14.2.4/bin/beam.smp -W w -MBas ageffcbf -MHas ageffcbf -MBlmbcs 512 -MHlmbcs 512 -MMmcs 30 -pc unicode -P 1048576 -t 5000000 -stbt db -zdbbl 128000 -s>
             ├─1060 erl_child_setup 32768
             ├─1454 sh -s disksup
             ├─1460 /usr/lib/erlang/lib/os_mon-2.9.1/priv/bin/memsup
             ├─1461 /usr/lib/erlang/lib/os_mon-2.9.1/priv/bin/cpu_sup
             ├─1496 /usr/lib/erlang/erts-14.2.4/bin/inet_gethost 4
             ├─1497 /usr/lib/erlang/erts-14.2.4/bin/inet_gethost 4
             └─1509 /bin/sh -s rabbit_disk_monitor

Oct 30 00:20:03 e-pc rabbitmq-server[1017]:   Doc guides:  https://www.rabbitmq.com/docs
Oct 30 00:20:03 e-pc rabbitmq-server[1017]:   Support:     https://www.rabbitmq.com/docs/contact
Oct 30 00:20:03 e-pc rabbitmq-server[1017]:   Tutorials:   https://www.rabbitmq.com/tutorials
.
.
.
```

### Linux log files
View and parse log files
Show contents of a file
```bash
❯ cat CNAME
erickdjm.xyz
```
View a file with pagination and scrolling
```bash
❯ less CNAME
```
Search for a string in a file
```bash
❯ grep PATTERN [FILE]
```
See the first lines (head end) of a text file
```bash
❯ head
```
View the last lines (tail end ) of a text file. A common use case for tail is to wwatch the status of a log fie in real time with the "f" flag like:
```bash
❯ tail -f /var/log/syslog
```
### Users and super users

User with id `1000`, and I am the user `erick`
```bash
❯ id
uid=1000(erick) gid=1000(erick) groups=1000(erick),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),120(lpadmin),132(lxd),133(sambashare),135(docker),136(wireshark),137(vboxusers)

❯ whoami
erick

❯ sudo id
[sudo] password for erick:
uid=0(root) gid=0(root) groups=0(root)

❯ sudo whoami
root
```
### Files and permissions
```bash
❯ ls -l
total 36
drwxrwxr-x 2 erick erick 4096 oct 28 19:20 archetypes/
-rw-rw-r-- 1 erick erick   13 oct 28 19:20 CNAME
```
## Chapter 3
### Understanding Linux Network Interfaces
> Loopback. The loopback (lo) interface will have an IP address of 127.0.0.1, which represents the host itself

> Ethernet. The ethernet 0 (eth0) interface is typically the 
connection to the local network.

Configure network interfaces/devices/links
```bash
❯ ip link
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN mode DEFAULT group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
2: wlp0s20f3: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc noqueue state UP mode DORMANT group default qlen 1000
    link/ether c8:58:c0:c1:86:30 brd ff:ff:ff:ff:ff:ff
3: docker0: <NO-CARRIER,BROADCAST,MULTICAST,UP> mtu 1500 qdisc noqueue state DOWN mode DEFAULT group default
    link/ether 02:42:9d:02:3e:64 brd ff:ff:ff:ff:ff:ff
```
 `ip link set [dev] { up | down }`
 `ip link set lo mtu 1500`

 ### MAC Addresses
 Media access control address is the unique identifier assigned to a network interface at layer 2 -- the Data Link Layer -- of the OSI Model.

 ### IP Addressing

 They are unique on the same network, every device has at least one, adn addresses typically fall  somewhere between 1.1.1.1 and 255.255.255.255  

```bash
❯ ip addr
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
2: wlp0s20f3: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc noqueue state UP group default qlen 1000
    link/ether c8:58:c0:c1:86:30 brd ff:ff:ff:ff:ff:ff
    inet 192.168.1.101/24 brd 192.168.1.255 scope global dynamic noprefixroute wlp0s20f3
       valid_lft 81572sec preferred_lft 81572sec
    inet6 2806:10a6:13:511b:e122:aa52:72c7:9797/64 scope global temporary dynamic
       valid_lft 599973sec preferred_lft 81052sec
    inet6 2806:10a6:13:511b:549a:f3d5:b811:cde1/64 scope global dynamic mngtmpaddr noprefixroute
       valid_lft 2591975sec preferred_lft 2591975sec
    inet6 fe80::3713:2ee:2680:726d/64 scope link noprefixroute
       valid_lft forever preferred_lft forever
3: docker0: <NO-CARRIER,BROADCAST,MULTICAST,UP> mtu 1500 qdisc noqueue state DOWN group default
    link/ether 02:42:9d:02:3e:64 brd ff:ff:ff:ff:ff:ff
    inet 172.17.0.1/16 brd 172.17.255.255 scope global docker0
       valid_lft forever preferred_lft forever
```

Sends out an Internet Control Message Protocol packet across the network and notifies whether the irs a response. If a host is up and able to communicate on the network an ICMP response will be returned.

```bash
❯ ping -c5 192.168.192.196
PING 192.168.192.196 (192.168.192.196) 56(84) bytes of data.
```
Another common Linux network troubleshooting toolis `traceroute`. Probes the network between the local system and a destination, gathering information about each IP router in the path. Is useful when you think there may be a network issue.
```bash
❯ traceroute erickdjm.xyz
traceroute to erickdjm.xyz (185.199.108.153), 30 hops max, 60 byte packets
 1  _gateway (192.168.1.254)  5.209 ms  5.144 ms  5.117 ms
 2  dsl-servicio-l200.uninet.net.mx (200.38.193.226)  5.552 ms  5.526 ms  5.508 ms
 3  172.16.1.1 (172.16.1.1)  5.487 ms * *
 4  bb-la-grand-12-ae44_0.uninet.net.mx (189.246.23.17)  45.113 ms  45.096 ms  45.080 ms
```
### DHCP
*Dynamic host configuration protocol* is commonly used for client systems or devices that don't experience any side effects from a periodically changing IP address. On server systems, administrators either manually configure static IP addresses, or they create what are know as static DHCP reservations that are tied to the MAC address of the network adapter.

Here's how the typical DHCP process works:

1. When a computer starts up, it sends a DHCP request out on 
the network.
2. Assuming a DHCP server is present, a DHCP server responds 
with the IP address configuration for that device. 
3. That IP address is marked as reserved so that it’s not 
accidentally assigned to some other device.

### DNS 

Computers that connect to each other using TCP/IP talk with each other using IP addresses. *Domain name system* (DNS) is used to map IP addresses to names.


Perfomrs verbose DNS lookups and is great for toubleshooting DNS issues.
```bash
❯ dig erickdjm.xyz

; <<>> DiG 9.18.28-0ubuntu0.20.04.1-Ubuntu <<>> erickdjm.xyz
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 43318
;; flags: qr rd ra; QUERY: 1, ANSWER: 4, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 65494
;; QUESTION SECTION:
;erickdjm.xyz.                  IN      A

;; ANSWER SECTION:
erickdjm.xyz.           1799    IN      A       185.199.111.153
erickdjm.xyz.           1799    IN      A       185.199.110.153
erickdjm.xyz.           1799    IN      A       185.199.109.153
erickdjm.xyz.           1799    IN      A       185.199.108.153

;; Query time: 35 msec
;; SERVER: 127.0.0.53#53(127.0.0.53) (UDP)
;; WHEN: Tue Oct 29 20:14:05 CST 2024
;; MSG SIZE  rcvd: 105
```

Enumeraates name service switch files, specifically for host entries.
```bash
❯ getent ahosts
127.0.0.1       localhost
127.0.1.1       e-pc
127.0.0.1       ip6-localhost ip6-loopback
127.0.0.1       kubernetes.docker.internal
```

The name server lookup, or nslookup, performs variety of different DNS server lookups: mail server, reverse lookups.
```bash
❯ nslookup
> erickdjm.xyz
Server:         127.0.0.53
Address:        127.0.0.53#53

Non-authoritative answer:
Name:   erickdjm.xyz
Address: 185.199.109.153
Name:   erickdjm.xyz
Address: 185.199.110.153
Name:   erickdjm.xyz
Address: 185.199.108.153
Name:   erickdjm.xyz
Address: 185.199.111.153
```

Show what active processes are that have the network interface open.
```bash
❯ netstat
Active Internet connections (w/o servers)
Proto Recv-Q Send-Q Local Address           Foreign Address         State
tcp        0      0 localhost:xtel          localhost:40626         ESTABLISHED
tcp        0      0 localhost:xtel          localhost:34374         ESTABLISHED
tcp        0      0 localhost:40642         localhost:xtel          ESTABLISHED
tcp        0      0 e-pc:51974              13.89.179.13:https      ESTABLISHED
tcp        0      0 localhost:34374         localhost:xtel          ESTABLISHED
tcp        0      0 localhost:40288         localhost:epmd          ESTABLISHED
tcp        0      0 e-pc:41384              static.73.91.90.1:https ESTABLISHED

```

## Chapter 4

### Bridging
First we are creating a brife named br0
The two ip link set commands add the two Ethernet onterfaces, eth0 and eth1, to the new bridge resulting in a connection between these two interfaces.
```bash
❯ sudo ip link add br0 type bridge
❯ sudo ip link add eth0 master br0
❯ sudo ip link add eth1 master br0
```
Show current forwarding database management.

```bash
❯ sudo bridge fdb show
[sudo] password for david:
01:00:5e:00:00:01 dev eth0 self permanent
33:33:00:00:00:01 dev eth0 self permanent
33:33:ff:d0:e8:7e dev eth0 self permanent
01:00:5e:00:00:fb dev eth0 self permanent
33:33:00:00:00:fb dev eth0 self permanen 
```

### Neighbor Table
When an IP node wants to communicate with a system in the same layer 2 domain, it looks in its neighbor table, or ARP table, to determine how to construct the Ethernet frame. If the desired destination IP address is not in the neighbor table, the node issues an ARP request, which is broadcast to everyone in the layer 2 domain, that asks, “Please tell me the MAC address for the node with IP address X.X.X.X.” Assuming the target device is available, the node with that IP address will respond. In Linux, you view (and manipulate) the Neighbor table using the ip neighbor show
```bash
❯ ip neigh show
172.20.10.2 dev eth0 lladdr ac:bc:32:9c:a6:3b REACHABLE
172.20.10.1 dev eth0 lladdr 72:70:0d:4c:6b:64 STALE
```

### IP Routing

You can view the routing table with:

```bash
❯ ip route show
default via 172.20.10.1 dev eth0 proto static metric 
1024
172.20.10.0/28 dev eth0 proto kernel scope link src 
172.20.10.10
```

Create a static route  to router 192.168.1.1 through the eth1 interfaces, we would use the **ip route** command:
```bash
❯ ip route add default via 192.168.1.1 dev eth1
```
### Virtual LANs (VLANs)
Configures VLANs on a Linux system by setting up a bridge (br0) with VLAN filtering and adding interfaces to manage tagged and untagged traffic. The 8021q module is loaded to enable VLAN tagging, and the bridge br0 is created to handle VLAN assignments. eth1 is assigned to VLAN 11 and eth3 to VLAN 12, both set to handle untagged traffic. eth2 is made a member of both VLANs (11 and 12), allowing it to route tagged frames across them. Finally, all interfaces are activated, enabling VLAN-based traffic segmentation across the specified Ethernet ports.
```bash
❯ sudo modprobe 8021q
❯ sudo ip link add br0 type bridge vlan_filtering 1
❯ sudo ip link set eth1 master br0
❯ sudo ip link set eth2 master br0
❯ sudo ip link set eth3 master br0
❯ sudo bridge vlan add dev eth1 vid 11 pvid untagged 
❯ sudo bridge vlan add dev eth3 vid 12 pvid untagged 
❯ sudo bridge vlan add dev eth2 vid 11
❯ sudo bridge vlan add dev eth2 vid 12 
❯ sudo ip link set up dev br0
❯ sudo ip link set up dev eth1
❯ sudo ip link set up dev eth2
❯ sudo ip link set up dev eth3
```

Check the status of the bridge links
```bash
❯ bridge link show 
```

Check the status of the VLANs tranversing the bridge
```bash
❯ bridge vlan show
```
View the forwarding database
```bash
❯ bridge fdb show
```

This setup connects two Linux systems over a VXLAN (Virtual Extensible LAN) tunnel, creating a virtual Layer 2 network between them. On each system, a bridge (br0) is created with VLAN filtering, and a VLAN interface (vlan10) is added with an IP in the 10.0.0.x/24 subnet. A VXLAN Tunnel Endpoint (VTEP) interface (vtep10) is configured on each host, specifying the VXLAN ID (1010) and local and remote IP addresses, allowing encapsulated traffic to traverse between hosts transparently. The interface eth1 is added to the bridge, set to VLAN 10 with untagged traffic, enabling the two Linux systems to communicate as if on the same local network.
> Linux System 1
```bash
❯ sudo ip link add br0 type bridge vlan_filtering 1
❯ sudo ip link add vlan10 type vlan id 10 link bridge 
protocol none
❯ sudo ip addr add 10.0.0.1/24 dev vlan10
❯ sudo ip link add vtep10 type vxlan id 1010 local 
10.1.0.1 remote 10.3.0.1 learning
❯ sudo ip link set eth1 master br0
❯ sudo bridge vlan add dev eth1 vid 10 pvid untagged 
```

> Linux System 1

```bash
❯ 
❯ sudo ip link add br0 type bridge vlan_filtering 1
❯ sudo ip link add vlan10 type vlan id 10 link bridge 
protocol none
❯ sudo ip addr add 10.0.0.2/24 dev vlan10
❯ sudo ip link add vtep10 type vxlan id 1010 local 
10.3.0.1 remote 10.1.0.1 learning
❯ sudo ip link set eth1 master br0
❯ sudo bridge vlan add dev eth1 vid 10 pvid untagged
```

## Chapter 5
Instead of trying to administer a Linux-powered network with hundreds 
of command and configuration files, Cumulus Linux includes a 
command line utility as part of the NCLU package that is invoked by 
the net command to provide a consistent and helpful user interface.
```bash
❯ net help
.
 #
 # COMMANDS are listed below and have context 
specific arguments which can
 # be explored by typing "<TAB>" or "help" anytime 
while using net.
 #
 # Use 'man net' for a more comprehensive overview.
 net abort
 net commit [verbose] [confirm] [description 
<wildcard>]
 net commit delete (<number>|<number-range>)
 net commit permanent <wildcard>
 net del all
 net help [verbose]
 net pending [json]
 net rollback (<number>|last)
 net rollback description <wildcard-snapshot>
 net show commit (history|<number>|<numberrange>|last)
 net show rollback (<number>|last)
 net show rollback description <wildcard-snapshot>
 net show configuration 

```

### Building better bridge
One of the most basic networking use cases is a single transparent bridge. In our example, we’ll put the interfaces named swp1, swp2, and swp3 into a transparent bridge with swp3 connecting back into our layer 2 bridge infrastructure.
```bash
❯ net add bridge bridge ports swp1,swp2,swp3
❯ net commit
```
### Two Links Are better than one

This command sequence configures a Multi-Chassis Link Aggregation (MLAG) setup to ensure redundancy and high availability for server connections in a network. In this setup, two switches work together to appear as a single logical unit to connected servers, enabling redundancy at both link and switch levels. The command net add clag peer sys-mac designates a shared MAC address for MLAG communication, while swp5 and swp6 are configured as peer links, which are essential for the two switches to sync state information. VLANs 100-199 are added to trunk traffic between the switches and servers. The command net add clag port bond is used to create bonded connections to core network switches (bond-to-spines) and to servers (host-01 and host-02), with unique clag-id identifiers for each connection. Finally, net commit applies these configurations, ensuring resilient connectivity and load balancing across the network paths.
```bash
❯
❯ net add clag peer sys-mac 44:38:39:FF:00:01 interface 
swp5,swp6 primary
❯ net add vlan 100-199
❯ net add clag port bond bond-to-spines interface swp3-4 
clag-id 500
❯ net add clag port bond host-01 interface swp1 clag-id 
1
❯ net add clag port bond host-02 interface swp1 clag-id 
2
❯ net commit
```
In this configuration, an IP fabric is created using a leaf-spine topology, ideal for modern data centers to handle high-speed, low-latency, layer 3 (IP routed) traffic flows. The leaf switch is set up to use BGP unnumbered on interfaces connected to spine switches (swp5-8), enabling automatic address assignments and streamlined connectivity without assigning specific IP addresses on each link. BGP advertisements are used to propagate reachability for the leaf’s IP subnets (10.0.0.0/24 and 10.1.0.1/32) across the network, ensuring efficient routing. Commands initialize BGP for Autonomous System (AS) 65001, add a loopback IP (for device identification), assign VLAN 1 with an IP address, and configure a bridge over ports swp1-4 for local connectivity. Finally, net commit applies these settings, creating a scalable, robust IP fabric with simplified configuration across the network infrastructure.
```bash
❯ net add bgp autonomous-system 65001
❯ net add loopback lo ip address 10.1.0.1/32
❯ net add bgp ipv4 unicast network 10.1.0.1/32
❯ net add vlan 1 ip address 10.0.0.1/24
❯ net add bgp ipv4 unicast network 10.0.0.1/24
❯ net add bgp neighbor swp5-8 interface remote-as 
external
❯ net add bgp ipv4 unicast neighbor swp5-8 activate
❯ net add bridge bridge ports swp1-4
❯ net commit 
```

In this setup, BGP EVPN (Ethernet Virtual Private Network) enables layer 2 peering across a layer 3 IP fabric, ideal for applications that need layer 2 connectivity, like VMware's vMotion, within a highly scalable layer 3 network. Here, BGP EVPN advertises learned MAC addresses across the network, allowing each leaf switch to forward layer 2 traffic directly to the appropriate VTEP (Virtual Tunnel Endpoint) without relying on traditional flooding methods or spanning tree protocols. The configuration assigns Autonomous System (AS) 65001, sets up loopback and VLAN IP addresses, and establishes a tagged VLAN (VLAN 100) with a VTEP for layer 2 connectivity. Commands enable VLAN 100 across interfaces swp1-4 and configure BGP unnumbered on spine connections (swp5-8), facilitating routing and advertising reachability. With these settings, BGP EVPN broadcasts VLAN 100's availability across the network, ensuring seamless layer 2 and layer 3 integration within the IP fabric.

```bash
❯ net add bgp autonomous-system 65001
❯ net add loopback lo ip address 10.1.0.1/32
❯ net add bgp ipv4 unicast network 10.1.0.1/32
❯ net add vlan 1 ip address 10.0.0.1/24
❯ net add bgp ipv4 unicast network 10.0.0.1/24
❯ net add interface swp1-4 bridge trunk vlans 100
Cumulus Linux 93 
❯ net add vxlan vtep100 vxlan id 100
❯ net add vxlan vtep100 vxlan local-tunnelip 10.1.0.1
❯ net add vxlan vtep100 bridge access 100
❯ net add vxlan vtep100 bridge learning off
❯ net add vxlan vtep100 mtu 9216
❯ net add bgp neighbor swp5-8 interface remote-as
external
❯ net add interface swp5-8 mtu 9216
❯ net add bgp neighbor swp5-8 interface remote-as 
external
❯ net add bgp ipv4 unicast neighbor swp5-8 activate
❯ net add bgp evpn neighbor swp5-8 activate
❯ net add bgp evpn advertise-all-vni
❯ net commit 
```

In chapters 1 through 5 of the Cumulus Networks book, the foundation for modern network architecture and best practices in data center networking is thoroughly established. The book begins with essential networking concepts and progressively introduces key topics such as layer 2 and layer 3 design principles, VLANs, MLAG (Multi-Chassis Link Aggregation) for redundancy, and the growing preference for IP-based fabrics over traditional broadcast domains. It then explores advanced network virtualization techniques with BGP EVPN, showing how BGP can facilitate both IP routing and layer 2 overlays, providing scalable and efficient connectivity. The focus on high-performance, resilient, and scalable networks—especially suited for data centers—underscores the shift towards simplified management and automation in networking. By the end of these chapters, readers are equipped with the core principles and practical configurations needed to design robust, flexible networks that can adapt to dynamic data center demands, from minimizing latency in leaf-spine architectures to using VXLAN and BGP for network virtualization.