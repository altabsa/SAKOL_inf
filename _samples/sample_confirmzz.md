---
title: "PZ z Zam. zakupu"
permalink: /samples/sample-confirmzz/
excerpt: "Potwierdzenie przyjetych ilości na dokumencie ZZ"
---

# Zadanie
Opis zadania
> Poniżej zostanie przedstawiony przykład zastosowania aplikacji SAKOL3. Na bazie SAP Bussiness One zostanie dodany dokument zamówienia zakupu, pozycje z zamówienia zostaną zrealizowane w SAKOL, po zrealizowaniu dokumentu ZZ w SAKOL zostanie dodany dokument potwierdzający ruchy magazynowe w SAP.

# Rozwiązanie
## Klasy
> W pierwszej kolejności dodajemy klasę PZ. Klasę dodajemy w panelu administracyjnym SAKOL w zakładce klasy. 

![image](https://user-images.githubusercontent.com/93259107/159937127-e83323c0-9926-4a8a-8dc8-cb312878596c.png)

> Nazwę klasy uzupełniamy jako PZ, uzupełniamy opis klasy. Pole opis jest istotne, ponieważ na liście add-on w SAKOL wyświetlane nazwy są własnie na podstawie pola Opis:

![image](https://user-images.githubusercontent.com/93259107/159937749-eadd982d-8038-4dce-bd12-1a62ed032322.png)

> Dodajemy kolejne pola:

![image](https://user-images.githubusercontent.com/93259107/159939279-911ae4a4-1dbb-48f6-9da5-433c69eb84d3.png)

> Dodanie wszystkich wymaganych pól:

![image](https://user-images.githubusercontent.com/93259107/160125008-ae8a9339-2ab8-4f50-9a1a-185bb8b60a05.png)


## Formatki
> Formatkę tworzyny w panelu administracyjnym w zakładce formatki. Tworzymy formatkę o nazwie PZ oraz podpinamy stworzoną klasę C_PZ:

![image](https://user-images.githubusercontent.com/93259107/159945467-c2a3edfb-b25a-476b-8c02-625f25087719.png)


## Addon
> jak zaprojektowac logikę

# Uwagi
> Ewentualne uwagi
