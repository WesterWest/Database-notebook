Databáze
=========
***********************************************

**relační databáze** 1970 - Codd
***********************************************

> **databáze** = strukturovaná data, umístěná v tabulkách

> **relační databáze** - umožňuje pracovat současně s daty z více tabulek

> **tabulka** - entita v určitém dtb prostředí
- spojujeme vazbami s určitou kardinalitou (mohutností)

> **atribut** - vlastnost stejného druhu

> **vazba** - rozlišujeme parcialitu (povinnost ve vztahu)
- >**vazba 1:N** - jeden záznam v jedné tabulce odpovídá N záznamů v druhé tabulce

**RDBMS**
- software, který řídí data směrem k organizaci a strukturuje je
- podporuje datové modely
- spravuje databázove struktury (tabulky, vazby atd.)
- spravuje transakce
- strukturalizuje požadavky aplikací

> **model reality** - část reálného světa určený pro zpracování v dtb systému

**doporučené konvence pojmenování objektu:**
- bez diakritiky
- zkráceno se zachováním významu
- bez mezer
- podtržítka nebo velká písmena (_camelCase, PascalCase nebo snake_case_)
- ne klíčová slova

> **primární klíč** - množina atributů jednoznačně definující každý záznam tabulky
- dělí se na:
  - přirozený
  - umělý
- také na:
  - jednoduchý
  - složený


> **kandidátní klíč** - množina atributů, které by _mohly_ být primárním klíčem, ale není vhodná

> **foreign key** - zprostředkovává spojení na primární klíč druhé tabulky

> **id** - unikátní celé číslo

> **Monolitická architektura**
Vývojové prostředí i klientská aplikace jsou umístěny na lokálním počítači
Aplikace přistupuje přímo k souborům na lokálním pevném disku nebo na síťovém souborovém serveru.
Databázové služby i logická komunikace se implementují jako součást klientské aplikace
_Microsoft access_

> **Klient/Server**
_Základní myšlenkou architektury je oddělení databázových služeb od klienta_
Komunikace mezi klientem a databází je flexibilní a otevřená
Databázové služby jsou prováděny na výkoném PC což umožnujě:
- centralizovanou správu systému
- zavedení bezpečnostních opatření
- přístup ke sdílení prostředků

> Server představuje databázi s jejími službami jako například:
- vyhledávání
- spojování
- načítání
- aktualizace
- analýza dat
Databáze se zkládá z fyzického prostoru pro uložení dat a z Databázových služeb (SŘDB)
_Veškerý přístup k datům probíhá prostřednictvím serveru, fyzicky se k žádným datům nikdo nedostane_

> Klient program nebo automatizovaný proces, který interaktivně se serverem
Do kategorie klient spadá veškerý software, který spolupracuje se serverem
Z databáze může data získávát i zapisovat
Přímý k datům nikdy nemá
Vždy komunikuje serverem a ten teprve s daty

Příklady klientů:
- utility pro správu systému
- sytém pro adhoc dotazy a sestavy
- uživatelské aplikace thin and thicc
- webové aplikace

Výhody K/S (vzhledem k předchozím architektirám):
- modulární charakter aplikací
- intuitivní vývoj a provoz klientů v různem GUI
- zjednodušení údržby aplikace a zvýšení bezpečnosti Informačního Systému

architektura K/S má několik podtipů, z nichž mezní hodnoty se nazývají _inteligentní server_ či _inteligentní klient_

> **Integrita** = splnění všech integritních omezení, které jsou na danou databázi požadovány

> **Integrita dat** = pravidla pro zajištění správnosti a konzistence upravených dat
Základní rozdělení pro integritu na sloupci je _null_ a _notnull_

Proč integrita? - Snaha odchytit chybu už na vstupu

> **Typy integrity** :
- deklarační- trvale přítomnaá
- procedurální - pouze pro nějakou proceduru

> **Datová integrita**:
- Doménová (atributy)
- Entitová = definuje pravidla pro údržbu integrity jednotlivých relací.
- Referenční integrita = zajišťuje zachování potřebných vztahů mezi relacemi; pravidlo, jež definuje platné hodnoty atribudů

> základní rozdělení:
- null
- not null
------------------------------------------------------
- doménová, standardní testy
- vstupní hodnota respektuje dolní/horní mez
- vstupní hodnota odpovídá tzv. masce
- možnost kontroly podle číselníku

> **Normalizace dat** = pravidla jak postupovat při transformaci entit a relací ER modelů na strukturu
fyzického uspořádání tabulek a vazeb v reálné databázi
(= proces rozhodování jaký sloupec umístíme v jaké tabulce)

**Proč normalizovat?**
- odstranění redundatních (opakujících se) dat
------------------------------------------------------
> **5(6) normálních forem:**
1. NF:
- každý atribut obsahuje jen atomické hodnoty, dále již nedělitelné

2. NF:
- je v první formě
- každý atribut **plně závislý** na celém primárním klíči

3. NF:
- je v druhé formě
- žádný z jejích atributů není tranzitivně závislý na klíči
- relace je ve třetinové formě pokud je ve druhé a všechny atributy jsou navzájem nezávislé

# SQL

## Agregační funkce
- mohou mít například funkce min() max() číslo a datum
- včetně group by
příklad asi:
`select count(id_os) from osoby;
select sum(plat_max) as vyplata_celk fro  osoby;
select max(plat) as nejvyssi as osoby;
min()
aug()`