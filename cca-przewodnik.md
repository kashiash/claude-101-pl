---
title: CCA - przewodnik
---

# Claude Certified Architect — Kompletny Przewodnik po Egzaminie CCA Foundations

> Autor: Rick Hightower | Źródło: Towards AI | 24 marca 2026

---

## Wszystko, co musisz wiedzieć, żeby zdać egzamin CCA Foundations za pierwszym razem

12 marca 2026 roku Anthropic uruchomił egzamin Claude Certified Architect (CCA) Foundations. Branża AI w końcu ma profesjonalną certyfikację, która sprawdza, czy naprawdę potrafisz budować systemy produkcyjne z Claude. Nie czy piszesz sprytne prompty. Nie czy obejrzałeś tutorial. Czy potrafisz zaprojektować prawdziwe oprogramowanie działające na produkcji.

Jeśli przygotowujesz się do egzaminu CCA i chcesz zdać za pierwszym razem — ten przewodnik jest dla Ciebie. To artykuł 1 z serii ośmiu. Przeprowadzę Cię przez wszystko, czego potrzebujesz: format egzaminu, pięć domen kompetencji, sześć scenariuszy produkcyjnych, modele mentalne odróżniające zdających od niezdających, oraz tygodniowy plan nauki oparty na tym, gdzie kandydaci faktycznie tracą punkty.

Anthropic opisuje ten egzamin jako:

> "Egzamin na poziomie 301, zaprojektowany dla doświadczonych profesjonalistów z co najmniej 6 miesiącami bezpośredniego, praktycznego doświadczenia w budowaniu z Claude."

Pytania są oparte na scenariuszach, dystraktorzy są wiarygodni, a egzamin testuje zarówno to, czego NIE robić, jak i to, co robić.

---

## Dlaczego CCA ma znaczenie właśnie teraz

Anthropic zainwestował 100 milionów dolarów w sieć partnerów Claude. Ta liczba mówi dokładnie, ile warta jest ta certyfikacja.

![Plan certyfikacji CCA na 4 tygodnie](img-placeholder "Claude Certified Architect — 4 week plan")

Partnerzy ogłoszeni przy tej inwestycji:
- **Accenture** — przeszkolił 30 000 specjalistów, uruchomił dedykowaną grupę biznesową Anthropic
- **Cognizant** — dał dostęp do Claude 350 000 pracownikom
- **Deloitte** — wdrożył platformę dla 470 000 pracowników
- **Infosys** — uruchomił Centrum Doskonałości

![Accenture, Cognizant, Deloitte, Infosys inwestują intensywnie w Claude](img-placeholder "Accenture, Cognizant, Deloitte, Infosys investing heavily")

To nie są programy pilotażowe. To transformacje siły roboczej mierzone w setkach tysięcy ludzi.

Każda z tych organizacji potrzebuje ludzi, którzy potrafią projektować systemy oparte na Claude na poziomie profesjonalnym. Certyfikat daje menedżerom ds. rekrutacji ustandaryzowany sygnał na rynku, który obecnie nie ma żadnego ustandaryzowanego sygnału.

CCA to pierwsza certyfikacja, jaką kiedykolwiek oferował Anthropic. Dodatkowe certyfikacje dla sprzedawców, architektów i deweloperów są planowane na późniejszy okres 2026 roku.

---

## Format egzaminu

| Parametr | Wartość |
|---|---|
| Czas trwania | 120 minut |
| Liczba pytań | 60 |
| Wynik zaliczający | 720 / 1000 |
| Koszt | 99 USD |
| Scenariusze | 4 z 6 (losowo) |
| Narzędzia | Brak — tylko wiedza z głowy |

**Kluczowe uwagi:**

- Dwie minuty na pytanie to mało, gdy pytanie to cały akapit (150–200 słów). Musisz czytać szybko i błyskawicznie rozpoznawać wzorce.
- Nie możesz zatrzymać egzaminu po jego rozpoczęciu.
- Cztery z sześciu scenariuszy pojawiają się losowo — musisz przygotować się na wszystkie sześć.
- Żadnych narzędzi: bez Claude, bez dokumentacji, bez zewnętrznych zasobów.

