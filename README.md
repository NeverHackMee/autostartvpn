# autostartvpn - https://www.neverhackme.com/autostart-openvpn/

![AutoStart-OpenVPN-1](https://user-images.githubusercontent.com/96632840/195457136-182c9378-942c-406d-b1c1-2429c740ebe3.jpeg)

autostartvpn command that will allow you to start and stop the connection to Hack The Box through Openvpn automatically.

This script must be added to your /usr/bin/ path to run it as a normal Linux command.

The script receives only one parameter through which to specify the type of VPN to start:

* -M Run the Machines VPN
* -S Run the StartingPoint VPN
* -E Run the EndGames VPN
* -F Run the Fortresses VPN
* -R Run the Release Arena VPN
* -stop Stop all the VPN instances
* –help Run the helpPanel”

Remember, before running it, make sure you have entered the path corresponding to each Hack The Box ovpn file in the global variables section.

The runvpn function allows you to automatically start your vpn instance, and shows you the IP associated to your tun0 interface corresponding to your VPN.

The stopvpn function (–stop param) allows you to stop all previously executed processes to prevent further network interfaces from being spawned like tun1, tun2 etc. This function is called too by runvpn function when a previous interface is running, so you don’t have to worry about stopping the previous instance.
