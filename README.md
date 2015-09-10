

context-devstack-meta.txt
-------------------------

Kontext pro template do metacentricka ON, ktery obsahuje mimo jine cast pro cloud-init, ktery nastavuje devstack.

Do CONTEXT=[ .... USERDATA_ENCODING="base64",USER_DATA="",...] pridat do USER_DATA vystup z  `cat context.txt|base64 -w 0`

Funguje pro template 2890 (Copy of METACLOUD-Ubuntu-14.04-x86_64 with devstack context).
Instanci z templatu 2887 (Copy of METACLOUD-Debian-8.1.0-x86_64 with devstack context), je treba po dobehnuti nasilne rebootovat, nedobehne tam koreknte shutdown.



context-ON-meta.txt
-------------------

Kontext pro template do metacentricka ON, ktery obsahuje mimo jine cast pro cloud-init, ktery nastavuje ON sandbox. 

Funguje 2918 (Copy of METACLOUD-Debian-8.1.0-x86_64 with ON sandbox context)




context-rOCCI-meta.txt
----------------------

Kontext pro template do metacentricka ON, ktery obsahuje mimo jine cast pro cloud-init, ktery nastavuje rOCCI sandbox.

Funguje 2920 (Copy of METACLOUD-Debian-8.1.0-x86_64 with rOOCI sandbox)



ONe_install
-----------

Script instalujici ONe 4.14 do Debian 8. Vytvari ucty pro rOCCI. Nastavuje defaultni heslo pro onedamin, 
ktere je nasledne vhodne zmenit. Predpokladane pouziti z cloud-initu:

runcmd:
- cd /var/tmp
- wget https://raw.githubusercontent.com/daren-ouz/metacloud-devstack-deb8-context/master/ONe_install
- bash /var/tmp/ONe_install



rOCCI_install
-------------

Script instalujici rOCCI do Debian 8. Jako parametr vyzaduje endpoint ONe. Pouziva ucty/hesla vytvorene
v ONe_install, pri pouziti s jinou ON je treba je upravit. Predpokladane pouziti z cloud-initu:

runcmd:
- cd /var/tmp
- wget https://raw.githubusercontent.com/daren-ouz/metacloud-devstack-deb8-context/master/ONe_install
- bash /var/tmp/rOCCI_install HERE_PUT_ONe_HOSTNAME