**Strategia zarządzania czasem:** Zrób szybki pierwszy przegląd, oznacz pytania, przy których się wahasz. Odpowiedz na te, które znasz na pewno. Wróć do oznaczonych z pozostałym czasem.

![Format egzaminu: 120 minut, 60 pytań, wymagane 720 z 1000, koszt 99 USD](img-placeholder "120 minutes, 60 questions, must get 720 out of 1,000 and the test cost $99")

---

## 5 Domen Kompetencji

![Wykres rozkładu wag domen egzaminu CCA: Architektura agentyczna 27%, Claude Code 20%, Inżynieria promptów 20%, Projektowanie narzędzi 18%, Zarządzanie kontekstem 15%](img-placeholder "CCA exam domain weight distribution chart showing five segments: Agentic Architecture 27%, Claude Code 20%, Prompt Engineering 20%, Tool Design 18%, Context Management 15%")

| Domena | Waga |
|---|---|
| Architektura agentyczna i orkiestracja | 27% |
| Claude Code — konfiguracja i przepływy pracy | 20% |
| Inżynieria promptów i ustrukturyzowane wyjście | 20% |
| Projektowanie narzędzi i integracja MCP | 18% |
| Zarządzanie kontekstem i niezawodność | 15% |

---

### Domena 1: Architektura agentyczna i orkiestracja (27%)

To najważniejsza domena. Ponad jedna czwarta egzaminu testuje umiejętność projektowania systemów wieloagentowych.

**Co musisz wiedzieć:**

- **Wzorzec koordynator-subagent**: koordynator deleguje zadania do wyspecjalizowanych subagentów i syntetyzuje ich wyniki
- **Hub-and-spoke**: równoległe, niezależne zadania bez zależności między nimi
- **Krytyczna zasada**: subagenty NIE dziedziczą kontekstu automatycznie. Gdy koordynator tworzy subagenta, ten zaczyna z pustym kontekstem. Musisz jawnie przekazać wszystko, czego potrzebuje.
- **Zarządzanie stanem sesji**: jak utrzymywać kontekst rozmowy przez wiele tur w pętli agentycznej
- **Dekompozycja zadań**: podział złożonych żądań na dyskretne podzadania
- **Logika eskalacji**: kiedy i jak agent powinien przekazać sprawę człowiekowi lub bardziej zaawansowanemu systemowi

> **Pułapka egzaminacyjna:** Najczęstszy błąd w Domenie 1 to wzorzec "super-agenta": jeden agent z 15+ narzędziami zamiast 3–4 wyspecjalizowanych agentów z 4–5 narzędziami każdy. Gdy widzisz odpowiedź konsolidującą wszystko w jednym potężnym agencie — ta odpowiedź jest prawie zawsze błędna.

---

### Domena 2: Claude Code — konfiguracja i przepływy pracy (20%)

**Co musisz wiedzieć:**

- **Hierarchia CLAUDE.md**:
  - Poziom projektu: `.claude/CLAUDE.md` — współdzielony przez kontrolę wersji, standardy dla całego zespołu
  - Poziom użytkownika: `~/.claude/CLAUDE.md` — osobiste preferencje, nie współdzielone
- **Niestandardowe polecenia slash i umiejętności**: jak tworzyć wielokrotnie używalne przepływy pracy jako umiejętności oparte na markdown
- **Tryb plan vs. bezpośrednie wykonanie**: tryb plan dla złożonych, wieloetapowych zadań; bezpośrednie wykonanie dla dobrze zdefiniowanych, niskiego ryzyka zadań
- **Integracja CI/CD**: flaga `-p` (lub `--print`) dla nieinteraktywnych potoków
- **Flaga `--bare`**: dla skryptowych wywołań CI/CD, pomija auto-discovery i zapewnia powtarzalne zachowanie
- **`--output-format json`**: dla ustrukturyzowanego wyjścia JSON z Claude Code

