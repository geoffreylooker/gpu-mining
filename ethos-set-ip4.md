# Setting a Static Internal IP for your ethOS Rig 
---------------------------------------------------
### In some cases, you may want to assign a static IP to your ethOS rig. It is recommended to assign static IPs based on mac addresses on your router. However, you can also set a static IP on linux itself:

#### Make changes to your interfaces using this as a guide. 

#### in /etc/network/interfaces change: 
        auto eth0
        iface eth0 inet dhcp 
        
#### to: 
        auto eth0
        iface eth0 inet static
           address 192.168.1.20
           netmask 255.255.255.0
           network 192.168.1.0
           gateway 192.168.1.1
           dns-nameservers 8.8.8.8 
           
        Reboot your rig.

        NOTE: Set the IP according to your correct IP range, outside of your DHCP range. 
