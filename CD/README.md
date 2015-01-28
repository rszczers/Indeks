Wirtualny Indeks
====

Diagram klas
----

Trzymając się zaleceń, diagram wykonany jest we Whitestar UML. 
Tutaj chciałbym zwrócić uwagę na kilka szczegółów. 


Konwencje
----

Linię oznaczającą implementację kreśli się w nim prostą ciągłą kreską zamiast
zwyczajnie, jak sądzę – przerywaną z białym grotem. Tam gdzie klasy implementują
interfejs uznałem, że rozsądniej będzie zaznaczyć implementację przez
generalizację, niż używać notacji proponowanej przez program (zwykłej kreski
między klasami).


Szczegóły projektowe
----
Projekt oparty jest na architekturze MVC. Kontrolery realizują wzorzec
strategii, Widoki – kompozyt, relacja Modele-Widoki – wzorzec obserwer.


Projektując aplikację miałem na uwadze wykonanie jej w – tutaj mała krotochwila
- technologii php i wydaje mi się, że nieznacznie czuć to w kilku miejscach.


Klasa Controller zawiera parser url, który odpala odpowiedni kontroler i
przekazuje mu odpowiednie argumenty po wyklikaniu przez użytownika odpowiedniego adresu.
To całkiem klasyczne rozwiązanie stosowane w popularnych cms'ach.


Widoki zorganizowane są w drzewo komponentów. Komponenty (np. GroupListView) są
pewnymi powtarzającymi się elementami strony (formularze, listy itp). Definicje
poszczególnych stron są zakodowane na twardo przy użyciu gotowych komponentów w katalogu
widoków, których diagram nie uwzględnia.


Z innych szczegółów implementacyjncyh warto zwrócić uwagę na klasę DbHelper,
która dziedziczy z klasy PDO, która w php realizuje
obsługę baz danych.