> **Pułapka egzaminacyjna:** Pytania o CI/CD prawie zawsze mają pułapkę polegającą na uruchomieniu Claude Code interaktywnie lub bez flagi `-p`. Gdy widzisz kontekst CI/CD, sprawdź mentalnie, czy flaga `-p` jest obecna. Jeśli jej brakuje — rozwiązanie jest błędne.

---

### Domena 3: Inżynieria promptów i ustrukturyzowane wyjście (20%)

Kluczowe słowo to "niezawodne". Claude produkujący JSON przez większość czasu nie wystarczy na produkcji.

**Co musisz wiedzieć:**

- **Wymuszanie schematu JSON przez `tool_choice`**: używanie `tool_choice` ze schematami wejściowymi do wymuszenia formatu wyjściowego programistycznie
- **API ustrukturyzowanych wyjść**: `client.messages.parse()` z modelami Pydantic (funkcja beta, wymaga nagłówka `anthropic-beta: structured-outputs-2025-11-13`)
- **Prompty few-shot**: dostarczanie przykładowych wejść i wyjść do prowadzenia formatu odpowiedzi Claude
- **Pętle walidacja-ponowna próba**: sprawdź wyjście względem schematu; jeśli nie przejdzie, wyślij błąd z powrotem do Claude z instrukcją naprawy
- **Główny anty-wzorzec**: poleganie wyłącznie na promptach dla zgodności JSON

> **Pułapka egzaminacyjna:** Każda odpowiedź mówiąca "dodaj instrukcje do systemowego promptu" jako rozwiązanie problemu zgodności JSON jest prawie na pewno błędna. Egzamin konsekwentnie nagradza `tool_choice`, API ustrukturyzowanych wyjść i pętle walidacja-ponowna próba.

---

### Domena 4: Projektowanie narzędzi i integracja MCP (18%)

Model Context Protocol (MCP) to otwarty standard Anthropic do łączenia systemów AI z zewnętrznymi narzędziami i danymi. Uruchomiony w listopadzie 2024, przyjęty przez OpenAI i Google DeepMind.

**Co musisz wiedzieć:**

- **Prymitywy MCP i kiedy używać każdego:**
  - **Tools (Narzędzia)**: wykonywalne funkcje, które model może wywołać. Używaj do akcji: zapytanie do bazy danych, wywołanie API, zapis pliku
  - **Resources (Zasoby)**: dane do wstrzyknięcia do promptów lub potoków RAG. Używaj dla kontekstu tylko do odczytu: dokumentacja, schematy, bazy wiedzy
  - **Prompts (Prompty)**: predefiniowane szablony lub przepływy pracy. Używaj dla wielokrotnie używanych wzorców instrukcji
- **Pliki konfiguracyjne**: `.mcp.json` — poziom projektu, współdzielony; `~/.claude.json` — poziom użytkownika, osobisty
- **Opisy narzędzi jako routing**: opis narzędzia to główny mechanizm, którego Claude używa do decydowania, które narzędzie wywołać
- **Zasada 4–5 narzędzi**: oficjalne wytyczne Anthropic to 4–5 skupionych narzędzi na agenta

> **Pułapka egzaminacyjna:** Granica narzędzie-zasób to najtrudniejsza ocena w tej domenie. Pytaj siebie: czy Claude musi to wywołać, żeby podjąć akcję, czy potrzebuje tylko danych jako kontekstu? Akcje to narzędzia. Kontekst to zasoby.

---

### Domena 5: Zarządzanie kontekstem i niezawodność (15%)

Najmniejsza domena wagowo, ale przekrojowa dla każdego scenariusza.

**Co musisz wiedzieć:**

- **Efekt "zagubiony w środku"**: Claude i wszystkie modele oparte na transformerach zwracają większą uwagę na informacje na początku i końcu okna kontekstu. Umieszczaj krytyczne informacje na początku lub końcu.
- **Degradacja kontekstu w długich sesjach**: jak łagodzić: ustrukturyzowane podsumowania, okresowe powtarzanie kluczowych faktów
- **Projektowanie eskalacji**: deterministyczne reguły wyzwalają eskalację, nie samoocena modelu

**Ekonomia tokenów:**

