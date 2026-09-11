________________________________________
<div align="center">

<b>
Jak lewarowane ETF-y wpływają na zmienność rynku?</b>

</div>

________________________________________

Materiał na youtube: https://www.youtube.com/watch?v=yTaDeAVQkyM](https://www.youtube.com/watch?v=4hm9FbO4T48

Artykuł: wkrótce

________________________________________

**Opis problemu**:

Czy rosnąca skala rynku lewarowanych ETF-ów zwiększa potencjalne znaczenie ich mechanicznego rebalansowania - szczególnie w okresach rynkowego stresu?

Jeszcze kilka lat temu dostępne badania nie potwierdzały istotnego wpływu rebalansowania LETF na zmienność całego rynku. Jedno z badań z 2018r. (https://www.sciencedirect.com/science/article/abs/pii/S1386418117302604) obejmujące okres 2006–2014 pokazało, że po uwzględnieniu rzeczywistych fund flows nie było przekonujących dowodów na to, że rebalancing lewarowanych ETF-ów istotnie zwiększał tzw. early i late-day returns (tj. okresy w których występuje wzmożona aktywność LETF w celu dokonania rebalancingu) i zmienność całego rynku.

Mechanizm jest jednak bardziej skomplikowany, ponieważ rzeczywiste fund flows mogą częściowo kompensować lub zwiększać transakcje wynikające ze zmian wartości aktywów. Załóżmy, że LETF ma $10 mld AUM i rynek spada. Sam spadek wartości aktywów zmniejsza ekspozycję funduszu i tworzy potrzebę jej ograniczenia. Jeżeli jednak jednocześnie do LETF-u napływają nowe środki, część tej potrzeby może zostać pokryta nowym kapitałem. W efekcie rzeczywisty rebalancing może być mniejszy lub większy od wartości wynikającej wyłącznie z AUM i zmiany aktywa bazowego. Nie oznacza to jednak, że LETF-y nie wpływają na ceny. Wniosek był znacznie bardziej precyzyjny: po uwzględnieniu rzeczywistych przepływów kapitału nie znaleziono przekonujących dowodów, że ich rebalancing w badanym okresie istotnie zwiększał późne zwroty i zmienność całego rynku.

Problem polega jednak na tym, że świat LETF-ów bardzo mocno zmienił się od czasu badanego okresu.

Od 2020 r. skala rynku lewarowanych ETF-ów gwałtownie wzrosła, a szczególnie dynamiczny rozwój nastąpił w technologii, półprzewodnikach i produktach opartych na pojedynczych spółkach. Dlatego wynik uzyskany dla lat 2006–2014 nie odpowiada jeszcze na pytanie, czy w obecnych warunkach, przy znacznie większej skali LETF-ów, ich wpływ na rynek nadal jest ograniczony.

________________________________________

**Założenia**:

- badanie oparto na zbiorze z ETFDB obejmujym 230 lewarowanych produktów o łącznym AUM wynoszącym $147 mld na dzień 6 sierpnia 2026 r.: https://etfdb.com/etfdb-category/leveraged-equities/

- okres badania: sierpień 2021 - sierpień 2026 (realnie dla LETF single stock to okres 08.2022-08.2026 (w sierpniu 2022 powstał pierwszy LETF single stock dostępny w naszym zbiorze danych))

- skupiono się na największych LETF technologicznych i półprzewodnikowych (TQQQ (3x Nasdaq-100), SOXL (3x SOX tj. indeks na półprzewodniki) oraz QLD (2x Nasdaq-100)) oraz dostępnych w bazie single-stock LETF (dla 20 spółek, m.in. NVDA, TSLA, MU, SMCI), czyli segmentach, w których skala lewarowania jest obecnie szczególnie duża (LETF sektorowe) lub ich popularność dynamicznie rośnie (LETF single stock)

- w przypadku spółek posiadających kilka lewarowanych produktów ich potencjalną presję rebalancingu zsumowano. Dzięki temu np. NVIDIA jest analizowana łącznie poprzez ekspozycję wynikającą z NVDL i NVDU, a Tesla poprzez wszystkie zakwalifikowane LETF-y znajdujące się w naszej bazie.

-  dla każdego LETF oszacowaliśmy potencjalną presję rebalancingu przy jednodniowym ruchu aktywa bazowego o 1%. Dla funduszu o dźwigni L wartość ta jest liczona jako: **Rebalancing Pressure = AUM × L × (L − 1) × 1%**

W przypadku funduszu 2x oznacza to potencjalną transakcję odpowiadającą około 2% jego AUM przy 1-procentowym ruchu aktywa bazowego. Dla funduszu 3x byłoby to już około 6% AUM. Mechanizm ten wynika z konieczności zwiększania ekspozycji po wzrostach i zmniejszania jej po spadkach, czyli z procyklicznego charakteru codziennego resetowania dźwigni.

Ważne: jest to miara potencjalnej, a nie rzeczywiście zrealizowanej presji rebalancingu. Nie posiadamy dziennych danych o rzeczywistych transakcjach funduszy, dlatego nie możemy stwierdzić, że dokładnie taka wartość została faktycznie kupiona lub sprzedana. Takie podejście wynika z ww. braku historycznych danych AUM.

-  potencjalną presję rebalancingu zestawiono z płynnością aktywa bazowego. Dla każdego aktywa bazowego obliczono medianę oraz średnią dziennego dollar volume z ostatnich 12 miesięcy, wykorzystując dane dzienne z yfinance. Na tej podstawie stworzono wskaźnik: **LETF Pressure / Median Dollar Volume** pokazujący, jak duża jest potencjalna presja rebalancingu (przy wzroście aktywa bazowego o 1%) w relacji do typowego dziennego obrotu daną akcją/etf.

-  rynkowy stres: Aby uniknąć sytuacji, w której każda spółka ma własne „dni stresowe”, wykorzystano QQQ jako wspólną miarę stanu rynku technologicznego. Za dzień stresowy uznano sesję, podczas której absolutna dzienna stopa zwrotu QQQ znajdowała się powyżej 90. percentyla dla całego badanego okresu.


________________________________________

**Źródła danych**:

- https://etfdb.com/etfdb-category/leveraged-equities/,
  
- biblioteka yahoo finance

________________________________________

**Podsumowanie i wnioski dla inwestora**:

**1.Skala LETF-ów jest już wystarczająco duża, aby ich rebalancing mógł mieć znaczenie dla rynku.** Na 06.08.2026 TQQQ i QLD miały łącznie $50,4 mld AUM, a potencjalna presja rebalancingowa przy 1% ruchu Nasdaq-100 wynosiła ok. $2,47 mld. W przypadku SOXL potencjalna presja odpowiadała aż 55,5% mediany dziennego obrotu SOXX.

**2. Spółki z większą ekspozycją na LETF są generalnie bardziej zmienne, zarówno w normalnych warunkach, jak i podczas rynkowego stresu.** Nie możemy jednak stwierdzić, że jest to efekt działania LETF - bardziej zmienne spółki mogą być jednocześnie częściej wybierane przez inwestorów korzystających z lewarowanych produktów.

**3. Nie znaleźliśmy przekonującego dowodu, że większa ekspozycja na LETF powoduje silniejsze względne wzrosty zmienności podczas market stress.** Grupa HIGH Exposure miała wprawdzie wyższą zmienność, ale jej Stress Multiplier był niższy niż w grupie LOW (2,67x vs 3,01x). 

**4. Pojawia się natomiast ciekawy sygnał w analizie kierunkowej:** w części najbardziej eksponowanych spółek (SMCI, TSLA) ruchy spadkowe były silniejsze względem Nasdaq-100 niż ruchy wzrostowe. Jest to zgodne z teoretycznym mechanizmem procyklicznego rebalancingu, ale wynik jest wrażliwy na niewielką liczbę obserwowanych spółek i nie powinien być traktowany jako dowód przyczynowości. 

**5. Analiza przed i po pojawieniu się LETF również nie pokazuje trwałego zwiększenia podatności spółek na rynkowy stres.** Średni Stress Multiplier spadł z 3,03x do 2,80x, a zależność między obecną ekspozycją LETF a zmianą tego wskaźnika była praktycznie zerowa.

**LETF-y należy traktować jako potencjalny wzmacniacz istniejących ruchów, a nie jako samodzielny czynnik wywołujący zmienność.** Ich znaczenie jest największe tam, gdzie potencjalna presja rebalancingowa jest duża w relacji do płynności aktywa bazowego. W przypadku najbardziej eksponowanych spółek technologicznych może to być dodatkowy czynnik ryzyka, szczególnie podczas gwałtownych ruchów rynkowych.
