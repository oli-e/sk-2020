# Podział i agregacja sieci

Dysponująć siecią o adresie ``172.16.0.0/16`` dokonaj podziału na 6 równe podsieci

| Parametr | wartość | komentarz(opcionalny) |
| ------------- |:-------------:| -----:|
| Adres sieci do podziału | 172.16.0.0 |  
| Maska sieci  | 16 | |
| Maska binarnie  | 255.255.0.0 | |


2^n >= 6
2^3 >= 6
n = 3

| Podsiec   | Adres podsieci | Host min     | Host max      | Adres rozgłoszeniowy |
| -------------     |:-------------: | -----:       | -----:        | -----:    |
| 1         | 172.16.0.0 | 172.16.0.1      | 172.16.31.253 |  172.16.31.254 |
| 2         | 172.16.32.0 | 172.16.32.1      |  |  |
| 3         | 
| 4         |
| 5         |
| 6         |
| 7         |
| 8         |