| Metoda | Oszczędność kosztów | Opóźnienie | Przypadek użycia |
|---|---|---|---|
| Prompt Caching | do 90% | Czas rzeczywisty | Powtarzające się systemowe prompty, dokumenty polityk, przykłady few-shot |
| Message Batches API | 50% | Do 24 godzin | Nocne audyty, przetwarzanie masowe, zadania offline |
| Real-Time API | Standardowe ceny | Czas rzeczywisty | Przepływy pracy skierowane do użytkownika, zadania blokujące |

> **Pułapka egzaminacyjna:** Gdy widzisz pytanie o optymalizację kosztów w systemie, gdzie użytkownicy aktywnie czekają na odpowiedzi — odpowiedź to nigdy Batch API. Odpowiedź to Prompt Caching dla powtarzającego się kontekstu.

---

## 6 Scenariuszy Produkcyjnych

Każdy egzamin losuje 4 z 6 scenariuszy. Musisz przygotować się na wszystkie sześć.

![Macierz pokrycia scenariuszy CCA — mapowanie sześciu scenariuszy egzaminacyjnych na pięć domen kompetencji z intensywnością cieniowania](img-placeholder "CCA scenario-domain coverage matrix mapping six exam scenarios to five competency domains with intensity shading")

![Tabela scenariuszy egzaminacyjnych](img-placeholder "Scenarios covered")

### Scenariusz 1: Agent rozwiązywania problemów obsługi klienta
Budujesz agenta wsparcia obsługującego żądania o wysokiej niejednoznaczności: zwroty, spory rozliczeniowe, problemy z kontem. Testuje logikę eskalacji i ograniczenia zgodności.

**Pułapka:** Używanie samooceny pewności Claude do decydowania o eskalacji. Używaj zamiast tego deterministycznych reguł biznesowych: kategoria zgłoszenia, kwota w dolarach, poziom konta.

### Scenariusz 2: Generowanie kodu z Claude Code
Konfigurujesz Claude Code do nawigacji po dużej bazie kodu i zadań generowania kodu.

**Pułapka:** Wiara, że większe okno kontekstu rozwiązuje problemy z dystrybucją uwagi. Nie rozwiązuje. Efekt "zagubiony w środku" stosuje się niezależnie od całkowitego rozmiaru kontekstu.

### Scenariusz 3: Wieloagentowy system badawczy
Projektujesz system wieloagentowy, gdzie koordynator wysyła zadania badawcze do wyspecjalizowanych subagentów z iteracyjnymi pętlami udoskonalania.

**Pułapka:** Anty-wzorzec "super-agenta": jeden agent ze wszystkimi 18 narzędziami zamiast dystrybucji 4–5 narzędzi na wyspecjalizowanego subagenta. Subagenty nie dziedziczą kontekstu koordynatora automatycznie.

### Scenariusz 4: Narzędzia produktywności deweloperów
Integrujesz Claude Code z przepływami pracy deweloperów używając niestandardowych poleceń slash i konfiguracji CLAUDE.md.

Testuje wiedzę o trybie plan vs. bezpośrednie wykonanie oraz hierarchii CLAUDE.md.

### Scenariusz 5: Claude Code dla CI/CD
Integrujesz Claude z potokami CI/CD dla automatycznych przeglądów kodu, generowania testów i informacji zwrotnych o pull requestach.

**Pułapka:** Każde rozwiązanie zakładające, że tryb interaktywny działa w potoku CI/CD. Krytyczny wzorzec: flaga `-p` dla trybu nieinteraktywnego z `--bare` dla powtarzalności.

### Scenariusz 6: Ekstrakcja ustrukturyzowanych danych
Wyodrębniasz ustrukturyzowane dane z nieustrukturyzowanych dokumentów używając schematów JSON.

**Pułapka:** Wymuszanie wyłącznie przez prompt. Prawidłowe podejście używa `tool_choice` ze schematami wejściowymi lub API ustrukturyzowanych wyjść z programistyczną walidacją i pętlami ponownych prób.

---

## Krytyczne Modele Mentalne

