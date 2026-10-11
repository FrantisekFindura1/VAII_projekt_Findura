# Webová aplikácia pre zvierací útulok a adopcie

František Findura

5ZYI33

## Stručný opis projektu

Webová aplikácia slúži ako platforma pre útulok zvierat. Prezentuje zvieratá, ktoré hľadajú nový domov a spravuje žiadosti o ich adopciu. Je určená pre ľudí ktorí si chcú adoptovať laebo pozrieť opustené zvieratá a taktieť pre zamestnancov útulku ktorí budú sledovať stav žiadostí a aktualizovať databázu.

## Role v projekte

návštevník - môže prezerať zoznam zvierat na adpociu a flitrovať medzi nimi

registrovaný používateľ - používateľ, ktorý môže podať žiadosti na adopciu a spravovať svoj profil

správca - admin, pridáva nové zvieratá, nahráva foto, upravuje ich stav, spravuje žiadosti

## Prípady použitia podľa rolí

Návševník si vyhľadá zviera v ponuke podľa filtrov, vytvorí si nový účet a prihlási sa tým do systému, tento používateľ odošle žiadosť o adopciu pre vybrané zviera.

Správca pridá nové zvieratá do databázy vrátane jeho fotografie, popisu, zdravotneho stavu atď., správca spravuje stavy žiadostí.

## Plánované entity

Pouzivatel

Zviera - reprezentuje konkrétne zviera v útulku(id, meno, druh, vek, zdrav\_stav, foto, popis) 1:N k ZiadostOAdopciu

ZiadostOAdopciu - žiadosti používateľa o zviera(id, datum,status, sprava\_od\_ziadatela, pouzivatel\_id, zviera\_id) N:1 k Použivateľovi a Zviera

Prispevok - financne alebo materialne dary pre útulok(id, suma, datum, sprava, pouzivatel\_id) N:1 k Pouzivatelovi

## Vzťahy medzi entitami

medzi Zviera a ZiadostOAdopciu je vzťah 1:N - jedno zviera môže mať viacero žiadostí, každá žiadosť patrí 1 zvieraťu

Pouzivatel a ZiadostOAdopciu je vzťah 1:N - jeden používateľ môže podať viacero žiadostí

Pouzivatel a Prispevok je vzťah 1:N - používateľ môže prispieť viac krát

## Hlavné stránky aplikácie

1.úvodná stránka - prehľad najnovšie pridaných zvierat a štatistiky

2.katalóg - stránka s interaktívnym zoznamom a filtrovaním zvierat

3.detail zvieraťa - podrobné info o vybranom zvierati

4.prihlásenie/registrácia

5.admin - spravovanie zvierat

6\.žiadosti použivateľov

## Rozdelenie funkcionality

základné:

autentifikácia používateľov s heslami uloženými v hash tvare, implementácia min. 3 entitných tabuliek, server aj klient validácia formulárov, CRUD operácie nad 2 entitami, práca so súbormi - fotky, responzívny dizajn , min. 20 CSS pravidiel



rozširujúce:

Pokročilá kontrola formulárov na strane klienta, použitie pokročilých vlastností CSS

