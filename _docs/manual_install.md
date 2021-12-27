---
title: "Instalacja"
permalink: /docs/manual-install/
excerpt: "Dokumetacja SAKOL - instrukcja instalacji"
---

# Architektura aplikacji
Poniżej przedstawiony został schemat aplikacji SAKOL. Aplikacja SAKOL składa się z Aplikacji na urządzenie z systemem Android, która może być również obsługiwana przez stronę WWW, Panelu administracyjnego SAKOL_ADMIN, SAKOL3 Data Service, czyli usługi która jest odpowiedzialna za działanie aplikacji SAKOL oraz wymianę danych. Aplikacja SAKOL ściśle współpracuje z aplikacją XDTW, poprzez XDTW następuje wymiana danych oraz synchronizacja dokumentów z bazą SAP. 

![image](https://user-images.githubusercontent.com/93259107/144219348-7c4014b1-b5a0-4d63-8fd9-09b2ffb5db86.png)

# Instalacja SAKOL DataService
## Instalacja bazy danych

Baza danych SAKOL3 działa na silniku SQL. Na początek instalacji SAKOL odtwarzamy pustą bazę w Management Studio

![image](https://user-images.githubusercontent.com/93259107/144235718-c351084f-6db9-4970-9fc2-92f2c1125ebe.png)

![image](https://user-images.githubusercontent.com/93259107/144236015-f14b38f0-e7a9-40d7-9c82-78ba69e15c9f.png)


## Instalacja usługi
W pierwszej kolejności tworzymy katalog SAKOL3 w którym umieszczamy katalogi z aplikacją WWW, panelem administracyjnym oraz usługą.

![image](https://user-images.githubusercontent.com/93259107/144237890-1ff27912-4976-4437-afda-64d61150f880.png)

Kolejnym krokiem jest edycja pliku konfiguracyjnego sakol3.ini, który znajduje się w katalogu SAKOL3_DataService.

![image](https://user-images.githubusercontent.com/93259107/144241631-4522f740-35ca-4807-8210-c14dec022ab3.png)

Zmieniamy parametry w pliku konfiguracyjnym.

![image](https://user-images.githubusercontent.com/93259107/147466691-626fb4c5-b422-4e69-9785-338ad42ff103.png)


W początkowej konfiguracji istotnymi parametrami są:
DataSource - jest to serwer SQL na którym jest baza danych SAKOL3
UserID - użytkownik SQL
Password - hasło SQL
DBName - nazwa bazy 
WSParam1 - Nazwa bazy SAP
HtmlAppPath - ścieżka do aplikacji WWW

Usługę instalujemy poprzez cmd z uprawnieniami administracyjnymi

![image](https://user-images.githubusercontent.com/93259107/144231064-8b4fb001-aa91-48c3-bba7-7a37f432bac1.png)

W cmd korzystamy z funkcji istallutil. 

![image](https://user-images.githubusercontent.com/93259107/144232784-b0c5285f-70f1-435a-8aa5-fb82c43ff701.png)

Jeżeli pojawi się poniższy komunikat oznacza, że usługa SAKOL3_DataService została zainstalowana

![image](https://user-images.githubusercontent.com/93259107/144233078-f430c7ee-e695-4bf2-81ba-58433f598685.png)



# Klient WWW
> Jak zainstalowac na IIS
W pierwszej kolejności dodajemy pulę aplikacji SAKOL3 w IIS

![image](https://user-images.githubusercontent.com/93259107/147079207-7f20cf91-b177-42a8-adbe-515b8a03ef2b.png)

Następnie konfigurujemy witrynę 

![image](https://user-images.githubusercontent.com/93259107/147083333-a6670db8-6704-47bd-aedb-9d08096e5f9d.png)

Konwertujemy nasz folder na aplikację 

![image](https://user-images.githubusercontent.com/93259107/147083597-8ddd8786-0ba5-4087-8ccf-414e32e7d7d5.png)

Zmieniamy ustawiania w pliku config.json, który znajduje się w następującej lokalizacji:

C:\Altab\Sakol3\inetpub\SAKOL3\assets

Edytujemy plik config.json. Zmianiamy wartość w polu EndPointAddress, ustawiamy adres witryny i port usługi.

![image](https://user-images.githubusercontent.com/93259107/147466858-5e653165-03c0-4494-8731-613856fc65ef.png)

Pamiętamy o pliku licencji, po któy musimy skontaktować się z firmą Altab, inaczej aplikacja SAKOL nie zadziała. Plik licencji należy skopiować do folderu z usługą:

![image](https://user-images.githubusercontent.com/93259107/147467202-4d270622-ee43-464e-919d-62778c7c9050.png)


Uruchamiamy aplikację SAKOL3 z poziomu IIS

![image](https://user-images.githubusercontent.com/93259107/147467174-76254d86-064b-4ed7-a0f5-f6969c79c411.png)

Aplikacja SAKOL z pustą bazą bez użytkowników i modułów wygląda następująco:

![image](https://user-images.githubusercontent.com/93259107/147467393-779f76ac-7a4e-418c-b5e8-3b7bb3ee43ad.png)


# Sprawdzenie instalacji
Po instalacji SAKOL3 przechodzimy do weryfikacji działania aplikacji, przechodzimy do panelu administracyjnego, żeby dodać uzytkownika i zalogować się do aplikacji:


