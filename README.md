# metacloud-devstack-deb8-context
Contex pro template do metacentricka ON, ktery obsahuje mimo jine cast pro cloud-init, ktery by mel nastavit devstack


Do CONTEXT=[ .... USERDATA_ENCODING="base64",USER_DATA="",...] pridat do USER_DATA vystup z  `cat context.txt|base64 -w 0`
