---
title: "zadania 11-15"
tags: ""
---
## zadanie 11

-   te zadanie opiera się na szyfrze przesuwającym o nazwie ROT13. polega on na przesunięciu każdego znaku z alfabetu łacińskiego na znak występujący 13 pozycji po nim
-   cat data.txt
-   strona www rot13

## zadanie 12

bylo to wg mnie najtrudniejsze zadanie
potrzebowalem wiele komend takie jak :

-   ls 
-   file
-   gzip -d
-   bzip2 -d
-   tar xf
-   mv
-   xdd -r [plik] > [nowy plik] rozszyfrowanie tekstu
    za kazdym razem gdy po dekompresji wychodził mi plik z inną kompresją to musiałem zmieniać nazwe tego pliku i dopiero pozniej moglem przystępować do dekompresji i tak z 10 razy aż w końcu dokopałem się do hasła 

### BARDZO TRUDNE ZADANIE DO ZROZUMIENIA

## zadanie 13

-   musiałem wejsc na konto bandita 14 za pomoca klucza ssh komendą:
-   ssh -i shhkey.private bandit14@localhost
-   pozniej wszedlem na folder /etc/bandit_pass/bandit14 i tam z uprawnieniami bandita14 moglem odczytać haslo do następnego lvla

## zadanie 14

#### w tym zadaniu musiałem pozostać na bandicie14 i musialem przenieść sie do portu 30000 za pomocą komendy :

-   nc localhost 30000 ( ponieważ ssh mi jakoś nie wchodziło to przeczytałem w internecie ze przez netcad jest łatwiej i mniej pisania)

#### później po połączeniu ukazało się nam hasło do kolejnego zadania

## zadanie 15

#### w tym zadaniu na bandicie 15 musiałem wejść na port 30001 by otrzymać swoje hasło do następnego lvla

#### użyłem następującej komendy by wejść na dany port i musiałem użyć komendy z ssl :

-   openssl s_client -connect localhost:30001

#### po wejściu musimy podać hasło z poprzedniego poziomu i wyświetla nam się komunikat Correct i podaje nam hasło do następnego poziomu
