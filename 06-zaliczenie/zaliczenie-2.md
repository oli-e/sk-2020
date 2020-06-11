# Zadanie 2

Projekt sieci spełnił oczekiwania, organizacja po uwzględnieniu nowych wymogów chce podzielić dotychczasowe sieci na kilka podsieci.

1. Zaprojektuj oraz udokumentuj prototyp rozwiązania z wykorzystaniem oprogramowania ``CISCO Packet Tracer``, ``VirtualBox`` lub podobnego. 

## Schemat

![zadanie 2](stage-02.svg)

## Charakterystyka
  * LAN 1 pozostaje bez zmian
  * LAN 2 zostaje podzielony na 3 równe podsieci
  * LAN 3 zostaje podzielony na 3 podsieci z uwzględnieniem
    * podsieć 1 ma obsłużyć do 512 hostów
    * podsieć 2 ma obsłużyć do 10 hostów
    * podsieć 3 ma obsłużyć do 32 hostów
  * Usunięty został również link pomiędzy Routerem (LAN 1) a Routerem (LAN 2)
  * Uwzględnij zmiany w tablicy routingów

Sieć pierwotna: 

LAN 1: 78.10.0.0/22

LAN 2: 78.10.4.0/22, nowy subnet mask: 255.255.255.0 (24)
* Podsieć 1: 78.10.4.0, Ranga hostów od: 78.10.4.1 do 78.10.4.254, Broadcast: 78.10.4.255, rozmiar subnetu 254
* Podsieć 2: 78.10.5.0, Ranga hostów od: 78.10.5.1 do 78.10.5.254, Broadcast: 78.10.5.255, rozmiar subnetu 254
* Podsieć 3: 78.10.6.0, Ranga hostów od: 78.10.6.1 do 78.10.6.254, Broadcast: 78.10.6.255, rozmiar subnetu 254

LAN 3: 78.10.8.0/22, nowy subnet mask: 
* Podsieć 1: 78.10.8.0, 
* Podsieć 2: 
* Podsieć 3: 


## Zawartość

 * Adresy poszczególnych sieci IP
 * Adresację linków pomiędzy routerami
 * Tablice routingów na poszczególnych routerach
 
