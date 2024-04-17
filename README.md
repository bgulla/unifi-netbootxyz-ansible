# unifi-netbootxyz-ansible
```
#  _   _ ____  __  __     __  ____   _______
# | | | |  _ \|  \/  |    \ \/ /\ \ / /__  /
# | | | | | | | |\/| |_____\  /  \ V /  / /
# | |_| | |_| | |  | |_____/  \   | |  / /_
#  \___/|____/|_|  |_|    /_/\_\  |_| /____|
#
```

This is a helper ansible-playbook to configure multi-arch/bios support for `netboot.xyz` on Unifi/UDM-OS devices such as the UDM Pro. Note: this playbook will need to be run on every UDM reboot, so throw it in a cron or setup jobs with `Ansible Semaphore`.

## Prereqs
* SSH enabled on your unifi-os device
* ansible installed
* SSH Public Key authentication. If you do not have this enabled (shame), you can yolo it and place the UDM root password in your inventories file with the added parameter `ansible_ssh_pass=<>`

## Steps
1) Clone this repository
2) edit the `./hosts.ini`, replace with the ip address of your UDM device.
3) edit the playbook.yml file to include the IP address of your `netboot.xyz` file.
4) run: `ansible-playbook -i ./hosts.ini ./playbook.yml`
5) `profit`

## References
* https://community.ui.com/questions/PXE-Network-boot-UDM-SE-Serving-files-conditionally-based-on-architecture/1843fcf6-87d5-4305-bc1d-4e55619ebb10 
* https://technotim.live/posts/netbootxyz-tutorial/ 