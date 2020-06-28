# Zadanie 1

Organizacja planuje ulepszyć działanie istniejącej sieci biurowej.

1. Zaprojektuj oraz udokumentuj konfigurację prototypu rozwiązania z wykorzystaniem oprogramowania ``VirtualBox`` lub podobnego. 

## Schemat

![zadanie 1](office.svg)

## Wymagania

W sieci pracują komputery biurowe oraz urządzenia siecowe współdzielące zasoby. Do tej pory organizacja borykała się z ręczna konfiguracją urządzeń oraz adresami IP które dla ludzi z poza kadry technicznej były niezrozumiałe. Postanowiono:

* Wykorzystać usługę DHCP do nadawania adresów w sposób automatyczny dla wszystkich stacji roboczych
* Serwer oraz durządzenia IP tj: drukarka muszą posiadać stałe adresy celem zminimalizowanai potrzeby rekonfiguracji ustawiań klientów
* Wprowadzić translację pomiędzy Adresami IP oraz nazwami domenowymi dla kluczowych zasobów
   - erp.mojaorganizacja.pl
   - drukarka.mojaorganizacja.pl
   - router.mojaorganizacja.pl
* Wszystkie urządzenia łączą się z siecią internet z wykorzystaniem bramy NAT
* Wykorzystać podsieć rozmiaru /22 pozwalającej zaadresować co najmniej 600 urządzeń

## Zawartość dokumentacji

 * **Charakterystyka rozwiazania** 
   - Topologia zawiera jak na załączonym schemacie dwa komputery stacjonarne, drukarkę oraz serwer oraz się łączy z siecią prywatną poprzez NAT oraz routery, która zawiera serwer. Celem jest by wszystkie urządzenia w każdej z sieci były w stanie się komunikować pomiędzy sobą oraz dodatkowo w sieci 78.10.100.0/22 większości adresy IP nadaje serwer DHCP znajdujący się pod adresem 78.10.100.2.
   
 * **Adresy sieci IP**
     - 78.10.100.0/22 
     - 78.10.0.0/22
     - Dla NAT: 5.5.5.0/24
     - 192.168.100.0/24
     
 * **Oprogramowanie wykorzystane do realizacji poszczególnych wymagań**
   - Cisco Packet Tracer
   
 * **Kluczowa konfiguracja oprogramowania pozwalająca na odtworzenie stanu po reinstalacji środowiska**
    ### Konfiguracja NAT z iptables
     * Połączenie NAT zostało zaprojektowane przy pomocy dwóch routerów w sieci 5.5.5.0 o masce 24(255.255.255.0), w tablicach routingu są dwa wpisy w jednym -   ``192.168.100.0/24 via 5.5.5.5`` i - ``78.10.0.0/16 via 5.5.5.6``

    ### Konfiguracja DHCP
     * na interfejsie ``FastEthernet0`` utworzono Pool ``serverPool`` z defaultowym gateway’em ``78.10.100.1`` oraz serwerem DNS ``78.10.100.5``. Jako IP startowe przydzielono ``78.10.100.0`` z maską ``255.255.252.0``. Maksymalną liczbę użytkowników ustalono na 600.

    ### Konfiguracja DNS
     * **drukarka.mojaorganizacja.pl** ->  ``78.10.100.5``
     * **erp.mojaorganizacja.pl** ->  ``78.10.100.10``
     * **router.mojaorganizacja.pl** ->  ``78.10.100.1``

 
    ### Konfiguracja interfejsów sieciowych
     * Router WRT300N posiada interfejsy o adresach ``LAN:78.10.100.1/22`` oraz Internet(połączenie z routerem1): ``78.10.0.1/22``
     * Router1 biorący udział w połączeniu NAT ma też dwa aktywne interfejsy - > ``GibEth8/0: 78.10.0.2/22`` i  ``GibEth7/0: 5.5.5.6/24``.
     * Router0 -> ``5.5.5.5/24`` oraz ``192.168.100.1/24``