![Drzewo decyzyjne anty-wzorzec vs. prawidłowy wzorzec — ścieżki z czerwonym X vs. zielonym checkmarkiem dla pięciu kluczowych decyzji architektonicznych](img-placeholder "Anti-pattern vs correct pattern decision tree showing red X paths versus green checkmark paths for five key architectural decisions")

### Model 1: Wymuszanie programistyczne bije wskazówki promptowe
Zawsze. Dla reguł biznesowych, zgodności JSON, decyzji routingowych: nie proś Claude o przestrzeganie reguł w prompcie. Wymuszaj je w kodzie.

> Prompty to wskazówki. Kod to prawo.

### Model 2: Subagenty nie dziedziczą kontekstu
Gdy koordynator tworzy subagenta, ten zaczyna z czystą kartą. Musisz jawnie przekazać kontekst, którego potrzebuje. To jeden z najczęściej testowanych konceptów na całym egzaminie.

### Model 3: Opisy narzędzi sterują routingiem
Claude nie wybiera narzędzi na podstawie nazw agentów ani nazw narzędzi. Czyta opisy narzędzi. Źle napisany opis oznacza wywołanie złego narzędzia. Pisz opisy jak dokumentację dla dewelopera, który nigdy nie widział Twojej bazy kodu.

### Model 4: Efekt "zagubiony w środku" jest realny
Umieszczaj krytyczne informacje na początku lub końcu kontekstu. Treść w środku długiego okna kontekstu otrzymuje mniej uwagi. Dotyczy to każdego scenariusza z długim kontekstem.

### Model 5: Dopasuj API do wymagań opóźnienia
- Batch API → zadania w tle
- Real-Time API → przepływy pracy skierowane do użytkownika
- Prompt Caching → optymalizacja kosztów dla powtarzającego się kontekstu z wymaganiami czasu rzeczywistego

---

## Katalog Anty-wzorców

### Domena 1: Architektura agentyczna

| Anty-wzorzec | Problem | Prawidłowy wzorzec |
|---|---|---|
| Super-agent z 15+ narzędziami | Degradacja dokładności wyboru, ryzyko rozrostu zakresu | 4–5 skupionych narzędzi na agenta, delegowanie do subagentów |
| Samoocena pewności do routingu | Pewność LLM nie jest skalibrowana dla produkcji | Deterministyczne reguły biznesowe (kwota, poziom konta, typ problemu) |
| Zakładanie dziedziczenia kontekstu przez subagenty | Subagenty zaczynają z pustym kontekstem | Jawne przekazywanie całego potrzebnego kontekstu |

### Domena 2: Claude Code

| Anty-wzorzec | Problem | Prawidłowy wzorzec |
|---|---|---|
| Uruchamianie bez `-p` w CI/CD | Tryb interaktywny zawiesza się w środowisku headless | Używaj `-p` dla trybu nieinteraktywnego, `--bare` dla powtarzalności |
| Preferencje użytkownika w projekcie CLAUDE.md | Osobiste preferencje trafiają do wszystkich członków zespołu | Preferencje użytkownika w `~/.claude/CLAUDE.md` |
| Bezpośrednie wykonanie dla złożonych zmian wieloplikowych | Ryzyko niezamierzonych zmian bez planu | Używaj trybu plan dla złożonych, wieloetapowych operacji |

### Domena 3: Inżynieria promptów

| Anty-wzorzec | Problem | Prawidłowy wzorzec |
|---|---|---|
| Wymuszanie JSON wyłącznie przez prompt | Podejście "best-effort", zawodzi na przypadkach brzegowych | `tool_choice` ze schematami wejściowymi lub API ustrukturyzowanych wyjść |
| Brak pętli walidacja-ponowna próba | Brak możliwości odzyskania po błędzie walidacji | Waliduj wyjście programistycznie, przy błędzie wyślij kontekst błędu z powrotem do Claude |

### Domena 4: Projektowanie narzędzi

