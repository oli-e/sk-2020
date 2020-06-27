# Zadanie 1

Organizacja planuje rozpoczęcie działalności w 3 budynkach, w każdym z nich przewiduje do 1000 urządzeń IP

1. Zaprojektuj oraz udokumentuj prototyp rozwiązania z wykorzystaniem oprogramowania ``CISCO Packet Tracer``, ``VirtualBox`` lub podobnego. 

## Schemat

![zadanie 1](stage-01.svg)

## Zawartość

 * Adresy poszczególnych sieci IP
  
   
  | Parametr | wartość | 
| ------------- |:-------------:|
| Adres sieci do podziału | ``96.10.0.0`` | 
| Maska sieci  | ``255.255.252.0`` | 

3 podsieci:
  
 * ``96.10.0.0/22``
 * ``96.10.4.0/22``
 * ``96.10.8.0/22`` 
 
Adresację linków pomiędzy routerami:

* ``Router1 (96.10.0.1) via Gig8 to Router2 (96.10.3.254) via Gig8``
* ``Router1 (96.10.8.1) via Gig9 to Router3 (96.10.11.254) via Gig9``
* ``Router2 (96.10.4.1) via Gig9 to Router3 (96.10.7.254) via Gig8``

Tablice routingów na poszczególnych routerach:
 
* ``Router1: 96.10.104.0/22 via 96.10.3.254``
* ``       96.10.108.0/22 via 96.10.11.254``

* ``Router2: 96.10.100.0/22 via 96.10.0.1``
* ``        96.10.108.0/22 via 96.10.7.254``

* ``Router3: 96.10.104.0/22 via 96.10.4.1``
* ``       96.10.100.0/22 via 96.10.4.1``
