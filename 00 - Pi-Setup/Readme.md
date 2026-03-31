00 - Pi- Setup

//Operating System//
- Raspberry Pi OS (64-bit) — Debian GNU/Linux 13 (trixie).
- Headless — no desktop environment.
- Confirmed 64-bit: `uname -m` returns `aarch64`.


//Imager Settings//
- Hostename `Hostname`.
- Username `Username`.
- SSH: enabled with password authentication.
- Wifi: Configured - Switching to ethernet soon.
- Raspberry Pi Connect: Disabled to avoid third party relay.

//First time connecting//
- Gained secure shell from windows command prompt using the following commands:
```ssh username@hostname```.

//First commands//
- Upgrading all packages on the base OS:
```sudo apt update && sudo apt upgrade -y```.

- Check disk space:
```df -h```.
 
//Network//
- Static IP reserved via router DHCP binding.
- IP: 'IP Address'.
- MAC: 'MAC Address' (wlan0).
- Currently on WiFi — ethernet preferred long term.


//Mistakes//
I flashed pi os desktop version not the lite version. I reflashed with lite. 
When trying to ssh to my homelab I received an error. 
When I reflashed Pi had a new host key but my laptop stored the older one in memory. 

To fix this i ran the following command: 

```ssh-keygen -R My Hostname```.

This command removes the old host key from known hosts. 

//Total time on setup//
~4/5 Hours including OS reflash and troubleshooting. 
