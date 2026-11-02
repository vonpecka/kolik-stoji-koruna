# Metodika: Kolik stojí koruna

Verze 1 (návrh k připomínkám)

Tento dokument popisuje, co a jak počítáme, dřív než vzniknou výsledky.
Každá pozdější změna metodiky projde v tomto repozitáři samostatnou větví
a bude zapsaná v tabulce verzí na konci, s důvodem.

## 1. Otázka

Kolik Česko stálo a stojí, že nepoužívá euro, ve srovnání se situací, kdy by
ho používalo?

Odpověď dáváme ve dvou oddělených vrstvách:

- **Vrstva 1: přímý náklad, který jde doložit z dat.** Čistý, po odečtení
  výhod koruny. Uvádíme ho v mld. Kč ročně a kumulativně v dnešní hodnotě.
- **Vrstva 2: makroekonomický kontext.** Převzaté odhady dopadu eura na
  růst HDP z odborné literatury.

Vrstvy se nesčítají. Vrstva 2 zahrnuje i efekty, které vrstva 1 počítá
zvlášť, takže by součet počítal totéž dvakrát.

## 2. Srovnávací situace

Počítáme čtyři scénáře, které se liší rokem, od kterého by Česko používalo
euro:

| Scénář | Začátek |
|---|---|
| A | 1. 1. 2004 |
| B | 1. 1. 2009 |
| C | 1. 1. 2012 |
| D | 1. 1. 2019 |

Rok 2004 je vstup ČR do EU, rok 2009 přijetí eura na Slovensku, rok 2019
poslední celý rok před pandemií covidu-19. Žádný z těchto roků není jediný
správný. Scénáře slouží k tomu, aby bylo
vidět, jak moc výsledek závisí na zvoleném začátku. Pokud vyjdou podobně, je
závěr robustní. Pokud ne, uvádíme všechny a rozdíl vysvětlujeme.

Scénář A je stylizovaný: v roce 2004 nemohlo Česko euro přijmout, protože
pravidla EU vyžadují nejméně dva roky v mechanismu ERM II. Počítáme ho jako
horní mez časového rozsahu.

Konec období je poslední rok, za který jsou k dispozici úplná data.

## 3. Vrstva 1: kanály

U každého kanálu počítáme po letech **expozici × jednotkový náklad**, zvlášť
hrubě a čistě (§ 4).

### 3.1 Konverze měn (spready a poplatky)

Jednotkový náklad se mezi skupinami plátců liší o řád, proto se počítá zvlášť:

| Skupina | Expozice | Jednotkový náklad |
|---|---|---|
| firmy, obchod s eurozónou | obrat zahraničního obchodu s eurozónou | kurzový spread pro firemní klienty |
| domácnosti, hotovost a převody | výdaje při cestách do eurozóny, převody | spread a poplatky pro drobné klienty |
| platební karty | transakce v eurech | poplatek za konverzi |
| dynamická konverze měny (DCC) | podíl transakcí s DCC | přirážka DCC |

Výsledek porovnáme s dřívějšími odhady transakčních nákladů z literatury.

### 3.2 Kurzové zajištění

Cena zajištění se odvozuje z forwardových bodů, které odpovídají úrokovému
rozdílu mezi korunou a eurem. Počítá se jako úrokový rozdíl × objem
zajištěných obchodů.

### 3.3 Úroky z úvěrů firem a domácností

Rozdíl sazeb na **nových** úvěrech se **stejnou dobou fixace** v Česku
a ve srovnávacích zemích (§ 6) × objem nových úvěrů v korunách. Rozdíl
sazeb se nenásobí celým stavem dluhu.

**Jedna expozice se nezapočítá dvakrát.** Úvěr v korunách nese úrokový
rozdíl (3.3). Úvěr v eurech u firmy s tržbami v korunách nese zajištění
(3.2) nebo kurzové riziko (3.4), nikdy obojí.

### 3.4 Kurzové riziko nezajištěných firem

