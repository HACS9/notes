---
title: "Metodyka"
description: "Jak liczę wyniki, benchmarki i obsunięcia."
---
## Wyniki

- Wszystkie wyniki w złotych (PLN), po przeliczeniu kursem średnim NBP z dnia notowania.
- Wynik portfela jest **ważony czasem** – wpłaty i wypłaty nie zmieniają wyniku. Dla eksperymentów podaję też stopę zwrotu uwzględniającą moment wpłat (XIRR).
- Okresy miesięczne liczone na ostatnią wycenę miesiąca.

## Benchmarki

- Fundusze z benchmarkiem podanym w karcie funduszu – porównanie z wartościami z karty.
- Benchmarki złożone z indeksów GPW (np. mWIG40TR, sWIG80TR, WIG) – składane miesięcznie z wag.
- Zamiast WIBOR/WIBID używam indeksu **POLSTR** (GPW Benchmark) – WIBOR jest wygaszany i nie ma darmowego źródła danych.
- Punkty odniesienia o stałej stopie (obligacje, lokata): naliczanie dzienne, kapitalizacja roczna, przed podatkiem.

## Ryzyko

- **Obsunięcie** – spadek od najwyższej dotychczasowej wartości.
- Korelacja z S&P 500 (12 miesięcy, stopy miesięczne). Dopóki portfel ma krótszą historię, liczę ją *pro forma* – na wagach docelowych i historii składników.

## Ocena eksperymentów

Każdy eksperyment ma protokół z horyzontem, progiem sukcesu i kryteriami porażki, zapisany przed startem. Po horyzoncie status to: **sukces**, **porażka** albo **nieudowodnione**. Przed końcem horyzontu podaję wyłącznie status bieżący.

## Jakość danych

Notowania z pojedynczymi błędnymi rekordami (skok i powrót następnego dnia) są pomijane. Okresy z wątpliwymi danymi oznaczam i nie wyciągam z nich wniosków do czasu weryfikacji.
