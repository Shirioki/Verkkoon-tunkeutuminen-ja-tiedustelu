# h1 Sniff

x) Wireshark article contains introduction on how to install wireshark and do our first Sniff.
  - Add user to a group
  - Saving and loading packets
  - Filters commands

  - Linux network interfaces are named by systemd
    - en = Ethernet
    - wl = Wifi
    - lo = loopback adapter
  - Common network interface names
    - wlp4s0 = WiFi card
    - enp1s0 = Wired ethernet card
    - enx738899738899 = Wired ethernet card, after x is MAC number

a) Debian installed. 

b) You can shutdown and turn up ur Internet connection with commands sudo ip link set enp0s3 down / sudo ip link set enp0s3 up

c) <img width="842" alt="Screenshot 2025-04-01 at 18 02 27" src="https://github.com/user-attachments/assets/a1e1d533-4446-4f56-8c9b-1437c49c0534" />

d) ## Oikeesti TCP/IP.

<img width="822" alt="image" src="https://github.com/user-attachments/assets/554b8319-a41b-40c7-8918-383348953349" />


- Internet layer is IPv6 (Source & Destination IPs)
- Application layer is HTTP (Port 80)
- Transport layer is TCP (Ports (51738 → 80))
- Link Layer is Ethernet II that can be seen in MAC address
