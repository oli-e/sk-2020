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




## Zawartość

 * Adresy poszczególnych sieci IP

   LAN 1: 78.10.0.0/22

   LAN 2: 78.10.4.0/22, nowy subnet mask: 255.255.255.0 (24)
    * Podsieć 1: 78.10.4.0, Ranga hostów od: 78.10.4.1 do 78.10.4.254, Broadcast: 78.10.4.255, rozmiar subnetu 254.
    * Podsieć 2: 78.10.5.0, Ranga hostów od: 78.10.5.1 do 78.10.5.254, Broadcast: 78.10.5.255, rozmiar subnetu 254.
    * Podsieć 3: 78.10.6.0, Ranga hostów od: 78.10.6.1 do 78.10.6.254, Broadcast: 78.10.6.255, rozmiar subnetu 254.

   LAN 3: 78.10.8.0/22, nowy subnet mask: 
    * Podsieć 1: 78.10.8.0, Ranga hostów od: 78.10.8.1 do 78.10.10.3, Broadcast: 78.10.10.4, subnet 512 hostów, maska 24.
    * Podsieć 2: 78.10.10.16, Ranga hostów od: 78.10.10.17 do 78.10.10.26, Broadcast: 78.10.10.26, subnet 10 hostów, maska 28.
    * Podsieć 3: 78.10.10.64, Ranga hostów od: 78.10.10.65 do 78.10.10.96, Broadcast: 78.10.10.97, subnet 32 hosty, maska 26.

 * Adresację linków pomiędzy routerami
    * Router1 (78.10.96.1) via Gig8 to Router2 (78.10.99.254) via Gig8
    * Router2 (78.10.100.1) via Gig9 to Router3 (78.10.103.254) via Gig9

 * Tablice routingów na poszczególnych routerach
    * Router1: 78.10.8.0/22 via 78.10.99.254
               78.10.10.16/28 via 78.10.99.254
               78.10.10.64/26 via 78.10.99.254
              
    * Router2: 78.10.0.0/22 via 78.10.96.1
               78.10.4.0/24 via 78.10.103.254
               78.10.5.0/24 via 78.10.103.254
               78.10.6.0/24 via 78.10.103.254

   * Router3: 78.10.8.0/24 via 78.10.100.1
              78.10.10.16/28 via 78.10.100.1
              78.10.10.64/26 via 78.10.100.1
