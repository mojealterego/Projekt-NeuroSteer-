# NeuroSteer — kanoniczna ROADMAP

> **UWAGA: CZYTAĆ PO WEJŚCIU DO REPOZYTORIUM. ZAKAZ SAMOWOLI.** Nie wolno usuwać, skracać, nadpisywać ani przenosić istniejących wymagań bez wyraźnej dyspozycji właściciela. Każda zmiana wymaga historii i dowodu.

Stan na 2026-10-16: repozytorium zainicjalizowane. Wszystkie pozycje implementacyjne są otwarte. Kryteria mierzalne wymagają wyników z rzeczywistych eksperymentów.

## Etap 00 — fundamenty
- [ ] NS-001: Struktura monorepo, Python/Rust, zależności przypięte wersjami, lockfiles.
- [ ] NS-002: CI: lint, typing, unit, integration, security, SBOM i skan sekretów.
- [ ] NS-003: Reprodukowalne środowisko CPU/GPU, seed, manifest eksperymentu i provenance.
- [ ] NS-004: Polityka licencji modeli, zbiorów danych i artefaktów.
- [ ] NS-005: Threat model, polityka danych, RBAC, sekretów i izolacji tenantów.

## Etap 01 — badania bazowe
- [ ] NS-006: Adaptery modeli open-weight i przechwytywanie aktywacji z wybranych warstw.
- [ ] NS-007: Wersjonowany zbiór aktywacji, sampling, metadane, kontrola jakości i retencja.
- [ ] NS-008: TopK SAE: trening, checkpointy, inferencja i odtwarzanie wyników.
- [ ] NS-009: Metryki reconstruction loss, explained variance, L0, dead features, feature splitting.
- [ ] NS-010: Stabilność cech między seedami; dopasowanie i porównanie słowników.
- [ ] NS-011: Automatyczne etykietowanie cech z oceną jakości i ograniczeniami kosztu.

## Etap 02 — Group-SAE
- [ ] NS-012: Implementacja metryki AMAD i testy numeryczne.
- [ ] NS-013: Deterministyczne grupowanie warstw i analiza czułości hiperparametrów.
- [ ] NS-014: Wspólny SAE dla grup warstw i kompatybilny baseline per-layer.
- [ ] NS-015: Benchmark jakości, pamięci, FLOPs, czasu GPU i kosztu end-to-end.
- [ ] NS-016: Weryfikacja hipotezy redukcji kosztu do 50%, z przedziałami ufności i analizą trade-off.

## Etap 03 — SAE-NO
- [ ] NS-017: Specyfikacja operatora neuronowego i jego domeny, kontrakty tensorów.
- [ ] NS-018: Implementacja SAE-NO, testy gradientów i stabilności numerycznej.
- [ ] NS-019: Ablacje SAE-NO kontra TopK SAE i Group-SAE na identycznych danych.
- [ ] NS-020: Benchmark spójności cech, kosztu, rekonstrukcji i wpływu na steering.

## Etap 04 — sterowanie aktywacjami
- [ ] NS-021: Extraction i kalibracja steering vectors z zestawami kontrolnymi.
- [ ] NS-022: Runtime hooks do odwracalnej interwencji w stanach ukrytych.
- [ ] NS-023: Polityki intensywności, warstwy, zakresu tokenów, wyłączenia i rollback.
- [ ] NS-024: Ocena skuteczności na zadaniach, false positives, degradacji użyteczności i drift.
- [ ] NS-025: Adwersarialne testy prompt injection, PII i niepożądanych zachowań bez deklaracji gwarancji eliminacji.

## Etap 05 — Real-Time Steering API
- [ ] NS-026: Specyfikacja OpenAPI, kontrakty wersjonowane, walidacja wejścia i błędy.
- [ ] NS-027: Control plane i data plane z izolacją tenantów i zasadą least privilege.
- [ ] NS-028: Uwierzytelnianie, autoryzacja, rate limits, quotas, audyt i idempotencja.
- [ ] NS-029: Kolejkowanie, backpressure, timeouty, circuit breakers i graceful shutdown.
- [ ] NS-030: Observability: tracing, metrics, structured logs, SLO i alerty.
- [ ] NS-031: Pomiar narzutu p50/p95/p99 i weryfikacja celu <50 ms w jawnie określonych warunkach.
- [ ] NS-032: SDK Python/TypeScript i przykłady integracji on-premise.

## Etap 06 — walidacja produkcyjna
- [ ] NS-033: Testy multi-tenant, multi-node, awaryjne i recovery na docelowej infrastrukturze.
- [ ] NS-034: Testy obciążeniowe, soak, chaos i izolacja awarii.
- [ ] NS-035: Niezależny audyt bezpieczeństwa i obsługa ustaleń.
- [ ] NS-036: Operator sign-off z dowodami i decyzją go/no-go.

## Etap 07 — produkt i komercjalizacja
- [ ] NS-037: Panel B2B: polityki, eksperymenty, historia interwencji i rozliczenia.
- [ ] NS-038: Customer discovery i walidacja potrzeb 3–5 design partners.
- [ ] NS-039: Analiza jednostkowej ekonomiki GPU, storage i API.
- [ ] NS-040: Dokumentacja wdrożeń, API, bezpieczeństwa i ograniczeń.
- [ ] NS-041: Weryfikacja aktualnych warunków SPC, kwalifikowalności i terminu naboru.
- [ ] NS-042: Przygotowanie materiałów grantowych i dowodów technicznych bez niezweryfikowanych twierdzeń.

## Rejestr dowodów
Każdy zamknięty punkt musi wskazywać commit SHA, CI run, test/benchmark, środowisko, datę i osobę zatwierdzającą. Brak dowodu = pozycja otwarta.

## Reguła aktualizacji
Po każdym etapie: aktualizuj statusy, dowody, ryzyka, zależności i nowe pozycje; zachowuj historię. Zakaz samowolnego usuwania lub przepisywania zakresu.
