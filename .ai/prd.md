# Dokument wymagań produktu (PRD) - 10xCards

## 1. Przegląd produktu

10xCards to webowa aplikacja edukacyjna, umożliwiająca użytkownikom szybkie generowanie, edytowanie i zarządzanie fiszkami edukacyjnymi. Dzięki integracji z modelami AI, aplikacja umożliwia tworzenie fiszek z wklejonego tekstu, wspierając metodę nauki poprzez powtórki interwałowe (spaced repetition). MVP koncentruje się na uproszczonej wersji produktu, która pozwala użytkownikom na korzystanie z kluczowych funkcjonalności bez rozbudowanych funkcji społecznościowych czy mobilnych.

## 2. Problem użytkownika

Ręczne tworzenie fiszek jest czasochłonne i zniechęcające, mimo że metoda spaced repetition jest jedną z najefektywniejszych technik zapamiętywania. Użytkownicy potrzebują szybkiego, prostego i skutecznego sposobu na generowanie i zarządzanie fiszkami na podstawie własnych materiałów edukacyjnych (np. notatek, podręczników).

## 3. Wymagania funkcjonalne

- Generowanie fiszek przez AI na podstawie tekstu wprowadzonego przez użytkownika
- Obsługa trzech typów fiszek: pytanie–odpowiedź, uzupełnianie luk, prawda/fałsz
- Możliwość ręcznego tworzenia fiszek
- Edycja, przegląd i usuwanie fiszek
- Dodawanie obrazów do fiszek
- Organizacja fiszek w kolekcje
- Przechowywanie danych przypisanych do konta użytkownika
- Logowanie i rejestracja przez Auth0
- Integracja z gotowym algorytmem powtórek
- Widok tabelaryczny zarządzania fiszkami
- Test e2e scenariusza od logowania do utworzenia fiszki
- CI/CD z Github Actions
- Hosting na DigitalOcean
- Twarde nadpisywanie fiszek (brak wersjonowania)

## 4. Granice produktu

MVP **nie** obejmuje:
- Zaawansowanego algorytmu powtórek (np. SuperMemo, Anki)
- Współdzielenia fiszek między użytkownikami
- Aplikacji mobilnych
- Importu z innych formatów plików (np. PDF, DOCX)
- Integracji z zewnętrznymi platformami edukacyjnymi
- Zaawansowanego systemu uprawnień lub ról
- Wersjonowania fiszek

## 5. Historyjki użytkowników

### US-001
- Tytuł: Rejestracja i logowanie
- Opis: Jako nowy użytkownik chcę zarejestrować się i zalogować za pomocą Auth0, aby móc tworzyć i zarządzać własnymi fiszkami.
- Kryteria akceptacji:
  - Użytkownik może utworzyć konto przez Auth0.
  - Użytkownik może zalogować się do aplikacji.
  - Po zalogowaniu widoczne są jego własne kolekcje fiszek.

### US-002
- Tytuł: Generowanie fiszek przez AI
- Opis: Jako użytkownik chcę wkleić fragment tekstu i wygenerować fiszki, aby szybko przekształcić materiał źródłowy w narzędzie do nauki.
- Kryteria akceptacji:
  - Użytkownik może wkleić tekst do pola wejściowego.
  - AI generuje zestaw fiszek w jednym z trzech formatów.
  - Użytkownik może zaakceptować, odrzucić lub edytować wygenerowane fiszki.

### US-003
- Tytuł: Ręczne tworzenie fiszek
- Opis: Jako użytkownik chcę tworzyć fiszki ręcznie, aby mieć pełną kontrolę nad treścią.
- Kryteria akceptacji:
  - Użytkownik może wybrać typ fiszki.
  - Użytkownik może wpisać pytanie, odpowiedź, opcjonalny obraz i przypisać fiszkę do kolekcji.
  - Użytkownik może zapisać fiszkę.

### US-004
- Tytuł: Zarządzanie fiszkami
- Opis: Jako użytkownik chcę przeglądać, edytować i usuwać moje fiszki w tabeli, aby łatwo nimi zarządzać.
- Kryteria akceptacji:
  - Użytkownik widzi listę fiszek w formie tabeli.
  - Użytkownik może kliknąć w fiszkę, aby ją edytować.
  - Użytkownik może usunąć dowolną fiszkę.

### US-005
- Tytuł: Organizacja fiszek w kolekcje
- Opis: Jako użytkownik chcę przypisywać fiszki do kolekcji, aby uporządkować materiał tematycznie.
- Kryteria akceptacji:
  - Użytkownik może tworzyć i nazwać nową kolekcję.
  - Użytkownik może przypisać fiszkę do kolekcji.
  - Użytkownik może przeglądać fiszki w ramach kolekcji.

### US-006
- Tytuł: Dodawanie obrazu do fiszki
- Opis: Jako użytkownik chcę dodać obraz do fiszki, aby lepiej zapamiętywać skojarzenia wizualne.
- Kryteria akceptacji:
  - Użytkownik może załadować obraz z pliku.
  - Obraz jest widoczny przy fiszce po zapisaniu.

### US-007
- Tytuł: Przetestowanie kluczowego przepływu (e2e)
- Opis: Jako zespół chcemy mieć test e2e sprawdzający scenariusz logowania i tworzenia fiszki, aby zapewnić podstawową niezawodność aplikacji.
- Kryteria akceptacji:
  - Test loguje użytkownika przez Auth0.
  - Test tworzy nową fiszkę z tekstu wygenerowanego przez AI.
  - Test kończy się sukcesem i waliduje obecność fiszki.

## 6. Metryki sukcesu

- Co najmniej 75% fiszek generowanych przez AI jest akceptowanych przez użytkownika.
- Co najmniej 75% tworzonych fiszek pochodzi z funkcji AI.
- Zakończenie implementacji MVP w ciągu 2 tygodni.
- Użytkownik może przejść pełen flow od logowania do utworzenia i zapisania fiszki bez błędów.
- Testy e2e przechodzą pomyślnie w CI/CD (Github Actions).

