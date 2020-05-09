## Zarządzanie interfejsami z wykorzystamiem programu IP

* stan interfejsu
    * interfejs up
    * interfejs down
* adresacja
    * dodaj adres
    * zmień adres
    * usuń adres
    * wyczyść adresy
* routing
    * pobierz trasę dla adresu
    
* adresacja fizyczna
    * pokaż adresy interfejsów dostępnych w sieci
    * pokaż adresy dla konkretnego interfejsu
     


### ip 

| subcommand    |  polecenie   | opis  |
| ------------- |:-------------| :---------------| 
|   ``addr``    |                            | informacje o adresacji i własnościach interfejsów |
|               |   ``ip addr``                 | informacja o wszystkich adresach             |
|               |   ``ip addr show dev enp0s3`` | informacja o konkretnym adresie              |
|   ``link``    |   | zarządza i wyświetla stan wszytskich inferfejsów  |
|       |  ``ip link`` | wyświetla informacje o interfejsach  |
|       |  ``ip link show dev em1`` | wyświetla informacje tylko dotyczące urządzenia em1  |
|       |  ``ip link set em1 up/down`` | em1 jest online/offline  |
|   ``route``   |  | wyświetla i modyfikuje tablicę trasowania |
| | ``ip route``  | wylicza wszystkie dostępne w jądrze systemu operacyjnego |
|   ``maddr``   |  | zarządza i wyświetla multikastowe ip adresy |
|   ``neigh``   |  | służy do dodawania nowego wpisu w tablicy sąsiedztwa |
|   ``help``    |  | wyświetla info dla subkomend |


