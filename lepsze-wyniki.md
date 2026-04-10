# Uzyskiwanie lepszych wyników

Szacowany czas: 15 minut

## Cele lekcji

Po zakończeniu tej lekcji będziesz potrafić:

- Rozpoznawać typowe wyzwania przy pierwszych kontaktach z AI i stosować techniki rozwiązywania problemów
- Zdefiniować pojęcie AI Fluency i wiedzieć, gdzie szukać informacji o płynnej pracy z AI
- Wyjaśnić, jak skonfigurować ewaluacje, aby lepiej zrozumieć, jak Claude radzi sobie z Twoimi konkretnymi zadaniami

---

## Typowe wyzwania i jak je rozwiązać

Gdy zaczynasz pracować z Claude, prawdopodobnie natkniesz się na momenty, gdy odpowiedź nie jest dokładnie taka, jakiej oczekiwałeś. To normalne — i jest to okazja do udoskonalenia swojego podejścia. Oto najczęstsze wyzwania i sposoby ich rozwiązania.

| Wyzwanie | Co się dzieje | Spróbuj tego |
|---|---|---|
| Odpowiedź Claude jest zbyt ogólna | Prompt nie zawierał wystarczającego kontekstu o Twojej sytuacji | Dodaj szczegóły dotyczące odbiorcy, roli lub ograniczeń. Zamiast „Napisz e-mail o opóźnieniu projektu", spróbuj: „Napisz e-mail do naszego klienta korporacyjnego wyjaśniający, że integracja oprogramowania opóźni się o dwa tygodnie. Był dotychczas cierpliwy, ale to już drugie opóźnienie. Zachowaj profesjonalny, ale przepraszający ton." |
| Odpowiedź jest za długa (lub za krótka) | Claude zgaduje odpowiednią długość | Bądź precyzyjny: „Daj mi podsumowanie w dwóch akapitach" lub „Ogranicz do 100 słów" albo „Potrzebuję wyczerpującej analizy — długość nie jest problemem." |
| Claude nie zastosował mojego formatu | Claude rozumiał *co* chcesz, ale nie *jak* to przedstawić | Pokaż, nie tylko opisuj. Podaj przykład formatu lub opisz strukturę wprost: „Użyj punktorów z pogrubionymi nagłówkami dla każdej sekcji." |
| Otrzymałem pewnie brzmiące informacje, które okazały się błędne | Claude czasem generuje wiarygodnie wyglądające, ale niepoprawne informacje, szczególnie przy konkretnych faktach lub niszowych tematach | Przy ważnych zadaniach weryfikuj kluczowe fakty niezależnie. Poproś Claude o podanie źródeł lub wskazanie poziomu pewności. Włącz wyszukiwanie w sieci, aby odpowiedzi były oparte na aktualnych informacjach. |
| Ton nie jest odpowiedni | Claude domyślnie przyjmuje pomocny i profesjonalny ton, który może nie pasować do Twoich potrzeb | Opisz ton prostym językiem: „Zrób to bardziej konwersacyjnym" lub „To powinno brzmieć autorytatywnie i formalnie." Podaj przykład tekstu w stylu, którego oczekujesz. |

---

## Nastawienie na iterację

Jedną z najważniejszych zmian w pracy z Claude jest uświadomienie sobie, że pierwszy prompt rzadko daje idealny wynik — i to jest w porządku. Traktuj swój pierwszy prompt jako początek rozmowy, a nie jednorazowe zapytanie.

Skuteczni użytkownicy Claude:

- **Traktują pierwsze wersje jako punkt wyjścia.** Przeglądają wynik, identyfikują co działa, a co nie, i doprecyzowują.
- **Dają konkretną informację zwrotną.** „Skróć to" jest okej, ale „Usuń pierwsze dwa akapity i spraw, żeby zakończenie było bardziej zorientowane na działanie" jest lepsze.
- **Wiedzą, kiedy zacząć od nowa.** Jeśli rozmowa zeszła na manowce, czasem szybciej jest otworzyć nowy czat z wyraźniejszym promptem, niż próbować naprowadzić Claude z powrotem.

---

## Czym jest AI Fluency?

AI Fluency to zdolność do efektywnej współpracy z narzędziami AI — nie tylko znajomość tego, które przyciski klikać, ale rozwijanie osądu pozwalającego dobrze używać AI w różnych sytuacjach.

**Framework 4D dla AI Fluency**, opracowany we współpracy badawczej między profesorem Rickiem Dakanem (Ringling College of Art and Design) a profesorem Josephem Fellerem (University College Cork), wyróżnia cztery kluczowe kompetencje, które łącznie pomagają w pełni wykorzystać interakcje z AI:

