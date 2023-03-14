# CNS PRIPREMNA PITANJA

1. What is the Address Resolution Protocol (ARP), and what is its role in a network?
ARP ili Address Resolution Protocol je komunikacijski protokol koji služi za povezivanje IP i MAC(fizičke) adrese nekog uređaja u lokalnoj mreži(LAN, WLAN).

2. What is a Man-in-the-Middle (MitM) attack, and how does ARP spoofing enable it?
Čovjek u sredini je vrsta napada prema kojemu se na komunikacijski kanal između pošiljatelja i primatelja ilegalno spaja treća strana te ga prisluškuje. ARP spoofing je vrsta napada prema kojoj napadač šalje lažne ARP zahtjeve prema željenoj lokalnoj mreži i na taj način uvjerava pošiljatelja da je on primatelj, a primatelja da je pošiljatelj. Na taj način ARP spoofing trećoj strani omogućuje neprimjetno spajanje na kanal.

3. How does an attacker use ARP spoofing to intercept network traffic?
Napadač šalje lažne ARP zahtjeve ciljanoj lokalnoj mreži. Odnosno pošiljatelju će poslati IP adresu stvarnog primatelja i svoju MAC adresu te ga tako uvjeriti da je on primatelj, a primatelju će poslati IP adresu stvarnog pošiljatelja i svoju MAC adresu te ga tako uvjeriti da je on pošiljatelj.

4. How is the cookie used to derive the encryption/decryption key?
Cookie je tajna vrijednost na koju se primjenjuje određena matematička funkcija ili algoritam za generiranje tajnog ključa. Npr. u simetričnoj enkripciji ista tajna vrijednost(tajni ključ) se koristi za enkripciju i dekripciju. S druge strane u asimetričnoj enkripciji različiti ključevi se koriste za enkripciju i dekripciju, postoje javni ključ i privatni ključ(tajna vrijednost).

5. What REST API request do you need to send to the crypto oracle the secret cookie?
GET /arp/cookie

6. How do you obtain the authentication token?
Potrebno ga je zatražiti od crypto oracle servera slanjem zahtjeva oblika: "POST username=my_name&password=my_pass /arp/token".

7. How do you use the authentication token to obtain the cookie?
Autentifikacijski token koristi se valjanu autentifikaciju korisnika kako bi mogao poslati GET /arp/cookie zahtjev crypto oracle serveru.

8. What encryption mode is used to encrypt the challenge in this lab?
CBC enkripcijski mod rada (AES-CBC).

9. What tool can you use to capture network traffic on a local network interface?
Tcpdump.
