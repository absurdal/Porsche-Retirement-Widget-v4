# Porsche Retirement Widget — wersja 3.0

Widget Android inspirowany srebrnymi zegarami Boxster 986. Grafika 1774 × 887 px z przezroczystym tłem; widget zachowuje proporcje, bez napisu nazwy na tarczach ani pod obudową.

- Środkowy wskaźnik: 0–700 dni, codzienny ruch wskazówki; wartości powyżej 700 są ograniczone do końca skali.
- Cyfrowe dni: rzeczywista liczba dni do 7 listopada 2028.
- Lewy wskaźnik: seksapil 46–54%, zmieniany deterministycznie każdego dnia.
- Prawy: stała wskazówka paliwa na rezerwie, świecąca kontrolka i temperatura.
- Odświeżanie po zmianie daty, uruchomieniu telefonu, zmianie rozmiaru oraz przez alarm dzienny.

## GitHub bez Android Studio

1. Utwórz **nowe puste repozytorium** (bez README), np. `Porsche-Retirement-Widget`.
2. Rozpakuj ZIP i prześlij **całą zawartość** (wraz z `.github/workflows/build.yml`) do repozytorium; zatwierdź zmiany.
3. Otwórz **Actions → Build Retirement986 APK**, poczekaj na zielony wynik.
4. Otwórz udany przebieg, pobierz artefakt `Retirement986-APK`, rozpakuj ZIP i zainstaluj `app-debug.apk`.

**Uwaga:** kod i bitmapa zostały przygotowane, ale APK tej wersji nie został lokalnie skompilowany ani przetestowany na telefonie. Pierwsza kompilacja GitHub Actions będzie testem. Grafika została retuszowana automatycznie, więc przy powiększeniu mogą być widoczne ślady po usuniętych wskazówkach.


## V4: wskazowka srodkowa

Oryginalna wskazowka i piasta zostaly usuniete z bitmapy i zastapione wskazowka rysowana dynamicznie z gradientem i cieniem. Skala: 0 dni = 155 stopni (dol-lewo), 700 dni = 360 stopni (prawo), wartosci >700 zatrzymuja sie na 7. Zachowana przezroczystosc PNG i proporcje 2:1. Test: ustaw date 07.11.2027, licznik powinien pokazac 366, wskazowka pomiedzy 3 a 4.

Wskazowka lewego zegara jest rowniez rysowana dynamicznie i zmienia sie raz na dobe (46-54%).
