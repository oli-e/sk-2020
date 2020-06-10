# Podział i agregacja sieci

Dysponująć siecią o adresie ``172.16.0.0/18`` dokonaj podziału na 6 równych podsieci

| Parametr | wartość | komentarz(opcionalny) |
| ------------- |:-------------:| -----:|
| Adres sieci do podziału |172.16.0.0 |  
| Maska sieci  | 255.255.192.0 | |
| Maska binarnie  | 11111111 11111111 11000000 00000000 | |


2^n >= 6
2^3 >= 6
n = 3

| Podsiec   | Adres podsieci | Host min     | Host max      | Adres rozgłoszeniowy |
| -------------     |:-------------: | -----:       | -----:        | -----:    |
| 1         | 172.16.0.0 | 172.16.0.1      | 172.16.31.253 |  172.16.31.254 |
| 2         | 172.16.32.0 | 172.16.32.1      |           |                  |
| 3         |  |          |||
| 4         |  |          |||
| 5         |  |          |||
| 6         |  |          |||
