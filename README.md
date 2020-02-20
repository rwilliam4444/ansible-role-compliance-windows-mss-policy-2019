# Role Name:
- ansible-role-compliance-windows-mss-policy-2019

# Description:
This MSS Policy Role was based off the CIS specs for 2019 servers.   This role
covers the "MSS" CIS section only. The checks and remediation commands are for
local settings only. Group Policy settings may override these settings. When the
 "remediate" variable is set to "YES", the role will try to remediate the
server's setting(s) according to the CIS standards.  The defaults/main.yml file
can be used to disable specific CIS items (i.e. "execute_<cis task #>") from
executing. The default value in the defaults/main.yml for these CIS item
variables (i.e. "execute_<cis task #>") is set to "YES". The value "YES" means
that the CIS item will execute at run time. Set the value to "NO" if you want to
skip this CIS item in question from executing.

# Requirements:
Windows Ansible related pre-requisites

# Role Variables:
# defaults file for ansible-role-compliance-windows-mss-policy-2019

Parameter | Choices/Defaults|Comments
----------|-----------------|--------
__remediate__ |"NO"| remediation flag
__AutoAdminLogon_cis__ |"0"| CIS value
__DisableIPSourceRouting_cis__ |"2"| CIS value
__DisableIPSourceRouting2_cis__ |"2"| CIS value
__EnableICMPRedirect_cis__ |"0"| CIS value
__KeepAliveTime_cis__ |300000| CIS value
__NoNameReleaseOnDemand_cis__ |"1"| CIS value
__PerformRouterDiscovery_cis__ |"0"| CIS value
__SafeDllSearchMode_cis__ |"1"| CIS value
__ScreenSaverGracePeriod_cis__ |5| CIS value
__TcpMaxDataRetransmissions_cis__ |3| CIS value
__TcpMaxDataRetransmissions2_cis__ |3| CIS value
__WarningLevel_cis__ |90| CIS value


# Example Playbook:
---
 - hosts: [win]
   roles:
   - ansible-role-compliance-windows-mss-policy-2019


# Author Information
Richard M. Williams (williamsitv@yahoo.com)