Firmy s tržbami v korunách a závazky v eurech nesou kurzové riziko samy.
Kanál započítáme, jen pokud pro něj najdeme spolehlivá data a metodu
(otevřená otázka 3). Jinak ho výslovně vyřadíme s odůvodněním.

### 3.5 Úroky ze státního dluhu

Rozdíl výnosů státních dluhopisů ČR a srovnávacích zemí × nově emitovaný
dluh, po letech. **Počítá se se znaménkem:** v letech, kdy si Česko půjčovalo
levněji než srovnávací země, jde o výhodu koruny a od výsledku se odečítá.

### 3.6 Evropské fondy

Kurzové rozdíly mezi alokací v eurech a čerpáním v korunách, se znaménkem.
Pohyb kurzu mohl vyjít i ve prospěch Česka.

## 4. Hrubý a čistý náklad

- **Hrubý náklad** je to, co zaplatili klienti.
- **Čistý náklad pro společnost** je hrubý náklad minus ta část, která
  zůstala jako příjem tuzemských bank. Ta je přesunem peněz uvnitř
  ekonomiky, ne ztrátou.

Uvádíme obojí. Hlavním výsledkem je čistý náklad.

## 5. Výhody koruny

Od vrstvy 1 se odečítá:

| Výhoda | Jak ji započítáme |
|---|---|
| levnější státní dluh v části období | v kanálu 3.5, se znaménkem |
| kurzový závazek ČNB 2013-2017 | dopad podle analýz ČNB; náklad intervencí uvádíme zvlášť |
| vlastní měnová politika v krizích (2008-2009, 2020, 2022) | převzaté odhady; kde kvantifikace neexistuje, popisně |

Zkušenosti nových členů eurozóny s růstem cen při přechodu na euro (Slovensko,
Chorvatsko) uvádíme v diskusi s daty.

## 6. Srovnávací země a robustnost

- **Hlavní srovnání:** Slovensko.
- **Skupina srovnávacích zemí:** Slovensko, Slovinsko, Estonsko, Lotyšsko,
  Litva, Chorvatsko. Všechny vstoupily do EU v roce 2004 nebo později
  a euro přijaly až po vstupu, takže začínaly z podobné pozice jako Česko.
- **Test robustnosti:** metoda syntetické kontroly.
- **Citlivostní analýza:** začátek (scénáře A-D), konverzní kurz, sazba pro
  převod na dnešní hodnotu, volba srovnávacích zemí a podíl zajištěných
  obchodů.

## 7. Převod na dnešní hodnotu

Náklady z minulých let převádíme na hodnotu ke konci posledního roku s daty
(otevřená otázka 2). Vedle toho uvádíme nominální a reálný součet.

## 8. Vrstva 2: makroekonomický kontext

Převezmeme publikované odhady dopadu eura na HDP Česka, zejména od Úřadu
vlády ČR a ČNB. Nepřepočítáváme je, uvádíme rozsah a zdroj.

## 9. Data a reprodukovatelnost

- Každé číslo ve studii vzniká skriptem z dat v tomto repozitáři. Text čísla
  jen cituje.
- Zdroje dat: ČNB, ECB, Eurostat, ČSÚ, Ministerstvo financí. Každý zdroj má
  v manifestu adresu, archivní kopii a otisk SHA-256 staženého souboru.

## 10. Otevřené otázky

1. **Konverzní kurz:** jakým kurzem by se koruna v každém scénáři
   převedla na euro. Ovlivňuje kanály 3.3 a 3.5.
2. **Sazba pro převod na dnešní hodnotu:** výnos desetiletých státních
   dluhopisů ČR, nebo inflace.
3. **Kurzové riziko nezajištěných firem:** zdroj dat a metoda.

## 11. Využití umělé inteligence

Na přípravě textu a rešerši se podílely nástroje umělé inteligence (Claude,
Anthropic). Všechna čísla počítají deterministické skripty v tomto
repozitáři. Kdokoli je může spustit a výsledek ověřit.

## Verze metodiky

| Verze | Změna | Důvod |
|---|---|---|
| 1 | první verze | |
