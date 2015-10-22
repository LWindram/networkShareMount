# networkShareMount

This script allows for the mounting of network shares using the SMB protocol.  It does attempt to mount all shares available to any user, so it is not appropriate in an environment where failed access attempts are monitored.

Built in kerberos checking and re-enabling.  AD is queried for SMB home  each time the script is run; if not accessible, the script will use two files written to the users home directory to ascertain the last used home.  These are overwritten each time the script is able to browse AD. 

The script can optionally add folders to the finder sidebar - if enabled, the script is dependent on sidebar.py, located at https://github.com/matt4836/changeSidebarLists/blob/master/Change_Sidebar_List.py
