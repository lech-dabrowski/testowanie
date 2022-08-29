# III - Testowanie statyczne

Testowanie statyczne to skomplikowana nazwa na zwykłe czytanie. Czytać można kod programu, specyfikację wymagań, diagram danej aplikacji itd. Nie jest wymaganie uruchomienie kodu. Podstawową zaletą tego podejścia jest szybkie i stosunkowo tanie wykrywanie potencjalnych błędów w testowanym systemie.

## Produkty pracy, które można testować statycznie:

- specyfikacja i wymagania (czyli jeden z najwcześniej powstających dokumentów)
- opowieści i historyjki użytkownika
- kod oczywiście
- dokumentacja (projekt techniczny, podręcznik użytkownika)
- modele, diagramy, makiety
- powstałe już testalia (plan testów, przypadki testowe)\

## Zalety testowania statycznego

- wykrycie defektów na wszesnym etapie pracy (nawet w wymaganiach)
- redukcja czasu i kosztów produkcji oprogramowania
- zapobieganie przedostawaniu się błędów na dalsze etapy pracy
- lepsza komunikacja w zespole (testowana dokumentacja jest lepsza)

## Co znajduje testowanie statyczne?

![4wQZt1.png](https://iili.io/4wQZt1.png)

## Proces przeglądu

### Planowanie

- ustalenie celów przeglądu
- wybór uczestników przeglądu
- przydzielenie odpowiednich ról uczestnikom
- ustalenie kryteriów wejścia i zakończenia
- ustalenie zakresu przeglądu
- sprawdzenie kryteriów wejścia

## Rozpoczęcie przeglądu

- rozesłanie dokumentów do uczestników przeglądu wraz z opisem celów
- udzielenie odpowiedzi na ewentualne pytania uczestników dotyczące przeglądu

## Przegląd indywidualny (przygotowanie się do przeglądu)

- przygotowanie uczestników do spotkania przeglądowego (przejrzenie i analiza dokumentów)
- zapisanie potencjalnych defektów, pytań i komentarzy (np. w formie rejestru uwag)

## Przekazanie informacji o problemach i analiza problemów

- dyskusja nt. wykrytych problemów, zapisanie defektów i rekomendacji ich poprawy
- dokonanie oceny i udokumentowanie charakterystyk jakościowych
- dokonanie oceny wniosków z przeglądu pod kątem kryteriów wyjścia w celu podjęcia decyzji

## Usunięcie defektów i raportowanie

- utworzenie raportów o defektach
- usunięcie defektów wykrytych w produkcie pracy
- poinformowanie odpowiedniej osoby lub odpowiedniego zespołu o defektach
- zarejestrowanie zaktualizowanego statusu defektów
- zebranie miar
- sprawdzenie, czy zostały spełnione kryteria wyjścia
- zaakceptowanie produktu pracy

## Role w przeglądzie

**Kierownik przeglądu** - planuje przegląd, podejmuje decyzje, monitoruje postęp

**Lider Przeglądu** - ponosi odpowiedzialność, wyznacza role

**Facylitator/Moderator** - dba o przebieg spotkania, rozwiązuje problemy, ważna rola w dużych, formalnych spotkaniach

**Autor** - twórca przeglądanego produktu, dysponuje wiedzą, naprawia znalezione błędy

**Przeglądający** - osoby zaproszone do przeglądu by znajdować błędy. Eksperci z różnych dziedzin, reprezentujący różne interesy i punkty widzenia

**Protokolant** - w bardziej formalnych przeglądach jest dedykowana osoba do dokumentowania procesu i rejestrowana znalezionych błędów. Często zastępowany przez program.

### Typy przeglądów

Przegląd nieformalny (koleżeński)
![4wbrzB.png](https://iili.io/4wbrzB.png)

### Przejrzenie

![4wmJqX.png](https://iili.io/4wmJqX.png)

### Przegląd techniczny

![4wmrvf.png](https://iili.io/4wmrvf.png)
Ważne: Przeglądający powinni mieć odpowiednie kompetencje i przygotować się do przeglądu. Rola facylitatora jest niezbędna.

### Inspekcja

![4wmmYb.png](https://iili.io/4wmmYb.png)
WAŻNE: Najbardziej formalna technika, ma zdefiniowane kryteria wejścia/wyjścia, używane są listy kontrolne, autor nie może pełnić ważnej roli w przeglądzie, trzeba się przygotować, powstaje raport.

## Techniki przeglądu

### przegląd ad hoc

nieformalny, na luzie, bez przygotowania i z minimum dokumentacji. Najlepiej stosowany jako technika uzupełniająca lub na samym początku.

### przegląd oparty na liście kontrolnej

bardziej usystematyzowane podejście z zadaniami do “odfajkowania”

### scenariusze i przebiegi próbne

wykorzystuje scenariusze i przypadki użycia oraz proste listy kontrolne. Dobrze stosować wraz z innymi technikami, by nie pominąć innych błędów.

### przegląd oparty na rolach

analiza dokumentu wchodząc w rolę przyszłego użytkownika tego dokumentu

### czytanie oparte na perspektywie

bardziej rozbudowana wersja powyższego, gdzie przeglądający przyjmują perspektywę użytkowników końcowych (administracja, marketing, inni interesariusze). Stosuje się listy kontrolne i tworzy dokumentację.
