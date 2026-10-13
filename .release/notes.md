## 0.0.5.0 P1 — ogranicznik biegu roboczego i diagnostyka

### Lista zmian

- Dodana stała warstwa Scripts/C330TransmissionWorkFix.lua ponad C330TransmissionFix.
- Aktywny limit prędkości narzędzia GIANTS wyznacza najwyższy bieg zapewniający co najmniej 1500 obr./min: około 8,4 km/h→II/1, 13–15 km/h→II/2; wolniejsze narzędzia mogą pozostać w zakresie I.
- Wybrany bieg stanowi sufit zmian w górę; zbyt wysoki bieg po opuszczeniu narzędzia jest redukowany po jednym kroku.
- I/3→II/1 pod obciążeniem dopuszczone, gdy II/1 jest biegiem roboczym, obroty ≥2050 i upłynęło 2 s; usunięta blokada load≤0.55 dla tego przejścia.
- Redukcja przy gazie ≥0.85, obciążeniu ≥0.75 i obrotach ≤1450.
- Po redukcji oraz podniesieniu pracującego narzędzia obowiązuje 2,5 s blokady zmian w górę.
- Diagnostyka D2 C330FULLDIAG pozostaje aktywna; krzywe silnika, moment, przełożenia, balast i opony bez zmian.
- Diagnostyka REAR_WHEELS zapisuje W1–W4 (przód lewy/prawy, tył lewy/prawy), rozszerzając pomiar nacisków osi.

### Znane błędy i ograniczenia

- Wydanie wstępne; pomiary jednoosobowe nie potwierdzają zachowania multiplayer.
