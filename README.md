# SnakeGame

## Opis projektu

**SnakeGame** to prosta gra konsolowa napisana w języku **C#**, której celem jest sterowanie wężem poruszającym się po planszy i zbieranie punktów poprzez zjadanie pojawiających się przeszkód (elementów reprezentujących jedzenie).

Projekt został wykonany w ramach ćwiczeń z **pracy zdalnej w systemie Git oraz współpracy zespołowej z wykorzystaniem platformy GitHub**.

Podczas realizacji projektu wykorzystano następujące mechanizmy:

- repozytorium zdalne GitHub
- klonowanie repozytorium
- tworzenie gałęzi (branches)
- commitowanie zmian
- wysyłanie zmian (push)
- pull request
- przegląd i scalanie zmian
- zarządzanie zadaniami poprzez **Issues**

Gra działa w **konsoli systemowej** i została zaprojektowana jako prosty projekt edukacyjny pokazujący podstawowe mechaniki gier oraz pracę z kontrolą wersji.

---

# Zasady gry

Celem gry jest zdobycie jak największej liczby punktów poprzez sterowanie wężem i zbieranie elementów pojawiających się na planszy.

### Podstawowe zasady

- gracz steruje wężem za pomocą klawiszy strzałek
- wąż porusza się po planszy ograniczonej ścianami
- na planszy pojawia się element reprezentujący jedzenie
- po zebraniu elementu gracz zdobywa punkt
- długość węża zwiększa się po zdobyciu punktu

Gra kończy się w przypadku kolizji:

- ze ścianą
- z własnym ciałem

Po zakończeniu gry wyświetlany jest komunikat **Game Over** wraz z wynikiem punktowym.

---

# Sterowanie

Sterowanie odbywa się przy pomocy klawiszy strzałek na klawiaturze.

| Klawisz | Funkcja |
|--------|--------|
| ↑ | ruch w górę |
| ↓ | ruch w dół |
| ← | ruch w lewo |
| → | ruch w prawo |

Program odczytuje naciśnięcia klawiszy w czasie rzeczywistym i zmienia kierunek ruchu węża.

---

# Mechanika gry

Gra działa w pętli programu, która wykonuje następujące operacje:

1. rysowanie planszy gry w konsoli  
2. wyświetlanie aktualnego wyniku  
3. rysowanie głowy i ogona węża  
4. odczytywanie wejścia z klawiatury  
5. aktualizacja pozycji węża  
6. sprawdzanie kolizji  
7. generowanie nowej przeszkody po zdobyciu punktu  

Pozycja elementów gry jest przechowywana w postaci współrzędnych **X oraz Y**.

---

# Struktura projektu

Projekt składa się z kilku plików źródłowych odpowiedzialnych za różne elementy działania gry.

## Snake.cs

Główny plik programu zawierający:

- logikę gry
- obsługę sterowania
- rysowanie planszy
- sprawdzanie kolizji
- aktualizację pozycji węża
- obsługę punktacji

W tym pliku znajduje się **główna pętla programu (`while`)**, która odpowiada za działanie gry.

---

## Pixel.cs

Plik definiujący klasę **Pixel**, która reprezentuje pojedynczy element na planszy.

Klasa przechowuje:

- pozycję X
- pozycję Y
- kolor elementu
- znak reprezentujący element na ekranie

Obiekty tej klasy są wykorzystywane do reprezentowania segmentów węża.

---

## Obstakel.cs

Plik definiujący klasę **Obstakel**, która reprezentuje element pojawiający się na planszy, będący celem do zebrania przez węża.

Klasa zawiera:

- współrzędne X
- współrzędne Y
- kolor elementu
- znak wyświetlany na ekranie

Po zebraniu przeszkody generowana jest nowa w losowej pozycji.

---

# Wymagania systemowe

Do uruchomienia projektu wymagane jest środowisko:

- **.NET SDK**
- system operacyjny obsługujący aplikacje konsolowe

Projekt był testowany w środowisku:

- Windows
- .NET

---
