---
title: "zadania 6-10"
tags: ""
---
## zadanie 6

-   ls -all
-   find / -size 33c znalazlem lokalizacje pliku bandit7.password i tam wlasnie bylo ukryte haslo
-   cd /var/lib/dpkg/info
-   cat bandit7.password

## zadanie 7

-   ls -all 
-   cat data.txt
-   grep "millionth" data.txt i obok tego słowa bylo poprawne hasło do nastepnego zadania

## zadanie 8

-   ls -all
-   cd data.txt
-   sort -n
    wiem ze jakos to mozna z unikatowym ale juz szybciej znalazlem unikatowe haslo

## zadanie 9

-   ls -all 
-   strings data.txt | grep "=" tu wyswietlilem linijke, która posiada znak równości "="

## zadanie 10

-   cat data.txt
    #### w środku znajdował się tekst w formacie base64, którym musial skonwertować na system ASCII . po wpisaniu komendy :
-   base64 -d data.txt teskt zostal skonwertowany u naszym oczom ukazało się haslo
