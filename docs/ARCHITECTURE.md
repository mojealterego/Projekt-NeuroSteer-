# NeuroSteer — architektura referencyjna

## Cel
Badawczo-produkcyjna platforma interpretowalności i kontrolowanego steeringu modeli open-weight.

## Komponenty
1. **Model adapters** — lokalne/hostowane modele z autoryzowanym dostępem do aktywacji.
2. **Activation collector** — sampling, bezpieczny storage i manifesty datasetów.
3. **SAE research** — TopK, Group-SAE/AMAD, SAE-NO i ocena stabilności.
4. **Feature registry** — wersjonowane słowniki, lineage, quality gates i etykiety.
5. **Steering compiler** — wektory, warstwy, skalowanie i ograniczenia.
6. **Inference data plane** — hooks, polityki interwencji, izolacja i fallback.
7. **Control plane** — tenancy, RBAC, API, audyt, konfiguracja i wersjonowanie.
8. **Evaluation plane** — benchmarki, red-team, obserwowalność i raporty.

## Granice zaufania
Nigdy nie zakładaj dostępu do hidden states modeli zamkniętych przez zwykłe API. Separuj uprawnienia treningu, publikacji wektorów i wykonania inferencji. Dane i aktywacje traktuj jako potencjalnie wrażliwe. Wdrożenia regulowane wymagają odrębnej walidacji i kontroli prawnej.

## Zasady naukowe
Group-SAE i SAE-NO są torami badawczymi, nie potwierdzoną przewagą. Cel 50% oszczędności i <50 ms to hipotezy mierzone wobec zdefiniowanych baseline'ów. Steering nie daje gwarancji eliminacji halucynacji, biasu ani wycieków PII.

## Źródło
Projekt Aplikacji Grantowej SPC.PDF (10 stron), dostarczony przez właściciela projektu, stanowi źródło wymagań koncepcyjnych; twierdzenia finansowe, programowe i badawcze wymagają niezależnej weryfikacji.
