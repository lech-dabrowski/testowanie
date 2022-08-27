# II - Testowanie w cyklu życia oprogramowania

## Dobre praktyki

każda czynność związana z wytworzeniem oprogramowania ma odpowiadające jej 

- każdy poziom testowania ma zdefiniowane cele
- analiza i projektowanie testów rozpoczyna się wraz z analizą i projektowaniem oprogramowania
- klient jest zaangażowany w projekt na wczesnym etapie
- poziomy testowania są dostosowane do specyfiki projektu i architektury systemu
- testerzy uczestniczą w dyskusjach dotyczących definiowania wymagań

## Modele wytwarzania

![4T3Hx9.jpg](https://iili.io/4T3Hx9.jpg)
Model sekwencyjny w którym czynności testowe zaczynają się jak najwcześniej - na przykład definiując wymagania zaczynamy planować testy akceptacyjne.

![4T3KUx.jpg](https://iili.io/4T3KUx.jpg)
Schemat modelu SCRUM w którym tester jest częścią zespołu uczestniczącego w sprintach.

## Poziomy testów

![4T3RUv.jpg](https://iili.io/4T3RUv.jpg)
Dla każdego poziomu testów możemy wyróżnić:

- podstawę testów
- przedmiot testów
- cele testowania
- typowe defekty i awarie
- środowisko testowe
- zakres obowiązków poszczególnych osób

## Testy modułowe

Testy wykonywane najczęściej przez programistów, ma modułach, które da się wywołać oddzielnie.
![4T3V0G.jpg](https://iili.io/4T3V0G.jpg)
Na kolejnych slajdach pojawiło się pojęcie TDD - Test Driven Development. Chyba taka bardziej ciekawostka - najpierw tworzy się testy a potem funkcjonalność. Niby fajne bo testy jako dokumentacja są zawsze aktualne a błędy znajduje się i naprawia szybko i tanio, ale brzmi to niepraktycznie i jedną z wade jest właśnie potrzeba dyscypliny w zepole.

## Testy integracyjne

Integrujemy albo moduły albo systemy (np. integrację istniejącego systemu sklepu internetowego z mikrousługą od płatności). Podstawą takich testów są projekty, diagramy i specyfikacje zaś przedmiotem są najczęściej podsystemy, bazy danych i interfejsy.
![4T3imB.jpg](https://iili.io/4T3imB.jpg)

### Podstawowe zasady integracji:

- Integrujemy tylko dwa moduły/systemy jednocześnie.
- poszczególne moduły lub systemy powinny być integrowane tylko raz
- kolejność i harmonogram integracji powinny być udokumentowane

## Strategie integracji

![4TFBrG.jpg](https://iili.io/4TFBrG.jpg)
Strategie są różne i chyba nie tak super ważne, ale na powyższym diagramie widać kilka ciekawych rzeczy: moduły 4 i 6 są krytyczne (można je przetestować jako piwersze), moduły 1, 2 i 5 można przetestować po kolei, zaś moduł 4 testujemy tylko z 3.

W sytuacji, gdy na potrzeby przeprowadzenia testu modułu trzeba zasymulować resztę systemu, tworzymy **jarzmo testowe** składające się ze **sterowników** (coś, co symuluje dane wejściowe wywołujące testowany moduł) oraz **zaślepek** (symuluje zachowanie modułu wywoływanego przez ten obecnie testowany)

### Programy używane w testach integracyjnych

![4TFN3J.jpg](https://iili.io/4TFN3J.jpg)

### Testy systemowe

Pierwsze testy całego systemu. Powinny być wykonywane przez niezależny zespół testerski (świeże spojrzenie, brak stronniczości). Jest to poziom na którym przeprowadzane są pełne scenariusze testowe (np. od zalogowania się do upuszczenia serwisu - tzw. end-to-end)
![4TFLv4.jpg](https://iili.io/4TFLv4.jpg)

### Testy akceptacyjne

Podstawą testów akceptacyjnych jest plan dotychczas wykonanych testów oraz informacje o wymaganiach wobec finalnego produktu. Jednym z założeń jest, by były wykonywane przez zespół pracowników twórcy systemu oraz jego odbiorcy.
![4TK28x.png](https://iili.io/4TK28x.png)
Testy akceptacyjne dzielimy ze względu na charakter akceptowanej cechy na:

- **Akceptację użytkownika (User Acceptance testing - UAT)** - testujemy czy finalny produkt spełnia potrzeby docelowej grupy użytkowników.
- **Akceptację zgodności operacyjnej (Operational Acceptance Testing - OAT)** - testowana jest wydajność systemu, obsługa błędów, współpraca z innymi systemami w firmie, możliwość robienia kopii zapasowych, instalowania/odinstalowywania, czynności pielęgnacyjnych itd.
- **Akceptację wymagań kontraktu -** sprawdzenie czy produkt końcowy spełnia wymagania określone w umowie sporządzonej na początku prac.
- **Akceptację legislacyjną** - należy określić, czy oprogramowanie spełnia wszystkie normy i przepisy charakterystyczne dla danego obszaru biznesowego.

Warto pamiętać o testach **alfa** oraz **beta** (testy wykonywane przez przyszłych użytkowników, alfa w siedzibie firmy oraz beta we własnych lokalizacjach)

## Typy testów

### Testowanie funkcjonalne

Testuje jak działa dany system. Podstawą testów są przypadki użycia, historyjki użytkownia oraz wymagania stawiane systemowi. Używamy technik czarnoskrzynkowych.
![4TKrNV.png](https://iili.io/4TKrNV.png)

### O przypadkach testowych, warunkach i wymaganiach słów kilka:

**Wymaganie** pojawia się na samym początku rozmów o tym, co oprogramowanie ma robić. Na etapie planowania testów, w oparciu o wymagania przygotuwuje się **warunki testowe**. Warunki są zazwyczaj wysokopoziomowe (zalogowanie się, odblokowanie konta) i używa się ich jako podstawy do stworzenia bardziej szczegółowych **przypadków testowych.**

Przypadek testowy składa się z:

- Warunków wstępnych
- Danych wejściowych
- Akcji do wykonania
- Oczekiwanych rezultatów i warunków końcowych

Przypadki można pogrupować w **zestawy testów,**

### Testowanie niefunkcjonalne

Celem testowania niefunkcjonalnego jest ocena określonych charakterystyk (bezpieczeństwo, niezawodność itd.). Jest to nadal test dynamiczny (odpala się program) zaś jego podstawą jest albo specyfikacja wymagań albo przypadki i historyjki użytkownika.
![4TKQKg.png](https://iili.io/4TKQKg.png)
Jest cała magiczna norma (na razie odmawiam uczenia się tych cyferek ale w tym przypadku to ISO/IEC 25010) która wymienia charakterystyki jakościowe systemu:
![4TKtUJ.png](https://iili.io/4TKtUJ.png)

**Wydajność** testujemy przeprowadzając testy wydajnościowe (stałe obciążenie), obciążeniowe (chwilowy skok obciążenia, np. standardowo 1000 użytkowników a podczas weekendowej promocji 5000) oraz przeciążeniowe (np. 10000 użytkowników by sprawdzić obsługę błędów)

**Bezpieczeństwo** oraz testowanie podatności na ataki jest opisane mega skrótowo w materiałach, ale mam nadzieję, że to będzie taki mój konik przez najbliższe lata. Można sprawdzać jak system uwierzytelnia i autoryzuje dostęp, jak wygląda walidacja danych wejściowych (czy można przeprowadzić *SQL injection*), testować odporność na *Denial of Service* lub jak aplikacja radzi sobie z podszywaniem się pod innych użytkowników.

**Użyteczność** obejmuje takie zagadnieia jak czytelność serwisu, dostępność dla ludzi ze specjalnymi potrzebami (w niektórych krajach jak UK jest to ważna kwestia legislacyjna) oraz to jak łatwo dany serwis się obsługuje w porównaniu do innych podobnych. Można testować z podziałem na role (np. czytelność mapy dla starszej osoby) i w oparciu o doświadczenie.

### Testowanie białoskrzynkowe

nie mam pojęcia co robi tutaj, bo jest szczegółowo opisane w rozdziale 4 a poza tym zachodzi podejrzenie, że to całe testowanie pokrycia kodu wyleciało z zakresu na ISTQB.
![4TKpNp.png](https://iili.io/4TKpNp.png)

### Testowanie związane ze zmianami

Test potwierdzający, inaczej retest sprawdza czy zgłoszona usterka została naprawiona. Wykonuje się ten sam test, który usterkę ujawnił i oczekuje się, że jego ponowne wykonanie nie ujawni błędu. Test jest prosty i z reguły się go nie automatyzuje.
![4TfdiX.png](https://iili.io/4TfdiX.png)
Test regresji ma na celu sprawdzenie czy modyfikacja kodu, która naprawiła wspomniany błąd nie spodowowała błędów w innych częściach aplikacji. Jeżeli naprawiony błąd przykładowo blokował dostęp do części funkcjonalności, należy przetestować czy jest ona wolna od usterek. Ze względu na swój czasochłonny charakter testy regresji są często automatyzowane.
![4TfFls.png](https://iili.io/4TfFls.png)

### Ważna tabelka

Przy każdym typie testów było napisane, że można go wykonywać na każdym poziomie. Poniższa tabelka daje praktyczny przykład jak wyglądają różne typy testów (funkcjonalne, niefunkcjonalne itd.) na poszczególnych poziomach (modułowe, systemowe, akceptacyjne itd.)
![4TfY5x.png](https://iili.io/4TfY5x.png)

### Testowanie pielęgnacyjne
Jest ważne dla utrzymania jakości przez cały cykl życia produktu. Zwłaszcza w zakresie:

- niezawodności
- kompatybilności
- bezpieczeństwa
- przenaszalności

Wydarzenia, które mogą zainicjować testowanie pielęgnacyjne to:

- Modyfikacja oprogramowania (poszerzenie funkcjonalności, patche, hotfixy)
- Migracja (np. przeniesienie na inny serwer, nową wersję systemu operacyjnego)
- Wycofanie (testujemy wtedy możliwości archiwizacji i procedur odzyskania danych)

Przykładowe czynności będące w zakresie testowania pielęgnacyjnego:

- testowanie wprowadzonych poprawek na wszystkich poziomach i typach testów
- testy regresji, których zakres ustala analiza wpływu

Zakres testów pielęgnacyjnych zależy przede wszystkim od poziomu ryzyka niesionego przez wprowadzone zmiany. Rozmiar zmian oraz całego systemu ma również znaczenie.

**Analiza wpływu** - Identyfikacja wszystkich produktów pracy, na które zmiana ma wpływ, w tym oszacowanie zasobów potrzebnych do przeprowadzenia zmiany. Jej cele to ocena zmian wprowadzonych w werji pielęgnacyjnej oraz identyfikacja obszarów systemu na które zmiany będą miały wpływ.