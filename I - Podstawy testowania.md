# I - Podstawy testowania

## Czynności związane z tesotwaniem

- planowanie testów
- wybór warunków testowych
- projektowanie i wykonywanie przypadków testowych
- wykonywanie testów dynamicznych (przy uruchomionej aplikacji)
- testy statyczne (czytanie dokumentacji, przegląd kodu)
- raportowanie postępu
- ocena spełnienia kryteriów zakończenia
- kończenie i zamykanie testów

## Weryfikacja

Sprawdzenie (i dostarczenie obiektywnergo dowodu) czy produkt procesu wytwarzania oprogramowania spełnia zdefiniowane wymagania.
**Weryfikujemy zgodność ze specyfikacją.**

## Walidacja

Sprawdzenie i dostarczenie dowodu na to, że produkt spełnia wymagania i potrzeby użytkownika końcowego.
**Walidujemy poprawność i użyteczność aplikacji**

## Wskaźniki KPI (Key Performance Indicators) w procesie testowym:

- stosunek defektów krytycznych do wszystkich
- liczba zgłoszonych awarii/defektów
- średni czas na rozwiązanie defektu
- średni czas od zaraportowania do naprawy
- ilość czasu poświęconego na naprawę defektów vs. cały czas na tworzenie kodu
- pokrycie wymagań oraz kodu testami

![image](https://iili.io/4TJWUQ.jpg)

# Siedem zasad testowania

## 1. Testowanie ujawnia usterki

Sam fakt wykrycia usterki (wynik błędu programisty, przyczyna awarii systemu) nie wpływa na jakość produktu. Usterka musi zostać naprawiona, a po naprawie musi nastąpić retest potwierdzający, że została usunięta.

## 2. Testowanie gruntowne jest niemożliwe (i niepraktyczne)

Nie ma sensu testować 10 tysięcy kombinacji dla czterocyfrowego PINu jeżeli podanie dwóch/trzech sprawdzi tą samą funkcjonalność.

## 3. Wczesne testowanie oszczędza czas i pieniądze

Koszt naprawienia błędu rośnie wykładniczo wraz z postępem prac nad oprogramowaniem.
![image](https://iili.io/4T23yN.jpg)

## 4. Kumulowanie się defektów

Niewielka liczba modułów może zawierać większość błędów. Jest to brane pod uwagę przy analizie ryzyka i pozwala na poprawne określenie priorytetów dla zespołu testującego. Zasada Pareta mówi, że za 80% rezultatów odpowiada 20% przyczyn, ale każda mądra głowa ma swoją własną interpretację tego, jakie liczby są prawdziwe.

## 5. Paradoks pestycydów

W skrócie: powtarzanie w kółko tych samych testów sprawia, że stają się mniej skuteczne. Należy regularnie przeglądać i uaktualniać testy.

## 6. Testowanie zależy od kontekstu

Wybór techniki testowania powinien zależeć od rodzaju systemu, poziomu ryzyka i uwarunkowań biznesowych projektu (budżet, czas, wymagania klienta).

## 7. Przekonanie o braku błędów jest błędem :)

Po pierwsze, zawsze można coś przegapić. Dlatego zbieramy dupochrony w postaci dokładnej dokumentacji całego procesu. Poza tym nawet system wolny od błędów może nie spełnić oczekiwań użytkownika z powodów niefunkcjonalnych (wydajność, bezpieczeństwo, użyteczność). 

# Proces Testowy (model PAPIWU, hehe)

![image](https://iili.io/4TJCNt.jpg)

Info z sylabusa, którego nie było w materiałach:
Planowanie: Analiza - CO? należy przetestować
Projektowanie - JAK? należy przetestować
Implementacja - Czy mamy wszystko by rozpocząć testy?
