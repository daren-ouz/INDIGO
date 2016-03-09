ONe_install
-----------

Script creating ONe 4.14 applience on Debian 8. Creates also rOCCI accounts. Sets default password for oneadmin, however is should be changed.

Supposed to be run via cloudinit as:

runcmd:
- cd /var/tmp
- wget https://raw.githubusercontent.com/daren-ouz/metacloud-devstack-deb8-context/master/ONe_install
- bash /var/tmp/ONe_install

power_state:
- mode: reboot


rOCCI_install
-------------

Script creating rOCCI appliance on Debian 8. Takes ONe endpoint as a parameter. Uses account/password created in ONe applience as a default, however, may be customized to use any ONe installation. 

Supposed to be run via cloudinit as:

runcmd:
- cd /var/tmp
- wget https://raw.githubusercontent.com/daren-ouz/metacloud-devstack-deb8-context/master/ONe_install
- bash /var/tmp/rOCCI_install HERE_PUT_ONe_HOSTNAME

power_state:
- mode: reboot


ONe_install_CentOS7
-------------------

Script (NOT COMPLETED YET!) creating FedCloud applience on CentOS 7. 

- supports    : ONe, rOCCI, Perun
- in progress : vmcatcher, oneacct, BDII (for more details see GGUS 119768)

Supposed to be run via cloudinit as:

runcmd:
- cd /var/tmp
- wget https://raw.githubusercontent.com/daren-ouz/metacloud-devstack-deb8-context/master/ONe_install_CentOS7
- bash /var/tmp/ONe_install_CentOS7

power_state:
- mode: reboot
