# Administrative divisions and population of the Russian Empire in 1897

**Tomasz M. Jankowski**  
to.j123@poczta.fm [remove 123]

Readme  
Database, v. 1.0


Last update: January 25, 2018


## Introduction

The database contains information on:
1. administrative divisions of the Russian Empire down to the second-level unit;
2. distribution of four religious populations in these units for 1897: Russian Orthodoxes, Jews, Roman Catholics, and Lutherans.

The database provides basic and standardized information on administrative divisions of the Russian Empire, including Congress Poland, Kavkaz, Finland, Siberia, and Middle Asia. Each record contains information on unit name (in Cyrillic), its type, area, alternate names and administrative center. Additionally for each unit total population and population of four religions is given.

The database reflects administrative division for in the beginning of 1897, both in names and the divisions. Thus it is compatible with administrative divisions used in the 1897 census of the Russian Empire and its published results.

For a few minor simplifications see section Simplifications.


## Missing data

A some data is missing in the database:
- area and population data for Finnish districts where the 1897 census was not enumerated,
- administrative centers of a few districts (especiall Finnish),
- geonameids of some province and district centers,
- alternate names of some provinces and districts. Completing them is constant work in progress.


## Naming convention

Most of first-level administrative units are called in Russian _gubernia_ and _oblast_. This file refers to these units as “provinces”. Most of second-level administrative units are called in Russian _uyezd_ and _okrug_. This file refers to these units as “districts”.

All names are provided in Russian in Cyrillic as they were provided in Troitsky’s publication in modernized spelling. In case a place name of unit center has changed since 1897, its historical name is provided.

Note that names of some districts was changed (e.g. Zaslavsky to Izyaslavsky). Naming in the databases is given for 1897.


## Database structure

The database contains two tables listing provinces (adm1) and districts (adm2) separately. Variables adm1_id or adm1 may be used as key for relating districts to corresponding provinces. Note that several districts had the same name (e.g. Belsky). Every combination of adm1 and adm2 is unique, though.


## Simplifiactions

Results of the 1897 census edited by Troitsky were aggregated on the level of districts mostly in accordance with actual administrative divisions. There were a few exceptions.

City-divisions (_градоначальство_) of Kerch-Enikale, Sevastopol, Odessa and Petersburg constituted separate second-level administrative units and did not belong to districts. In Troitsky’s publication and this database Kerch-Enikale and Sevastopol are listed as separate adm2 (_okrugs_), but Odessa and Petersburg are included respectively in the districts of Odessa and Petersburg.

Cities of Kronshadt and [Mykolayiv](https://ru.wikipedia.org/wiki/Николаевское_военное_губернаторство) (rus. Nikolayev) constituted (most likely) separate first-level administrative units, Military-Provinces ([_военное губернаторство_](https://ru.wikipedia.org/wiki/Военный_губернатор_(Россия)), and did not belong to provinces of Kherson and Sankt-Petersburg, respectively. In Troitsky’s publication and this database these two cities are treated respectively as a part of Kherson and Petergofsky district.

Troitsky’s vol 69. lists Zakatalsky _okrug_ as a part of Tbilisi gubernya, but according to Dictionary of Brokgauz & Efron, Zakataly okrug is independent adm1. The database reflects actual divisions and lists Zakatalsky _okrug_ as first-level unit.

Additioanlly, Amurskaya and Zakatalsky provinces were not divided into second-level administrative divisions. For the sake of compatibility these areas were assigned one theoretical second-level division with names of Amurskaya and Zakatalsky. 

Several names Finnish districts are derived from cities other than the biggest cities in the district. If these big cities were not a part of districts, this database does not reflect their separate status.


## Sources

- _Первая всеобщая перепись населения Российской империи 1897 г_. Ed. Николай Александрович Тройницкий, vol. 1–89. Санкт-Петербург: Центральний Статістіческий Комитет Министерства Внутренних Дел, 1899–1905. Tables 12, 13. [https://commons.wikimedia.org/wiki/Category:Первая_всеобщая_перепись_населенiя_Россiйской_Имперiи_в_89_томах](https://commons.wikimedia.org/wiki/Category:Первая_всеобщая_перепись_населенiя_Россiйской_Имперiи_в_89_томах); [https://archive.org/details/Statisticsofthe1897AllRussiaCensus](https://archive.org/details/Statisticsofthe1897AllRussiaCensus), both accessed on Jan 25, 2018. The data has not been validated with errata with an exception for volumes on Kievskaya and Estlyandskaya provinces.
- Закатальский округ. _Энциклопедический словарь Брокгауза и Ефрона_. Vol. 12. Ed. Ф. А. Брогауз, И. А. Ефрон. Санкт-Петербург: И. А. Ефрон, 1894. 
[https://ru.wikisource.org/wiki/ЭСБЕ/Закатальский_округ](https://ru.wikisource.org/wiki/ЭСБЕ/Закатальский_округ), accessed on Jan 25, 2018.
- Финляндия. _Энциклопедический словарь Брокгауза и Ефрона_. Vol. 36А. Ed. Ф. А. Брогауз, И. А. Ефрон. Санкт-Петербург: И. А. Ефрон, 1902. [https://ru.wikisource.org/wiki/ЭСБЕ/Финляндия](https://ru.wikisource.org/wiki/ЭСБЕ/Финляндия), accessed on Jan 25, 2018.
- _Россия. Географическое описание Российское Империи по губерниям и областям с географическими картами_. Ed. А. Е. Рябченко. Санкт-Петербург: Бережливость, 1913. [http://www.runivers.ru/upload/iblock/49c/rossiya.pdf](http://www.runivers.ru/upload/iblock/49c/rossiya.pdf), accessed Jan 25, 2018.


## License

This database may be used solely for the purposes of academic research as long as it is properly cited. You may redistribute the database solely as complete package and with indication of the source.


## Citation

Tomasz M. Jankowski. _Administrative divisions and population of the Russian Empire in 1897_, v. 1.0 (https://github.com/tmjank/ru_emp_adm)

## Files

Database package consists of four files: 

- readme.md
- codebook.md
- adm1.csv (UTF-8, coma separated)
- adm2.csv (UTF-8, coma separated)