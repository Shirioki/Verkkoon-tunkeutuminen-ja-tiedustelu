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

With the filter command

dns.qry.name 

we can see that the user have visited www.terokarvinen.com and google.com

<img width="1080" alt="image" src="https://github.com/user-attachments/assets/506e5ee5-f14d-45db-9f17-3996612ebfcc" />

## i) Analyysi
I opened Wireshark and chose enp0s3 as my network. We can see in my screenshot there are TCP- TLS-packets in IPv6 Network

- Protocols are TCP and TLSv1.3
- Source Port is 43000 and Destination port 443 (HTTPS)
- We can also see Source IP and Destination IP from the chart
  
What happens here is that my computer (source port 4300) wants to connect to a server (port 443). It sends a packet to the server and server send a packet back and the connection is created. After this the TLSv1.3 protocol start encrypting. My computer sends a "Client Hello" message, with supported encryption methods and the server replies back "Server Hello, Change Cipher Spec" message. After this all communication becomes encrypted.

<img width="1091" alt="image" src="https://github.com/user-attachments/assets/cc2554a2-f8e1-4fb4-884f-15cfc03e5ebd" />


## References

Karvinen 2025: Verkkoon tunkeutuminen ja tiedustelu
https://terokarvinen.com/verkkoon-tunkeutuminen-ja-tiedustelu/

Wireshark Q&A: Filter to display DNS queries https://osqa-ask.wireshark.org/questions/55754/whata-a-display-filter-that-matches-dns-queries-for-a-particular-host-name/

Karvinen 2025: Wireshark - Getting Started https://terokarvinen.com/wireshark-getting-started/

Karvinen 2025: Network Interface Names on Linux https://terokarvinen.com/network-interface-linux/

Karvinen 2024: Install Debian on Virtualbox - Updated 2024 https://terokarvinen.com/2021/install-debian-on-virtualbox/

Wikipedia: Internet protocol suite https://en.wikipedia.org/wiki/Internet_protocol_suite



