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

# Project Description
I already work with Debian system and it's beginner friendly which is why i think it is a better choice.

- **Debian vs Rocky Linux :** Debian is more reliable and has a lot of packages, while Rocky is a clone of RHEL.
- **AppArmor vs SELinux :** SELinux is very strong but is coplex to use, whereas AppArmor is easier but is less flexible.
- **UFW vs firewalld :**
- **VirtualBox vs UTM :**