# analiza ruchu sieciowego

  * https://www.tcpdump.org/
  * https://www.wireshark.org/
  * https://wiki.wireshark.org/CaptureFilters

## OSI

  ![osi-iso](osi.svg)

## Komunikacja

  ![osi-flow](osi-flow.svg)

## Wartstwa transportowa

  * nawiązanie i obsługa połączeń (sesji) pomiędzy hostami,
  * śledzenie połączeń pomiędzy hostami,
  * podział danych na mniejsze fragmenty,
  * identyfikowanie poszczególnych aplikacji,
  * kontrola przepływu danych,
  * retransmisja w przypadku utraty danych.

## Zadanie 

### TCP vs UDP
1.
   * Przygotuj konfigurację sieci gdzie wykorzystasz 2 komputery. 
     * PC-1 pełniący rolę serwera testowanych usług
     * PC-2 pełniący rolę klienta oraz snifera dla testowanych usług
   * Uruchom PC2 w z wykorzystaniem dystrybucji z interfejsem graficznym
   * Zainstaluj program wireshark dla ``PC2``
   * Wykonaj analizę i zanotuj spostrzerzenia
     * tcp echo server vs udp echo server


![10-cwiczenia](tcpvsvg.svg)


### HTTP vs HTTPS
2. 
   * Zainstaluj serwer ``HTTP`` program nginx
   * Przygotuj certyfikat zabezpieczajączy połączenie z serwerem
   * Skonfiguruj możliwość połączenia z wykorzystaniem nowo utworzonych certyfikatów
   * Porównaj komunikacją na różnych warstwach OSI w zależności od wykorzystanego protokołu HTTP vs HTTPS
   
   
   Unlike HTTP, where requests and responses are sent and returned in plaintext, HTTPS uses TLS/SSL to encrypt the communication between      the client and the server.

      There are many benefits of using HTTPS over HTTP, such as:
         *All the data is encrypted in both directions. As a result, sensitive information cannot be read if intercepted.
         *Google Chrome and all other popular browsers will mark such website as safe.
         *HTTPS allows you to use the HTTP/2 protocol, which significantly improves the site performance.
         *Google favors HTTPS websites. Such site will rank better if served via HTTPS.

       The preferred method to redirect HTTP to HTTPS in Nginx is to configure a separate server block for each version of the site. 
      
