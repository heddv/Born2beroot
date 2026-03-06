*This project has been created as part of the 42 curriculum by kislamov.*

# Description
The project consists of setting up a server while following specific requirements, such as creating at least 2 encrypted partitions using LVM, implementing a strong password policy and configuring sudo following strict rules.

# Project structure
```bash
tree
```

- `monitoring.sh` is a script that contains all the commands used to display information about our virtual machine every 10 minutes (using crontab).

- `signature.txt` contains the signature of our machine.

> ⚠️ **Note :** shut down the machine and run the following command: `shasum machinename.vdi`, it will display the machine's signature.  
After obtaining the signature, do not start the machine again, as the signature will change.

# Instructions
To create a VM, first download Debian.
Then Virtual Box (or any equivalent software), click on "New", and configure the virtual machine. Then attach the Debian ISO file to the virtual machine. Once everything is set up, start the VM. A terminal will appear, which means that the machine is ready to be configured.

### Useful commands
- `lsblk` : displays information about block devices and encrypted partitions.

# Resources
To better understand the many bash commands and their specific purposes, AI was used to help deepen our understanding whenever an issue was encountered.

Other resources :
- Tutorial on [Youtube](https://www.youtube.com/watch?v=JGuJaj9pths)
- Documentation [debian instalation](https://goopensource.fr/debian-installation-sans-interface-graphique/)
- Setting strong [password policy](https://www.server-world.info/en/note?os=Debian_10&p=password)
- SELinux vs AppArmor [comparaison](https://www.explinux.com/2023/01/apparmor-vs-selinux-quick-comparision.html)
- UFW vs firewalld [comparaison](https://dev.to/salamilinux/simple-firewall-with-ufw-or-firewalld-i9d)
- VirtualBox vs UTM [comparaison](https://www.howtogeek.com/virtualbox-vs-utm-which-is-best-for-linux-vms-on-mac/)

# Project Description
I already work with Debian and it is beginner-friendly, which is why i think it is a better choice.

- `Debian vs Rocky Linux` : Debian is easier and has a large community with many forums, tutorials, and resources available. It is known for its stability.  
Rocky is compatible with RHEL and provides an enterprise-level operating system.
- `AppArmor vs SELinux` : Both AppArmor and SELinux are Linux security modules that restrict what programs can do on the system after they start running.  
The difference is that SELinux is very powerful but complex to use and relies on policies to define what actions are allowed on the system.  
AppArmor is easier to configure and use, but it is less flexible because it relies on path-based access control.
- `UFW vs firewalld` : A firewall controls incoming and outgoing network traffic, protecting the system from unauthorized access. It can define which ports are open or closed and which IP addresses can connect. Without it, the system is more vulnerable to attacks.  
UFW is simpler and better for basic setups, while firewalld is more dynamic and commonly used in enterprise environments.
- `VirtualBox vs UTM` : They are both virtualization tools used to run virtual machines. UTM is lightweight and faster but has fewer graphical features, while Virtualbox is slower but easier to learn and offers features such as snapshots, which allow you to save the state of a VM.