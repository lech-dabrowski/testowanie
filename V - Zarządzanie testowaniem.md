# V - Zarządzanie testowaniem

## Niezależne testy - po co i dlaczego?

### Poziomy niezależności:

- brak niezależnych testerów - twórcy testują własne produkty,
- niezależni testerzy wewnątrz zespołu projektowego,
- niezależny zespół testowy lub grupa testerów wewnątrz organizacji podlegająca kierownikowi projektu lub zarządowi,
- niezależni testerzy z departamentów biznesowych lub społeczności użytkowników,
- niezależni specjaliści, wynajęci lub wewnątrz organizacji, do określonych typów testów takich jak użyteczności, zabezpieczeń lub certyfikatów

Testy niezależne są fajne, ale kosztują i mogą mieć inne wady, więc decyzja zawsze jest zależna od  kontekstu projektu (budżet, czas, poziom ryzyka). Częstą praktyką jest wykonywanie części testów samodzielnie (np. testy modułowe) oraz korzystanie z testów niezależnych tam, gdzie brakuje ekspertyzy (np. ekspertów do testów akceptacyjnych) lub zasobów.

### Wady i zalety

![4Nz5v4.png](https://iili.io/4Nz5v4.png)

### Zadania kierownika oraz testera

![4NzmcG.jpg](https://iili.io/4NzmcG.jpg)

### Plan testów

To taki über dokument, który postaje przed rozpoczęciem testów i ewoluuje przez cały czas trwania procesu (zmiany są śledzone, by wiedzieć kto i kiedy zmienił dany parametr po zatwierdzeniu dokumentu). W zależności od kontekstu projektu może (ale nie musi) zawierać następujące pola:

1. **Identyfikator planu testów**
2. **Wprowadzenie**
3. **Opis przedmiotu testów**
4. **Zakres testów**
   Obszary, które będą testowane. Może się okazać, że testowany produkt ma wiele innych funkcji, ale zakres testów obejmuje np. tylko bezpieczeństwo.
   Chyba też tutaj bym wrzucił kryteria wejścia (jakie warunki są niezbędne by w ogóle rozpocząć testy - na przykład działająca wersja aplikacji i dostęp do konkretnej bazy danych)
5. **Wyłączenie z zakresu**
   WAŻNE: może się okazać, że części wymagań nie da się spełnić, części funkcji nie da się przetestować, w związku z czym należy na wczesnym etapie wyłączyć je z zakresu i uzyskać zatwierdzenie klienta.
6. **Podejście do testowania**
   Tu wlatuje opis strategii testów (temat - rzeka, o tym będzie później). Generalnie ten punkt opisuje na co kładziony będzie największy nacisk podczas tego konkretnego procesu.
7. **Kryteria zaliczenia/nie zaliczenia testów**
8. **Kryteria zawieszenia/wznowienia**
9. **Produkty pracy (testalia oraz artefakty)**
10. **Czynności i zadania testowe**
11. **Środowiska testowe**
12. **Role i odpowiedzialność**
13. **Potrzeby szkoleniowe**
14. **Harmonogram**
15. **Ryzyka i plany awaryjne**
16. **Zatwierdzenie planu**

## Strategie testów i podejście do testowania

Wybór strategii ma wpływ na to jakie techniki zostaną użyte oraz jakie typy i poziomy testów będą zdefiniowane dla projektu. Ma też wpływ na ustalenie kryteriów wejścia/wyjścia.

### Strategia analityczna

- Testy oparte na ryzyku
- Priorytety ustalane na podstawie analizy ryzyka oraz wymagań

### Strategia oparta na modelu

- testy projektuje się na podstawie modelu konkretnego aspektu produktu
- odnoszę wrażenie, że ani Coders Lab ani autorzy sylabusa tak naprawdę nie wiedzą o co chodzi

### Strategia metodyczna

- testy są projektowane w oparciu o ustalone wcześniej warunki testowe wynikające z wymagań danej dziedziny biznesowej (np. testując system dla linii lotniczych koncentrujemy się na testowaniu wydajności i niezawodności)
- ta strategia zakłada użycie list kontrolnych oraz stosowanie ataków usterkowych

### Strategia zgodna z procesem

- Testy są projektowane tak, by spełnić konkretne normy danego obszaru biznesowego (np. linie lotnicze, bankowość, podejrzewam, że jakiś zaawansowany przemysł lub farmaceutyka)

### Strategia konsultatywna (kierowana)

### Strategia minimalizująca regresję

- Planowanie testów opiera się na wytycznych od interesariuszy lub ekspertów w danej dziedzinie
- Zakłada się takie projektowanie testów, by testy regresji (sprawdzające czy wprowadzone zmiany nie spowodowały defektów/awarii gdzie indziej) były możliwie łatwe i przyjemne. Tworzy się automatyczne skrypty testowe.

### Strategia reaktywna

- Testowanie jest ukierunkowane na to, by reagować na zdarzenia zamiast działania według ustalonego planu.
- Wykorzystuje testowanie eksploracyjne i techniki oparte na doświadczeniu
- Brzmi jak dziadostwo

Warto wspomnieć, że w zależności od kontekstu projektu różne strategie można łączyć.

## Kryteria wejścia i wyjścia (definicje gotowości i ukończenia)

![4Nu8P9.png](https://iili.io/4Nu8P9.png)

### Przykłady kryteriów wejścia:

- dostępność możliwych do testowania wymagań, historyjek i modeli
- dostępność i gotowość środowiska testowego
- gotowość narzędzi testowych
- podstawa testów jest dostępna do testowania (np. kod)

### Przykłady kryteriów wyjścia:

- zakończenie zaplanowanych zadań
- osiągnięcie wymaganego poziomu pokrycia
- estymaty gęstości błędów lub miar niezawodności (lol, skopiowałem słowo w słowo jak bylo w materiałach)
- nieprzekroczenie uzgodnionych limitów defektów (np. brak błędów krytycznych, obecnych parę nieistotnych dupereli, których nikomu nie chciało się naprawić)

## Określenie pracochłonności testowania

### Charakterystyka produktu

- ryzyko
- jakość podstawy testów
- wymagania
- wielkość i złożoność produktu

### Rezultaty testów

- liczba wykrytych błędów
- wyniki retestów i regresji

### Proces wytwarzania oprogramowania

- stabilność i dojrzałość organizacji
- dostępność narzędzi
- proces testowy i presja czasu

### Czynniki ludzkie

- umiejętności i doświadczenie zespołu
- kultura pracy, skuteczność kierownictwa

## Ryzyko

![4Nufvj.png](https://iili.io/4Nufvj.png)
![4NA60X.jpg](https://iili.io/4NA60X.jpg)

## Ryzyko projektowe > ryzyko produktowe

### Macież ryzyk:

![4N5T67.png](https://iili.io/4N5T67.png)

### Analiza wpływu ryzyka (ryzyko = prawdopodonieństwo * wpływ)

![4N558u.png](https://iili.io/4N558u.png)

Z powyższej tabelki wynika przykładowo, że choć szansa na wystąpienie ryzyka 2 jest bardzo mała, to jednak jest na tyle poważne, by mieć najwyższy poziom.