| Anty-wzorzec | Problem | Prawidłowy wzorzec |
|---|---|---|
| Eksponowanie danych tylko do odczytu jako narzędzie | Nadużycie abstrakcji narzędzia, marnowanie wywołań | Używaj MCP Resources dla danych tylko do odczytu, Tools dla akcji |
| Niejasne opisy narzędzi | Claude nie może niezawodnie wybrać właściwego narzędzia | Precyzyjne, specyficzne opisy z dokładnymi granicami i przypadkami użycia |

### Domena 5: Zarządzanie kontekstem

| Anty-wzorzec | Problem | Prawidłowy wzorzec |
|---|---|---|
| Batch API dla obsługi klienta na żywo | Batch API może trwać do 24 godzin | Real-Time API dla wszystkich przepływów pracy skierowanych do użytkownika |
| Surowy transkrypt rozmowy jako przekazanie eskalacji | Efekt "zagubiony w środku", trudny do przetworzenia przez człowieka | Ustrukturyzowane podsumowanie JSON z kluczowymi polami na górze |
| Krytyczne informacje zakopane w środku kontekstu | Mniej uwagi ze względu na efekt "zagubiony w środku" | Umieszczaj krytyczne informacje na początku lub końcu kontekstu |

---

## 4-Tygodniowy Plan Nauki

*Plan zakłada, że już budujesz z Claude. Jeśli zaczynasz od zera, dodaj 2–4 tygodnie.*

### Tydzień 1: Podstawy i modele mentalne
**Kursy:** Claude 101 i AI Fluency: Framework and Foundations

Cel: zinternalizuj słownictwo i modele mentalne przed przejściem do zaawansowanego materiału.

Do końca tygodnia 1 powinieneś umieć zdefiniować bez zaglądania: pętla agentyczna, wzorzec koordynator-subagent, forkowanie kontekstu, powód zatrzymania (stop reason), `tool_choice`, pętla walidacja-ponowna próba, efekt "zagubiony w środku".

### Tydzień 2: Podstawowe umiejętności (Tydzień największych inwestycji)
**Kurs:** Building with the Claude API (8–10 godzin; to najważniejszy pojedynczy kurs)

Cel: praktyczne doświadczenie z wzorcami, które egzamin testuje najciężej.

Przejdź przez każde ćwiczenie. Zbuduj pętlę walidacja-ponowna próba od zera. Ćwicz ustrukturyzowane wyjście z `tool_choice` i schematami JSON. Zrozum powód zatrzymania `tool_use` i jak programistycznie sprawdzać wyniki narzędzi.

Do końca tygodnia 2 powinieneś mieć działający kod dla: pętli walidacja-ponowna próba, wywołania ustrukturyzowanego wyjścia wymuszonego przez `tool_choice`, prostego agenta z 3–4 narzędziami.

### Tydzień 3: Zaawansowane tematy (Tydzień miny lądowej Domeny 4)
**Kursy:** MCP Mastery, Claude Code in Action, Introduction to Agent Skills

Cel: zamknij luki w projektowaniu narzędzi MCP i konfiguracji Claude Code.

Zbuduj serwer MCP w Pythonie. Eksponuj 3 narzędzia i 1 zasób. Połącz z Claude Code. Zwróć szczególną uwagę na granicę między narzędziami a zasobami.

Do końca tygodnia 3 powinieneś mieć: działający serwer MCP z narzędziami i zasobem, prawdziwy projekt z poprawnie skonfigurowanym CLAUDE.md, udane uruchomienie Claude Code w trybie headless.

### Tydzień 4: Ćwiczenia, anty-wzorce i symulacja egzaminu
**Aktywności:** Weź oficjalny egzamin próbny. Przejrzyj każdą błędną odpowiedź. Celuj w 900+ przed zaplanowaniem prawdziwego egzaminu.

Cel: przekształć wiedzę w szybkość wykonania w dniu egzaminu.

Weź egzamin próbny w prawdziwych warunkach: bez notatek, bez dokumentacji, bez kart przeglądarki. Zmierz czas. Skategoryzuj błędne odpowiedzi według domeny.

Zbuduj projekt końcowy: agent koordynator z dwoma subagentami, każdy z 4–5 narzędziami, jawnie przekazujący kontekst między nimi.

---

## Alokacja czasu nauki

