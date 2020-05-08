# NAT - Network address translation

## Zadanie

![zadanie 7](nat-1.svg)

1.
   * Przygotuj konfigurację sieci zgodnie z powyższym diagramem
   * Zweryfikuj poprawność połączenia z siecią internet dla ``PC0``
      * adresacja
      * konfiguracja DHCP (opcjonalna ale wygodna) 
   * W pierwszej kolejności przygotuj ``PC0``, ``PC-1``
   * Upewnij się o poprawnej konfiguracji parametru systemu ``ip_forward`` dla ``PC0``
   * Do konfiguracji wykorzystaj właściwą konfigurację ``VirtualBox`` która pozwoli na dostęp do internetu dla ``PC-1`` za pomocą interfejsu ``eth0``
   * Wykonaj konfigurację translacji adresów tak aby udostępnic komunikację z siecią internet dla ``PC-2``
   * Przygotuj dokumentację powyższego procesu
   *  **czy istnieje różnica jeżeli adres eth0 statyczny/dynamiczny? Jeżeli to jaka?**


![zadanie 7](nat-2.svg)

1. 
    * Przygotuj konfigurację sieci zgodnie z powyższym diagramem
    * Wykonaj konfigurację translacji adresów tak aby udostępnic komunikację z siecią internet dla ``PC-2`` oraz ``PC-3``
    
2. 
    * Jeżeli konfiguracja była do tej pory statyczna, rozszerz architekturę o automatyczną konfigurację hostów w podsieciach ``192.168.64.192/27`` oraz ``172.16.95.216/29`` z wykorzystaniem usługi ``DHCP``


## Zadanie do domu

1. Zapoznaj się z pojęciem Maskarady IP ``MASQUERADE``

Network Address Translation (NAT, translacja adresów rodzimych. Znane również jako maskarada IP) To technika przesyłania ruchu sieciowego poprzez router, która wiąże się ze zmianą źródłowych lub docelowych adresów IP, zwykle również numerów portów TCP/UDP pakietów IP podczas ich przepływu. Zmieniane są także sumy kontrolne (zarówno w pakiecie IP, jak i w segmencie TCP/UDP), aby potwierdzić wprowadzone zmiany.

Większość systemów korzystających z NAT ma na celu umożliwienie dostępu wielu hostom w sieci prywatnej do Internetu przy wykorzystaniu pojedynczego publicznego adresu IP. Niemniej NAT może spowodować komplikacje w komunikacji między hostami i może mieć pewien wpływ na osiągi.

Wraz ze wzrostem liczby komputerów w Internecie, zaczęła zbliżać się groźba wyczerpania puli dostępnych adresów internetowych IPv4. Aby temu zaradzić, lokalne sieci komputerowe, korzystające z adresów prywatnych, mogą zostać podłączone do Internetu przez jeden router, mający mniej adresów internetowych niż komputerów w tej sieci. Mimo iż w każdej prywatnej sieci może być zalokowane niemal 17 milionów adresów[1] to ograniczeniem będą używane do NAT porty, których jest 65535.

Router ten, gdy komputery z sieci lokalnej komunikują się ze światem, dynamicznie tłumaczy adresy prywatne na adresy zewnętrzne, umożliwiając użytkowanie Internetu przez większą liczbę komputerów niż posiadana liczba adresów zewnętrznych.

NAT jest często stosowany w sieciach korporacyjnych (w połączeniu z proxy) oraz sieciach osiedlowych.
  
## Materiały

* https://linux.die.net/man/8/iptables
