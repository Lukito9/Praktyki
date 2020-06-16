---
title: "zadania 21-25"
tags: ""
---
## zadanie 21

#### te zadanie opiera się na CRON czyli programie do cyklicznego wykonywania zadań

-   ls /etc/cron.d/
-   cat /etc/cron.d/cronjob_bandit22 ( sprawdzamy jakie zadanie ma przydzielone bandit22)
-   cat /usr/bin/cronjob_bandit22.sh
-   cat /tmp/t07lds....

#### i wyświetla nam się hasło do następnego zadania

## zadanie 22

#### hasło jest poukrywane w plikach

-   cat /etc/ceon.d/cronjob_bandit23 ( tu pokazuje nam, że plik z haslem jest pod adresem /usr/bin/cronjob_bandit23.sh
-   cat /usr/bin/cronjob_bandit23.sh (tutaj mytarget znajduje się w ( echo I am user $myname | md5sum | cut-d ' ' -f 1 , pozniej wyświetla sie nam hash który pozniej wklejamy do adresu (cat /tmp/ {HASH} i wyświetla nam się hasło do następnego zadania)

## zadanie 23

#### musiałem stworzyć w folderze /car/spool/bandit24 skrypt, dzięki któremu mogłem przekierować hasło, które było usuwane co minutę do pliku w folderze /tmp/lukasz9 zebym mógł go na luzię odczytać po usunięciu skryptu

### komendy :

-   cd /var/spool/bandit24
-   vim test.sh
-   w skrypcie wpisuje:

#### #!/bin/bash

#### cat /etc/bandit_pass/bandit24 > /tmp/lukasz9/haslo

-   chmod 777 test.sh
-   cd
-   cd /tmp/lukasz9
-   czekamy 60 sekund 
-   cat haslo ( i mamy hasło do następnego zadania)

### zadanie 25

-   ls 
-   cat bandit26.sshkey
-   ssh bandit26@localhost -i bandit26.sshkey ( tu nas wywalało, więc musialem znaleźć skrypt który mnie wywalał 
-   cat /etc/passwd
-   cat /usr/bin/showtext ( tu znajdował się skrypt)
-   po przeczytaniu skryptu dowiadujemy się ,ze wyświetla on duzy tekst BANDIT26 po czym się wyłącza, musiałem znaleźć sposob by zatrzymać skrypt, zeby nie doszedł do końca i nie wywalił mnie 
    \-sięgając pamięcia  do problemu, którego miałem w szkole, czyli nie wyświetlenie całego pliku z powodu za małego okna, wpadłem na pomysł, by zmniejszyć okno terminala i w ten sposób udało mi się zatrzymać skrypt 
-   później musiałem ogarnąć zeby edytować tekst edytorem VI 
-   wyszukałem komendy " :e ", która otwiera plik do edycji i za pomocą tej komendy otworzyłem plik z hasłem 
-   vi
-   :e /etc/bandit_pass/bandit26
-   i pokazuje się nam hasło 

# Dziękuję za uwagę!
