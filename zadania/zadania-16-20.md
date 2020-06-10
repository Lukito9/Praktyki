---
title: "zadania 16-20"
tags: ""
---
## zadanie 16

#### w tym zadaniu musimy przeszukac porty od 31000-32000

### komendy:

-   nmap localhost 31000-32000 
-   ncat --ssl localhost 31790 ( tu musimy wpisać haslo z poprzedniego zadania i ukazuje nam się rsa key bandita 17)
-   pico key ( musialem za pomocą edytora tekstu wpisac ten rsa key na pulpicie, zeby później z jego pomocą zalogować sie na nastepny poziom za pomocą ssh)
-   chmod 400 key ( trzeba nadać prawa tylko do odczytywania pliku )
-   ssh -i key bandit17@bandit.labs.overthewire.org -p 2200 

## zadanie 17

#### trzeba odszukac różnic pomiędzy starym haslem a nowym komendą:

-   diff password.old password.new ( na dole pojawiają się zmienione linie tekstu i kopiujemy nową linie tekstu z pliki password.new i to jest nasze hasło)

## zadanie 18

w 18 zadaniu musiałem ominąc plik .bashrc za pomocą komendy ssh przy logowaniu:

-   ssh -T bandit18@bandit.labs.ovethewire.org -p 2200
-   cat readme ( i w pliku było haslo do następnego)

## zadanie 19

w tym zadaniu musimy za pomocą konta uzytkownika bandit20 otworzyć plik, bo tylko on ma uprawnienia do otwierania plików. 

-   ./bandit20-do cat /etc/bandit_pass/bandit20

## zadanie 20

\####w tym zadaniu musiałem otworzyć nowy terminal i sie zalogować na dwoch terminalach na zadanie 20 i musiałem połączyć te dwa konta za pomocą metcad na porcie 1234
\###komendy :

-   cat /etc/bandit_pass/badnit20 | nc -l localhost -p1234 ( hasło bandita20 przesłałem na drugi terminal
-   ./suconnect 1234 ( połączyłem się i dostałem powiadomienie o pomyślnym połączeniu i w wiadomości zwrotnej na drugi terminal otrzymałem haslo do kolejnego zadania)
