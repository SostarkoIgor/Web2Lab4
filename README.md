# Web2Lab4

Ovo je riješenje četvrte laboratorijske vježbe iz kolegija "Napredni razvoj programske potpore za web"

## Tekst zadatka

Potrebno je pokazati da se vlastita web stranica s pripadajućim resursima brže učitava korištenjem HTTP/2 protokola.

### Prvi dio: Instalacija i konfiguracija

U prvom dijelu projekta potrebno je:

1. Instalirati web poslužitelj **nginx**
2. Izraditi vlastiti **SSL certifikat**
3. Aktivirati **HTTPS/SSL**
4. Konfigurirati podršku za **HTTP/2** protokol u nginx poslužitelju
5. Uključiti **HTTP/2** protokol
6. Potvrditi da je podrška za **HTTP/2** protokol uključena

Za izvršenje prvog dijela vježbe koristiti sljedeće resurse:

- [nginx.org](http://nginx.org/)
- [Ubiq: Nginx SSL Configuration Step-by-Step](https://ubiq.co/tech-blog/nginx-ssl-configuration-step-step-details/)
- [CheapSSLSecurity: How to Enable HTTP/2 on Nginx](https://cheapsslsecurity.com/p/how-to-enable-http-2-on-nginx/)
- [Ubiq: How to Enable HTTP/2 in Nginx](https://ubiq.co/tech-blog/how-to-enable-http2-in-nginx/)
- [DigiCert: Nginx OpenSSL Installation](https://www.digicert.com/kb/csr-ssl-installation/nginx-openssl.htm)

Potvrdu da je HTTP/2 uključen napraviti kako je objašnjeno na predavanju.

### Drugi dio: Izrada web stranice

Nakon završetka prethodnih koraka (1. – 6.), pristupiti izradi vlastite web stranice s kojom će se pokazati jedna od dvije ključne prednosti protokola HTTP/2 nad HTTP/1.x, a to je brzina prijenosa dokumenata koji se mogu uspješno binarno komprimirati i/ili velikog broja istih dokumenata (zbog server push mehanizma).

#### Koraci za izradu:

1. U **html** direktoriju poslužitelja stvoriti direktorij **„lab4“** (npr. C:\nginx-1.22.0\html\lab4).
2. Izraditi vlastitu web stranicu koja sadržava:
   - Određeni tekst
   - Veći broj **CSS** ili **JS** datoteka
   - Više od 10 slika (JPEG, PNG, ili drugih formata)

Zbog binarnog prijenosa podataka HTTP/2 protokolom, preporuča se slijediti upute sa predavanja o optimalnom sadržaju web stranice za demonstraciju optimizacije brzine prijenosa.

#### Logiranje vremena učitavanja:

1. Logirati vrijeme učitavanja stranice na instanci **nginx** poslužitelja kada je **HTTP/2** uključen i kada je isključen (tj. kada je podržan samo **HTTP/1.x**).
2. Generirati dvije slike ekrana (print screen, screenshots) konzole web preglednika:
   - **http2.jpg** (s uključenim HTTP/2)
   - **no_http2.jpg** (s isključenim HTTP/2)

#### Generiranje HAR datoteka:

1. Generirati dvije HAR (HTTP Archive) datoteke:
   - **no_http2.har** (bez podrške za HTTP/2)
   - **http2.har** (s uključenom podrškom za HTTP/2)

Logirati samo ono što je dovoljno da se vidi podrška za HTTP/2, kao što je prikazano na slici niže. Prevelike datoteke i višestruko redundantni podaci neće se prihvaćati.

2. Print screen kartice **Network** u konzoli web preglednika mora obuhvaćati:
   - Zaglavlje
   - Listu s podacima
   - Podnožje i rubove konzole

Ako koristite **Windowse**, preporuča se generirati slike ekrana ugrađenom **Cropping tool** aplikacijom. Ovaj tool se aktivira istodobnim pritiskom na **WIN TIPKA + SHIFT + S**. Slike ekranom pomoću kamere mobitela neće se prihvaćati.

### Isporuka

Kao odgovor na ovo pitanje isporučiti redom:

1. Adresu javno dostupnog **git repozitorija** koji sadržava:
   - Traženu web-stranicu sa svim pripadajućim datotekama
   - Konfiguracijsku datoteku **nginx.conf**
   - Log datoteke **http2.har** i **no_http2.har**
   - Slike ekrana (screenshots) konzole web preglednika **http2.jpg** i **no_http2.jpg**
   
2. Napomene:
   - Npr. "Svi koraci su uspješno implementirani."
   - Npr. "Nisam uspio/la implementirati..." 
