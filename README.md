# NDFC interface policy bulk modifier

The goal of this Python script is to alleviate the process of doing a bulk modification of the freeform config in Cisco NDFC access and trunk interface policies (based on "int_trunk_host" and "int_access_host" templates)

How to use: 

 - Before execution make sure to modify the variables at the beggining of the script, to match your specific environment.
 - Run "python3 script.py" from a computer with reachability to Nexus Dashboard.


Note:  This script can also be used as a workaround in case of hitting [CSCwe98453](https://bst.cisco.com/bugsearch/bug/CSCwe98453)

*****

Caveats / To-Do

 - The script takes care of removing only "ttag" and "ttag-strip" CLI config from server ports (not fabric ports) configured based on templates "int_trunk_host" and "int_access_host". Other types of interface types, like Port-Channels or virtual Port-Channels are not modified in the current release.
