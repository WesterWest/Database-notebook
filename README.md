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

>**Monolitická architektura**
Vývojové prostředí i klientská aplikace jsou umístěny na lokálním počítači
Aplikace přistupuje přímo k souborům na lokálním pevném disku nebo na síťovém souborovém serveru.
Databázové služby i logická komunikace se implementují jako součást klientské aplikace
_Microsoft access_

>**Klient/Server**
Základní myšlenkou architektury je oddělení databázových služeb od klienta
Komunikace mezi klientem a databází je flexibilní a otevřená


 
