# Ursus C-330 / C-330M — Farming Simulator 25

Repozytorium analizy i rozwoju moda Ursus C-330 / C-330M 4x2. Autorzy: **StrielokPL**, Speedy, Miziuu.

## Wydania i lista zmian

- [0.0.5.0 P1 — ogranicznik biegu roboczego i diagnostyka](https://github.com/StrielokPL/ursus330G/releases/tag/0.0.5.0P1): biegi według aktywnego limitu narzędzia, redukcja przy przeciążeniu, ochrona przed oscylacją i pełna diagnostyka.
- [Opis zmian P1](.release/notes.md).
- [Historia zmian](CHANGELOG.md).

Projekt został zaimportowany z paczki 1.1.2.0, a numeracja została rozpoczęta od nowa. Pierwszą udokumentowaną bazą przebudowy jest 0.0.0.2. Stabilna baza kariery 0.0.4.3 stanowi historyczny punkt odniesienia; opublikowane w tym repozytorium P1 jest wydaniem wstępnym.

## Najważniejsze zmiany przebudowy

- Fabryczna automatyczna skrzynia 6F/2R: I/1→I/2→I/3→II/1→II/2→II/3; start zależny od masy i ochrona obrotów/obciążenia.
- Minimalne 2 s przed zmianą w górę i ochrona dużego skoku II/2→II/3.
- Opcjonalny odczyt Advanced Damage System; błędne próbki zastępowane natywnym obciążeniem GIANTS.
- Masa bazowa C-330 1675 kg, naciski około 38/62; przedni balast 42 kg, tylne metalowe warianty 40/144/184 kg. Pełny balast metalowy 226 kg, łącznie około 1901 kg.
- Suche opony: spring=12, damper=22, suspTravel=0.07 m.
- Niezależna woda w tylnych oponach: +132 kg na koło, +264 kg łącznie, około spring=14/damper=30.
- MudSystemPhysics zachowuje sterowanie ciśnieniem, promieniem i tarciem.
- Lokalna kolejność sklepu: silnik→koła→woda→przedni balast→kabina→konsola ładowacza.
- Static Cabins usuwa 18 kabinowych movingTool, powiązane sterowanie i animacje; kabiny pozostają geometrią statyczną. Poprawka odzyskuje 18 flag synchronizacji.
- P1 dodaje C330TransmissionWorkFix i wyznacza sufit biegu roboczego zapewniający co najmniej 1500 obr./min przy limicie narzędzia.
- Redukcja przy zbyt niskich obrotach oraz 2,5 s ochrony po redukcji i podniesieniu pracującego narzędzia.
- Zintegrowany rejestrator C330FULLDIAG zapisuje również wszystkie cztery koła W1–W4.

## Znane błędy i ograniczenia

- Multiplayer bieżącej przebudowy nie jest w pełni zweryfikowany.
- Historyczne potwierdzenie Static Cabins z ADS 0.9.2.4 i AIASF nie stanowi potwierdzenia całego bieżącego sterownika.
- P1 zawiera diagnostykę; pełne wydania usuwają C330FullDiagnostic.lua, zachowując poprawkę skrzyni.
- Dane jednoosobowe nie potwierdzają zachowania sieciowego.

## Dokumentacja

- [Baza techniczna C-330](docs/FS25_C330_TECHNICAL_BASELINE.md)
- [Status weryfikacji](docs/VALIDATION_STATUS.md)
- [Geneza poprawki Static Cabins i AIASF](https://github.com/StrielokPL/Farming25fixnmix)