- **Delegation (Delegowanie):** Decydowanie, jaką pracę powinni wykonywać ludzie, jaką AI, i jak rozdzielać zadania między nimi. Obejmuje rozumienie celów, możliwości AI i strategiczne wybory dotyczące współpracy.
- **Description (Opisywanie):** Skuteczne komunikowanie się z systemami AI. Obejmuje jasne definiowanie wyników, kierowanie procesami AI i określanie pożądanych zachowań.
- **Discernment (Ocenianie):** Przemyślana i krytyczna ocena wyników, procesów i zachowań AI. Obejmuje ocenę jakości, dokładności, stosowności i identyfikację obszarów do poprawy.
- **Diligence (Staranność):** Odpowiedzialne i etyczne korzystanie z AI. Obejmuje przemyślane wybory dotyczące systemów AI, zachowanie przejrzystości i odpowiedzialność za pracę wspomaganą przez AI.

Przez cały ten kurs już ćwiczyłeś te umiejętności. Framework promptów z Lekcji 2 (ustawianie sceny, definiowanie zadania, określanie zasad) wywodzi się z Opisywania. Techniki rozwiązywania problemów powyżej czerpią z Oceniania i Staranności.

Aby dowiedzieć się więcej, sprawdź nasz bezpłatny kurs AI Fluency, który zgłębia wszystkie cztery kompetencje z praktycznymi ćwiczeniami i zastosowaniami w rzeczywistych sytuacjach.

---

## Ewaluacja Claude dla Twoich zadań

Gdy zaczynasz integrować Claude z coraz większą częścią swojej pracy, możesz się zastanawiać: skąd wiem, czy Claude jest naprawdę dobry w tym konkretnym zadaniu?

Tu kluczowe staje się **Ocenianie**. **Ewaluacje** (ang. *evals*) to sposób na rozwinięcie intuicji do oceny wyników Claude przy zadaniach, które są dla Ciebie ważne. To systematyczne metody testowania, jak dobrze Claude radzi sobie z konkretnymi typami zadań.

### Dlaczego ewaluacje mają znaczenie

Twoja praca jest wyjątkowa. Claude może świetnie radzić sobie z tworzeniem tekstów marketingowych, ale potrzebować więcej wskazówek przy dokumentacji technicznej w Twojej dziedzinie. Przeprowadzanie prostych ewaluacji pomaga:

- Zrozumieć, gdzie Claude wnosi największą wartość w Twoim procesie pracy
- Zidentyfikować zadania, przy których trzeba dostarczyć więcej kontekstu lub przykładów
- Budować zaufanie do wyników Claude przy powtarzających się zadaniach

### Proste podejście do ewaluacji

Nie potrzebujesz złożonej infrastruktury, żeby oceniać Claude. Oto praktyczne podejście:

1. **Zbierz przykłady.** Zgromadź 5–10 przykładów zadania, które wykonujesz regularnie — e-maile, które napisałeś, raporty, które stworzyłeś, analizy, które przeprowadziłeś.
2. **Stwórz prompty testowe.** Napisz prompty, które generowałyby podobne wyniki. Uwzględnij kontekst, który naturalnie miałbyś przy wykonywaniu tego zadania.
3. **Porównaj wyniki.** Uruchom prompty i porównaj odpowiedzi Claude z Twoimi przykładami. Zadaj sobie pytania:
   - Czy Claude uchwycił kluczowe informacje?
   - Czy ton i styl są odpowiednie?
   - Czego brakuje lub co można poprawić?
4. **Udoskonal swoje podejście.** Na podstawie tego, czego się nauczyłeś, dostosuj prompty, dodaj przykłady pokazujące Claude, jak wygląda dobry wynik, lub zidentyfikuj miejsca, gdzie niezbędna jest ludzka weryfikacja.

### Przykład: Używanie Claude do analizy danych

[![Obejrzyj wideo](https://img.youtube.com/vi/Zzn-g8lvLMA/0.jpg)](https://youtu.be/Zzn-g8lvLMA?si=VCbziRriemM6MY1p)

Aby ocenić, jak Claude może pracować z Twoimi danymi:

1. Znajdź zbiór danych, który ręcznie analizowałeś
2. Stwórz prompty zlecające Claude przeprowadzenie analizy
3. Porównaj wyniki Claude z Twoimi oryginałami
4. Zanotuj wzorce i doprecyzuj prompt — może Claude uzyskuje właściwe liczby, ale nie dostrzega ogólnych wzorców

Ten rodzaj lekkiej ewaluacji pomaga rozwinąć intuicję dotyczącą pracy z Claude przy zadaniach, które są dla Ciebie ważne — i wskazuje, gdzie skupić energię na przeglądaniu i udoskonalaniu.

---

## Refleksja po lekcji

Przed przejściem dalej zastanów się:

- Które z typowych wyzwań już napotkałeś? Jakich technik możesz spróbować następnym razem?
- Gdzie w Twojej pracy prosta ewaluacja pomogłaby ocenić, czy Claude nadaje się do powtarzającego się zadania?
- Jak Framework 4D może pomóc Ci myśleć o współpracy z Claude?