| Domena | Waga | Godziny | Priorytet |
|---|---|---|---|
| Architektura agentyczna i orkiestracja | 27% | 8–10 h | Najwyższy; zbuduj projekt koordynator-subagent |
| Claude Code — konfiguracja i przepływy pracy | 20% | 6–7 h | CI/CD i hierarchia CLAUDE.md są intensywnie testowane |
| Inżynieria promptów i ustrukturyzowane wyjście | 20% | 6–7 h | Zbuduj pętlę walidacja-ponowna próba; nie pomijaj |
| Projektowanie narzędzi i integracja MCP | 18% | 6–8 h | Dodaj dodatkowy czas; granica narzędzie-zasób jest trudniejsza niż waga sugeruje |
| Zarządzanie kontekstem i niezawodność | 15% | 4–5 h | Tabela ekonomii tokenów musi być zapamiętana |
| **Łącznie** | **100%** | **30–37 h** | |

---

## Opinie wczesnych kandydatów

- Trudność jest realna. Konsensus społeczności: "to nie jest certyfikacja, którą zdasz po obejrzeniu tutoriala"
- Rozpoznawanie anty-wzorców ma znaczenie tak samo jak znajomość prawidłowych odpowiedzi
- Granice narzędzi MCP potykają ludzi bardziej niż jakikolwiek inny temat
- Zarządzanie czasem jest krytyczne, szczególnie w łańcuchach scenariuszy
- Jeden kandydat opublikował wynik 985/1000 na Reddit — perfekcyjne wyniki są możliwe
- Wynik zaliczający to 720, co daje znaczący margines błędu

---

## Słownik kluczowych pojęć

| Termin | Definicja |
|---|---|
| Pętla agentyczna (Agentic Loop) | Cykl: odbierz wejście, rozumuj, wywołaj narzędzia, oceń wyniki, zdecyduj o następnym kroku |
| Forkowanie kontekstu (Context Forking) | Podział kontekstu na oddzielne gałęzie dla różnych subagentów |
| Wzorzec koordynator-subagent | Agent koordynator deleguje do wyspecjalizowanych subagentów i syntetyzuje wyniki |
| Programistyczny hook | Wymuszanie na poziomie kodu (np. PostToolUse) walidujące lub transformujące wyjścia narzędzi |
| Powód zatrzymania (Stop Reason) | Sygnał API dlaczego generowanie się zatrzymało (np. `tool_use`, `end_turn`, `max_tokens`) |
| `tool_choice` | Parametr API kontrolujący wybór narzędzia: `auto` (model decyduje), `any` (musi użyć narzędzia), lub konkretne narzędzie |
| Pętla walidacja-ponowna próba | Sprawdź wyjście względem schematu; przy błędzie wyślij błąd z powrotem do Claude do korekty |
| MCP Resources | Katalogi danych/schematy eksponowane do wstrzyknięcia (kontekst tylko do odczytu) |
| MCP Tools | Wykonywalne funkcje, które model może wywołać do podjęcia akcji |
| MCP Prompts | Predefiniowane szablony instrukcji lub przepływy pracy |

---

## Zasoby do nauki

### Oficjalne zasoby Anthropic
- Anthropic Academy: [anthropic.skilljar.com](https://anthropic.skilljar.com) (13 kursów, BEZPŁATNE dla wszystkich)
- Przewodnik po egzaminie CCA: Oficjalny przewodnik na SlideShare
- Egzamin próbny: Dostępny przez Anthropic Academy (cel: 900+ przed prawdziwym egzaminem)

### Oficjalna dokumentacja
- Dokumentacja Claude Agent SDK
- Dokumentacja Claude Code
- Dokumentacja MCP
- Zaawansowane użycie narzędzi (Anthropic Engineering)
- Dokumentacja przetwarzania wsadowego
- Dokumentacja ustrukturyzowanych wyjść

---

*Artykuł 1 z 8 w serii CCA Exam Prep. Autor: Rick Hightower — dyrektor technologiczny i inżynier danych, który kierował rozwojem ML/AI w firmie z listy Fortune 100.*
