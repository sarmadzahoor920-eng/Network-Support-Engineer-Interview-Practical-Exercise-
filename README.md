# Network-Support-Engineer-Interview-Practical-Exercise-

## Steps Taken to Complete the Task

- Installed Oracle VirtualBox, downloaded the MikroTik CHR (ISO/VDI) image, deployed it in VirtualBox, ensured the MikroTik CHR was        running, then downloaded Winbox on the desktop, accessed MikroTik via Winbox, and configured a basic firewall rule for secure            management access.

- Installed Ubuntu 22.04 LTS and Ansible (version 2.17).

- Configured network connectivity and enabled SSH access on the MikroTik CHR.

- Created an Ansible inventory file (hosts) with the required connection parameters.

- Installed the community.routeros Ansible collection.

- Created an Ansible playbook (RADIUS.yml) to add a RADIUS client on MikroTik with:

- RADIUS Server Address: 35.227.71.209

- Secret: testing123

- Service: hotspot

- Executed the playbook and verified that the RADIUS client was successfully added.

- Added a second network interface (ether2) in VirtualBox.

- Configured the Hotspot feature on ether2 using Winbox.

- Verified Hotspot operation and RADIUS configuration.

- Exported the MikroTik configuration to a file named chr.rsc.

- Organized all Ansible files, configuration exports, screenshots, and documentation in a GitHub repository.


## Challenges Encountered

-  While accessing MikroTik via Winbox, a network connectivity issue was encountered due to the network adapter being set to NAT instead    of Bridged Adapter in VirtualBox. This was resolved by changing the adapter mode to Bridged, allowing proper network access to the       MikroTik CHR.
- SSH host key verification errors when connecting to Mikrotik for the first time.
- Compatibility issues with older Ansible versions during initial testing.
- Understanding RouterOS CLI behavior (commands such as `exit` not working as expected).

These issues were resolved by upgrading Ansible to version 2.17, accepting the SSH host key, and using Winbox for easier RouterOS configuration.


## References and Resources

- Ansible Documentation: https://docs.ansible.com
- Mikrotik RouterOS Documentation: https://help.mikrotik.com
- Ansible Galaxy – community.routeros: https://galaxy.ansible.com/community/routeros
- VirtualBox Documentation: https://www.virtualbox.org/wiki/Documentation
