# CESNET appliances

In this reporitory, CESNET appliances created in INDIGO project are stored. There are older ones written for Debian 8 and newer ones written for Centos 7. All appliances install only simple one-host environment where all the components coexist together - this is maily for sake of simplicity (minimum firewall, configuration and orchestration issues).

---

## ONEDock_testbed_install

ONEDock testbed appliance on CentOS 7. 

- bricks    : ONe, rOCCI, ONEDock

Supposed to be run via cloudinit as:

runcmd:
- cd /var/tmp
- yum install -y wget
- wget https://raw.githubusercontent.com/daren-ouz/INDIGO/master/ONEDock_testbed_install
- bash /var/tmp/ONEDock_testbed_install

power_state:
- mode: reboot



## FedCloud_install

FedCloud appliance on CentOS 7. 

- bricks    : ONe, rOCCI, Perun, oneacct, BDII
- in progress : vmcatcher

Supposed to be run via cloudinit as:

runcmd:
- cd /var/tmp
- yum install -y wget
- wget https://raw.githubusercontent.com/daren-ouz/INDIGO/master/FedCloud_install
- bash /var/tmp/FedCloud_install

power_state:
- mode: reboot



## FedCloud_on_ONe5_install

FedCloud appliance on CentOS 7. 

- bricks    : ONe5
- in progress : rOCCI, Perun, oneacct, BDII, vmcatcher

Supposed to be run via cloudinit as:

runcmd:
- cd /var/tmp
- yum install -y wget
- wget https://raw.githubusercontent.com/daren-ouz/INDIGO/master/FedCloud_on_ONe5_install
- bash /var/tmp/FedCloud_on_ONe5_install

power_state:
- mode: reboot




## ONe_install_CentOS7

Script (NOT COMPLETED YET!) creating FedCloud appliance on CentOS 7. 

- supports    : ONe, rOCCI, Perun
- in progress : vmcatcher, oneacct, BDII (for more details see GGUS 119768)

Supposed to be run via cloudinit as:

runcmd:
- cd /var/tmp
- yum install -y wget
- wget https://raw.githubusercontent.com/daren-ouz/INDIGO/master/ONe_install_CentOS7
- bash /var/tmp/ONe_install_CentOS7

power_state:
- mode: reboot



## ONe_install

Script creating ONe 4.14 appliance on Debian 8. Creates also rOCCI accounts. Sets default password for oneadmin, however is should be changed.

Supposed to be run via cloudinit as:

runcmd:
- cd /var/tmp
- yum install -y wget
- wget https://raw.githubusercontent.com/daren-ouz/INDIGO/master/ONe_install
- bash /var/tmp/ONe_install

power_state:
- mode: reboot



## rOCCI_install

Script creating rOCCI appliance on Debian 8. Takes ONe endpoint as a parameter. Uses account/password created in ONe appliance as a default, however, may be customized to use any ONe installation. 

Supposed to be run via cloudinit as:

runcmd:
- cd /var/tmp
- yum install -y wget
- wget https://raw.githubusercontent.com/daren-ouz/INDIGO/master/rOCCI_install
- bash /var/tmp/rOCCI_install HERE_PUT_ONe_HOSTNAME

power_state:
- mode: reboot



