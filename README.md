# NeuroSteer

> **UWAGA — PRZECZYTAJ PRZED ROZPOCZĘCIEM PRACY W REPOZYTORIUM. ZAKAZ SAMOWOLNYCH ZMIAN ZAKRESU I ROADMAPY.**

Research and engineering platform for mechanistic interpretability, sparse autoencoders and inference-time activation steering.

## Status

**Inicjalizacja projektu.** Nie ma jeszcze dowodów na skuteczność sterowania, redukcję kosztów ani gotowość produkcyjną.

## Zakres

- Mechanistic interpretability i rejestracja aktywacji modeli open-weight.
- TopK SAE: trening, rekonstrukcja, sparsity, stabilność i ocena interpretowalności.
- Group-SAE: grupowanie warstw na podstawie AMAD, benchmark względem SAE per-layer.
- SAE-NO: niezależny tor eksperymentalny z kontrolowanymi baseline'ami.
- Activation Addition: kontrolowane, odwracalne interwencje w modelach z dostępem do stanów ukrytych.
- Real-Time Steering API: autoryzacja, polityki, audyt, izolacja tenantów i metryki opóźnień.

**Granica techniczna:** zewnętrzne API zamkniętych modeli bez dostępu do aktywacji nie pozwala na bezpośrednie activation steering. Możliwe są jedynie osobne mechanizmy wejścia/wyjścia, których nie wolno przedstawiać jako sterowania stanami ukrytymi.

## Dokumenty

- [ROADMAP.md](ROADMAP.md) — kanoniczna mapa drogowa i kryteria odbioru.
- [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md) — architektura docelowa i ograniczenia.

## Zasady

1. Przed zmianami przeczytaj README, ROADMAP i architekturę.
2. Nie usuwaj, nie skracaj ani nie przemieszczaj pozycji ROADMAP bez wyraźnego polecenia.
3. Nowe wymagania dopisuj z identyfikatorem i kryteriami odbioru.
4. Oznaczaj jako wykonane tylko po dostarczeniu weryfikowalnych dowodów.
5. Nie deklaruj wdrożenia, audytu zewnętrznego ani wyników benchmarków bez pomiarów.
