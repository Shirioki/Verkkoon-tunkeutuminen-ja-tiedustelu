# h2: Lempiväri: violetti

## x) Lue ja vastaa lyhyesti kysymyksiin.

![image](https://github.com/user-attachments/assets/2185bc5d-2be1-4fa1-bfde-dc488f5ae305)

Tuskan pyramidi kuvastaa, kuinka vaikeaa hyökkääjän on reagoida eri tyyppisten indikaattoreiden estämiseen. Mitä korkeammalla ollaan pyramidissä sitä vaikeampi indikaattori on estää.

![image](https://github.com/user-attachments/assets/d94df61d-8893-49ac-a804-10cead35a067)

Timantti-malli on perusta kyberuhkien analysoimiseen, se jakaa tiedot neljään osaan: 

- Adversary: Who did the attack?
- Capability: How did they do it?
- Victim: Who was targeted?
- Infrastructure: What was used?

Tämä malli auttaa hahmottamaan näiden osien väliset suhteet ja ymmärtämään hyökkääjää.


## a) Apache log.

Asensin apachen komennolla "sudo apt install apache2". Tämän jälkeen avasin selaimen ja menin http://192.168.101.113 tämä avasi apachen oletussivun, joka kertoo että Apache toimii.

<img width="1092" alt="image" src="https://github.com/user-attachments/assets/7f83c70a-f0c6-4e15-ba77-517dfc9698c5" />

## b) Nmapped.

<img width="735" alt="image" src="https://github.com/user-attachments/assets/27038504-974b-494c-9872-67312c555842" />

- 80/tcp open http Apache httpd 2.4.62 ((Debian)) : Tämä tarkoittaa, että portti 80/tcp on auki ja käytössä on apache web palvelin versio 2.4.62

## c) Skriptit

Skriptejä jotka olivat automaattisesti päällä, kun käytin "-A" parametriä ovat 

- http-title
- http-robots
- http-server-header

## d) Jäljet lokissa.

Komennolla sudo grep -i nmap /var/log/apache2/access.log löysin sanan "nmap" pienellä. 

Asioita mistä tunnistaa porttiskannauksen :

- IP:stä nähdään että skannaus on tehty lokaalisti
- Pyynnöt on tehty erittäin nopeasti
- "Nmap scripting engine" kertoo että pyynnät ovat Nmapin NSE-skriptejä

### Millaisilla hauilla tai säännöillä voisit tunnistaa porttiskannauksen jostain muusta lokista, jos se on niin laaja, että et pysty lukemaan itse kaikkia rivejä?

Komennolla grep "Nmap Scripting Engine" /var/log/apache2/access.log 

<img width="1265" alt="image" src="https://github.com/user-attachments/assets/b185c7fa-93ca-48b3-9423-97a52b39367c" />


## e) Wire sharking.

Aloitin tehtävän käynnistämälle Wireshark:n ja valitsin "Loopback:lo". Tämän jälkeen suoritin komennon "sudo nmap -A localhost". Skannauksen jälkeen tallensin tiedoston .pcap muotoon.

Seuraavaksi avasin hakukentän (Ctrl+F), josta valitsin Display filter -> String -> Packet bytes. Tämän jälkeen kirjoitin hakuun nmap ja tulos oli seuraavanlainen.

<img width="1280" alt="image" src="https://github.com/user-attachments/assets/5c76f19d-a7d6-4347-b3b6-92f9e15d71d6" />

### Yleinen analyysi

Kaappauksessa näkyy, että Nmap lähettää HTTP-pyyntöjä ja käyttää User-Agent "Nmap Scripting Engine" tunnistetta. Tämä tarkoittaa että skannauksessa on käytetty NSE-skriptejä.

## f) Net grep. 

<img width="584" alt="image" src="https://github.com/user-attachments/assets/168b69d3-474e-4c1e-8d0f-efc0691b7683" />

## g) Agentti.











