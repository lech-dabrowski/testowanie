# IV - Techniki Projektowania Testów

## Wybór technik testowania

Czynniki wpływające na wybór techniki testowania:

- Typ modułu lub systemu, wymagania klienta czas i budżet
- Poziom ryzyka
- przewidywany sposób korzystania, doświadczenie zespołu i typowe defekty

Stopień sformalizowania wybranych technik zależy od:

- dojrzałości procesów w firmie
- ograniczeń czasowych
- ewentualnych wymagań

W praktyce najdoskonalsze efekty uzyskuje się poprzez zastosowanie wypadkowej wynikającej z doświadczenia, teorii, znajomości użytej technologii oraz intuicji.

## Kategorie technik testowania

![4Nq4yP.png](https://iili.io/4Nq4yP.png)
![4NBWiJ.png](https://iili.io/4NBWiJ.png)

## Techniki czarnoskrzynkowe

### Podział na klasy równoważności

Jest to podział na podzbiory (inaczej klasy abstrakcji) powodujące to samo zachowanie systemu.
![4NB6l4.png](https://iili.io/4NB6l4.png)

Dla pełnego pokrycia należy przetestować **conajmniej jeden** przypadek z **każdej** klasy.
Jeśli w przypadkach testowych są stosowane niepoprawne klasy równoważności, należy je testować indywidualnie aby uniknąć maskowania awarii.

### Analiza wartości brzegowych

Rozszerzenie techniki testowania klas równowazności, ale stosowana tylko dla **uporządkowanych klas**, kóre zawierają **dane liczbowe lub sekwencyjne**.

![4NCerx.png](https://iili.io/4NCerx.png)
Analiza wartości brzegowych może zostać zastosowana na każdym poziomie testowania.
Na egzaminie do analizy wartości brzegowych zakładamy technikę trzypunktową

### Tablice decyzyjne

Tablica decyzyjna przedstawia kombinację wejść (warunków) z odpowiadającymi wyjściami (akcjami). Używamy ich do:

- złożonych reguł biznesowych, które oprogramowanie musi realizować
- wymagań zawierających warunki i zależności logiczne
- tablice decyzyjne mogą być wykorzystywane na każdym poziomie testów, gdzie działanie systemu zależy od kilku decyzji logicznych.
  ![4NnXvp.jpg](https://iili.io/4NnXvp.jpg)

### Przejścia między stanami

Czarnoskrzynkowa technika projektowania przypadków testowych, w której przypadki są projektowane tak, aby sprawdzały dozwolone oraz niedozwolone przejścia między stanami. Podejście to pozwala:

- określić stany, w których może się znaleźć system
- wskazać możliwe przejścia między poszczególnymi stanami
- określić zdarzenia i warunki, które powodują przejścia pomiędzy stanami

![4NnwuI.png](https://iili.io/4NnwuI.png)

Powyższy diagram **maszyny stanowej** zawiera:

- **Poszczególne stany** w jakich dany system się może znaleźć (stan początkowy, końcowy, stany pośrednie) w tabelkach oznaczane S1, S2 itd.
- **Przejścia** pomiędzy nimi (oznaczone strzałkami)
- **Zdarzenia/Akcje** (nad strzałkami) opisujące co się dzieje na danym etapie
- schemat tego nie uwzględnia, ale ważne sa treż **warunki dozoru** (kryteria niezbędne by dane zdarzenie miało miejsce lub by akcja była możliwa do wykonania)

Projektowanie przypadków testowych w oparciu o diagram maszyny stanów polega na opracowaniu testów weryfikujących np.:

- pokrycie każdego stanu
- wykonanie typowej sekwencji
- wykonanie specyficznej sekwencji przejść
- przetestowanie przejść niedozwolonych

Testowanie przejść między stanami może być wykorzystane na każdym poziomie testów, wszędzie tam, gdzie istnieją obiekty posiadające różne stany.

### Przypadki użycia

Przypadki użycia (ang. use cases) są powszechnie wykorzystywane do opisu wymagań funkcjonalnych. Odnoszą się one do interakcji pomiędzy systemem a użytkownikiem i są opisem sekwencji kroków (zdarzeń), opisują przepływ procesu przez system.

Każdy przypadek zawiera:

- warunki wstępne, które muszą zostać spełnione, żeby przypadek użycia został spełniony
- warunki końcowe, czyli widoczne dla aktora rezultaty wykonania przypadku oraz stan systemu po zakończeniu przypadku użycia
- podstawowe użycie, opisujący poszczególne czynności aktora niezbędne do osiągnięcia określonego celu
- może zawierać zachowanie wyjątkowe (alternatywne), która opisuje mniej prawdopodobne, choć dopuszczalne czynności aktora niezbędne do osiągnięcia określonego celu
- może zawierać mechanizm obsługi defektów - odpowiedź systemu i odtworzenie po wystąpieniu awarii wynikającego z pomyłki, defektu w aplikacji lub błędu komunikacji np. skutkującego komunikatem błędu.

Zalety:

- przypadki testowe wykrywają często awarie w przepływach procesów biznesowych
- użyteczne w projektowaniu testów akceptacyjnych z udziałem zespołu biznesowego
- pozwalają wykryć awarie integracji, powodowane przez brak współpracy poszczególnych modułów

![4NoqKJ.png](https://iili.io/4NoqKJ.png)

## Techniki białoskrzynkowe

### Testowanie i pokrycie instrukcji

Odsetek instrukcji wykonywalnych, które zostały przetestowane przez zestaw testowy.
![4Nojlj.png](https://iili.io/4Nojlj.png)
1, 2, 4, 5, 6 to różne instrukcje. 3 (else) nie jest traktowane jako instrukcja wykonywalna.

NA EGZAMIN: jeżeli będzie pytanie o zaprojektowanie **jak najmniejszej liczby** przypadków testowych, to warto by któryś z przypadków pokrywających 2 lub 4 pokrył także 5 (A równe 8)

### Testowanie decyzji

Odsetek możliwych wyników decyzji, które zostały przetestowane przez zestaw testowy. 100% pokrycia decyzji jest równoważny 100% pokrycia gałęzi oraz implikuje 100% pokrycia instrukcji.
![4NoUWF.png](https://iili.io/4NoUWF.png)
NA EGZAMIN: decyzje > instrukcje

### Testowanie kodu ogólnie

Metoda analityczna, określająca które części programu zostały wykonane (pokryte) przez zestaw testowy. Choć teoretycznie można stosować ją na każdym etapie projektu, to zdecydowanie najwięcej uzywa się jej w początkowych fazach testowania.

![4Nomsn.png](https://iili.io/4Nomsn.png)
![4Nx90G.png](https://iili.io/4Nx90G.png)

## Techniki oparte na doświadczeniu

Powszechną praktyką jest **zgadywanie defektów** - bazując na wiedzy, intuicji i doświadczeniu sporządza się listę możliwych, spodziewanych defektów i próbuje się wywołać awarie.

### Testowanie eksploracyjne

Jest to technika nieformalna, która powinna być uzupełnieniem innych, bardziej formalnych testów. Podczas **sesji testowej** (dobrze, by miała określony z góry czas) jednocześnie **projektuje** się testy, **wykonuje** je, oraz **zapisuje** ich wyniki.
TE stosuje się najczęściej gdy:

- Specyfikacji albo nie ma, albo jest niekompletna/przestarzała
- Jest mało czasu na wykonanie testów
- By uzupełnić bardziej formalne testy

Produktem pracy takiego testowania jest najczęściej **karta testów:**
![4Nxfz7.png](https://iili.io/4Nxfz7.png)

## Testowanie w oparciu o listę kontrolną

Wykaz czynności (zwykle z "okienkami" do "odfajkowania") przygotowywany dla skomplikowanych zadań w celu zapewnienia:

- właściwej (optymalnej) kolejności
- niepominięcia żadnego istotnego etapu postępowania.

Lista ma charakter wysokopoziomowy (ogólne przypadki, implementacja może wymagać doświadczenia od testera), można ją utworzyć dla **różnych typów testów** i na **róznych poziomach**. Listę można aktualizować wraz z rozwojem projektu.

![4Nxo0b.png](https://iili.io/4Nxo0b.png)
