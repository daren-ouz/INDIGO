# metacloud-devstack-context
Contex pro template do metacentricka ON, ktery obsahuje mimo jine cast pro cloud-init, ktery nastavuje devstack


Do CONTEXT=[ .... USERDATA_ENCODING="base64",USER_DATA="",...] pridat do USER_DATA vystup z  `cat context.txt|base64 -w 0`

Funguje pro template 2890 (Copy of METACLOUD-Ubuntu-14.04-x86_64 with devstack context).
Instanci z templatu 2887 (Copy of METACLOUD-Debian-8.1.0-x86_64 with devstack context), je treba po dobehnuti nasilne rebootovat, nedobehne tam koreknte shutdown.
