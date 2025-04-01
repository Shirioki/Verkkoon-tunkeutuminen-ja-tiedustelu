# h1 Sniff

## x) Read and summaries
Wireshark article contains introduction on how to install wireshark and do our first Sniff.
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

## a) Debian installed. 

## b) Ei voi kalastaa
You can shutdown and turn up ur Internet connection with commands sudo ip link set enp0s3 down / sudo ip link set enp0s3 up

## c) Wireshark

<img width="842" alt="Screenshot 2025-04-01 at 18 02 27" src="https://github.com/user-attachments/assets/a1e1d533-4446-4f56-8c9b-1437c49c0534" />

## d) Oikeesti TCP/IP.

<img width="822" alt="image" src="https://github.com/user-attachments/assets/554b8319-a41b-40c7-8918-383348953349" />

- Internet layer is IPv6 (Source & Destination IPs)
- Application layer is HTTP (Port 80)
- Transport layer is TCP (Ports (51738 → 80))
- Link Layer is Ethernet II that can be seen in MAC address

## e) Mitä tuli surffattua?

In this exercise we had to examine surfing-secure.pcap and describe what kind of capture it is. When clicking on "Statistics" menu on the "Endpoints" tab you can see two IP addresses in the capture, meaning there is traffic between two devices

<img width="631" alt="image" src="https://github.com/user-attachments/assets/d250c376-5b5d-47c5-ae70-71e6ae4e703b" />

There is over 283 packets that are TCP, TLS and DNS packets. In "Statistics" menu under "Capture file Properties" you can see the time span, speed and packet size 

<img width="696" alt="image" src="https://github.com/user-attachments/assets/146b68b2-d764-4469-9130-4449a8f1f408" />

## g) Minkä merkkinen verkkokortti käyttäjällä on?

<img width="748" alt="image" src="https://github.com/user-attachments/assets/5636230d-30a0-4997-9a02-3fe6d8e9731e" />

We can see that under Ethernet II the Network card is Realtek

## h) Millä weppipalvelimella käyttäjä on surffaillut?






