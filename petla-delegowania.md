# Pętla delegowania i staranności — analiza danych

[![Obejrzyj wideo](https://img.youtube.com/vi/Zzn-g8lvLMA/0.jpg)](https://youtu.be/Zzn-g8lvLMA?si=VCbziRriemM6MY1p)

---

W poprzedniej lekcji zajmowaliśmy się prywatnością i bezpieczeństwem danych — co bezwzględnie trzeba chronić i jak to robić. Teraz porozmawiajmy o pytaniu, które prawdopodobnie powstrzymywało Cię przed używaniem AI do analizy danych: **Jak mogę ufać wynikom?**

Dzisiejsza lekcja dotyczy **pętli delegowania i staranności** — czyli systematycznego budowania zaufania do analitycznych możliwości AI poprzez testowanie go na danych, które już rozumiesz. Dzięki temu możesz lepiej zrozumieć, jak AI wesprze Twoje konkretne potrzeby.

---

## Jak działa pętla delegowania

Proces zaczyna się od delegowania. Oto jak to wygląda:

1. Zidentyfikuj konkretne zadanie analityczne, które wykonujesz regularnie i chcesz delegować do AI.
2. Znajdź dane z przeszłości, dla których już przeprowadziłeś analizę.
3. Pracuj z AI, aby odtworzyć to, co zrobiłeś — oceniając co działa, a co nie.
4. Udoskonal swoje podejście i przetestuj ponownie.

Jeśli AI potrafi odtworzyć Twoje znane wyniki, wiesz jak go używać i możesz mu ufać przy podobnych zadaniach w przyszłości. Jeśli nie — nauczyłeś się, że tego zadania nie powinieneś delegować.

---

## Przykład: Rio i Valley Veterans Services

Poznaj **Rio**, dyrektora programu w Valley Veterans Services. Co kwartał analizuje frekwencję w programach wraz z wynikami zatrudnienia — oblicza wskaźniki uczestnictwa, śledzi miesięczne zmiany i sprawdza, czy frekwencja koreluje z sukcesem w znalezieniu pracy. Ta analiza zajmuje mu regularnie wiele godzin.

### Rozważając delegowanie

Rio wie, że chce nadal korzystać z wyników tej analizy, aby ulepszać swój program. Chce samodzielnie interpretować wyniki, ale chętnie pozbyłby się żmudnego czyszczenia danych i formuł. Aby sprawdzić, czy AI sprawdzi się w tym scenariuszu, testuje go na danych z poprzedniego kwartału — zna dokładnie wyniki tej analizy i ma surowe, nieuporządkowane dane sprzed jej przeprowadzenia. To jego przypadek testowy.

### Pętla w działaniu

Rio wgrywa dane i zaczyna pracę z AI, używając **opisywania** i **oceniania** do przeprowadzenia analizy. Po każdej odpowiedzi AI sprawdza wyniki względem tego, co wie, i notuje potencjalne luki w rozumowaniu modelu.

**Pierwsza próba:**

> „Udostępniam dane o frekwencji i wynikach zatrudnienia z naszego programu szkoleń zawodowych z ostatniego kwartału. Przeanalizuj wzorce uczestnictwa w ciągu trzech miesięcy i przedstaw graficznie korelacje między poziomem frekwencji a sukcesem w zatrudnieniu. Szczególnie interesuje mnie to, czy regularna frekwencja przewiduje lepsze wyniki w znalezieniu pracy."

AI odpowiada podsumowaniem. Rio nie zakłada jednak, że to fakty — sprawdza wyniki i notuje co jest dobre, a co nie. AI poprawnie zidentyfikowało korelację między frekwencją a zatrudnieniem, ale pominęło kluczowy wgląd dotyczący połączonego programu pomocy mieszkaniowej i zatrudnienia.

**Doprecyzowanie:**

Rio prosi AI, żeby spróbowało ponownie, zwracając szczególną uwagę na typ programu. Tym razem AI wyłapuje swój błąd. Rio notuje, że w przyszłych kwartałach będzie musiał wyraźnie prosić AI o uwzględnienie typu programu przy analizie.

**Trudniejszy test:**

> „Czy możesz też spojrzeć na to według daty zapisania się uczestników?"

AI odpowiada — Rio obserwuje, że mimo braku danych o zapisach, AI mogło pomóc je wyodrębnić. Notuje, żeby później skrzyżować te wyniki.

### Wnioski Rio

Po tym procesie Rio systematycznie zwalidował, co AI potrafi, a czego nie, przy jego kwartalnych raportach:

- Z odpowiednim opisem AI potrafi dokładnie odtworzyć analizę, którą wcześniej robił ręcznie.
- AI potrzebuje dat zapisów w danych, żeby przeprowadzić analizę kohortową — inaczej będzie próbowało je wywnioskować, czego Rio nie chce.
- Rio ma teraz przetestowane podejście, które może pewnie stosować z nowymi danymi, oraz jasne notatki o tym, jakie informacje musi dołączyć i jaki kontekst nadal musi dodawać samodzielnie.

Gdy Rio używa tego zwalidowanego podejścia z nowymi danymi, jego staranność trwa nadal — sprawdza, czy liczby mają sens, bierze odpowiedzialność za końcowy raport i jest transparentny co do roli AI. Ale teraz działa z zwalidowaną pewnością, a nie zgadywaniem.

---

## Framework: jak to zastosować

1. **Zidentyfikuj konkretne zadanie analityczne** do delegowania — bądź precyzyjny co do tego, czego potrzebujesz.
2. **Znajdź dane z przeszłości**, dla których już przeprowadziłeś analizę. Potrzebujesz właściwych odpowiedzi, żeby ocenić, czy AI do nich dojdzie.
3. **Pracuj z AI, aby odtworzyć przeszłą analizę** i systematycznie oceniaj wyniki:
   - Co AI wyprodukowało?
   - Jak podeszło do zadania?
   - Jak zakomunikowało wyniki?
4. **Zidentyfikuj luki, udoskonal delegowanie i przetestuj ponownie.**

Jeśli możesz zwalidować, że AI produkuje poprawne wyniki — masz podejście, które możesz pewnie stosować na nowych danych. Jeśli nie możesz tego osiągnąć po kilku udoskonaleniach — nauczyłeś się, że tego zadania nie powinieneś delegować.

---

## Co jeśli nie czujesz się pewnie z danymi?

Jeśli nie jesteś zbyt biegły w analizie danych i nie byłbyś w stanie samodzielnie wychwycić luk w procesie — AI może być też przydatnym narzędziem do burzy mózgów i wdrażania rozwiązań, na które sam byś nie wpadł.

Modele AI są wyjątkowo dobre w kodowaniu, więc mogą pomóc z:

- pisaniem formuł Excel
- reformatowaniem nieuporządkowanych danych
- i wieloma innymi zadaniami

W takich przypadkach po prostu przynieś swoje pytanie lub pomysł do AI i poproś o pomoc w zrozumieniu, jak mogłoby wyglądać rozwiązanie — tak jak pracowałbyś z analitykiem danych w swoim zespole. Podczas pracy z AI ciągle proś o wyjaśnienia, żebyś mógł śledzić proces i rozumieć końcowy wynik.

Pamiętaj: **walidacja buduje pewność, ale nie eliminuje odpowiedzialności.** Nadal jesteś odpowiedzialny za sprawdzenie, czy wyniki mają sens, i za transparentność co do roli AI w procesie analizy.

---

## Zastosowania

To podejście działa przy każdym zadaniu analitycznym, które rozważasz:

- analiza darczyńców
- prognozowanie budżetu
- synteza ankiet
- śledzenie wyników

Najpierw przetestuj, zwaliduj co działa, a potem stosuj z większą pewnością. Albo dowiedz się, czego w ogóle nie powinieneś delegować.

---

## Co dalej

W następnej lekcji przyjrzymy się augmentacji przepływu pracy i temu, jak stosować te same zasady, gdy AI obsługuje rutynowe zadania w Twoim imieniu.
