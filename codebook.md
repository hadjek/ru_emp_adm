# Administrative divisions and population of the Russian Empire in 1897

**Tomasz M. Jankowski**  
to.j123@poczta.fm [remove 123]

Readme  
Database, v. 1.0


Last update: January 25, 2018


## Table adm1


### adm1_id
integer

Unique 2-digit number identifying province. Follows numbering convention used in contemporary statistical publication of the Russian Empire, in which provinces are arranged alphabetically by geographical region:
- European Russia: 01 to 50,
- Congress Poland: 51 to 60,
- Caucasus: 61 to 71,
- Siberia: 72 to 80,
- Central Asia: 81 to 89.

Additionally Zakatalsky _okrug_ was assigned 90 and Finish provinces were assigned 91 to 98. These provinces (most likely) did not have their official number assigned.

Note that leading 0 may be removed when opening CSV files in Excel.

### adm1  
character

Name of the province (in Russian in Cyrillic).


### adm1_type  
character

Type of the province (in Russian in Cyrillic): _gubernya_, _oblast_, etc.


### adm1_center  
character

Place name of the political center of the province (in Russian in Cyrillic).


### adm1_geonameid  
integer

Identification id of the province center from the [Geonames](http://geonames.org) database, which may be used for retrieving e.g. geographic localisation. 


### adm1_alternate  
character

Alternate names of a province. Semicolon separated. Variations do not reflect historical spelling variations, only changes in names overtime (before and after 1897) or names in foreign languages. 


### adm1_link  
character

URL to Russian Wikipedia.


### adm0  
character

Name of the political region of the Russian Empire (in Cyrillic).


## Table adm2

### adm1_id  
integer

Unique 4-digit number identifying district. First two digits identifies province (adm1_id), last two digits identify district within the province (in alphabetical order).
Note that leading 0 may be removed when opening CSV files in Excel.

### adm1  

See above. Used for relational purposes.


### adm2  
character

Name of the district (in Russian in Cyrillic)


### adm2_type  
character

Type of the province (in Russian in Cyrillic): _uyezd_, _okrug_, etc.


### adm2_center  
character

Place name of the political center of the province (in Russian in Cyrillic).


### adm2_geonameid  
integer

Identification id of the district center from the [Geonames](http://geonames.org) database, which may be used for retrieving e.g. geographic localisation. 


### adm2_alternate  
character

Alternate names of a district. Semicolon separated. Variations do not reflect historical spelling variations, only changes in names overtime (before and after 1897) or names in foreign languages. 

Local names provided completely for Estonian and Finnish districts.


### adm2_area  
double

Area of the district in square versts (1 vest = 1.0668 km).

Troitsky’s summaries provide data for a few grouped districts:
- Aksha, Nerchinsk, Chita (129480);
- Troitskosavsk and Verkhneudinsk (113750);
- Baysky and Zmyeinogorsky (169256.3).
Area for individual districts was estimated based on population distribution (Aksha district population 2x to reflect possible lower population density).

Area of Zmyeinogorsky district taken from [Wikipedia](https://ru.wikipedia.org/wiki/Змеиногорский_уезд).


### pop_1897_tot  
integer

Total population includes foreigners (иностранных поддананых). Foreigners were not included in totals for religions in Arkhangelskaya, Olonetskaya, Vitebskaya provinces. Number of foreigners was low (less than 1000 per province).


### pop_1897_tot_j  
integer

Total Jewish population.
Does not include Karaites.


### pop_1897_tot_o  
integer

Total population of Russian Orthodoxes and Old Believers (_Yedinoverie_).


### pop_1897_tot_rc  
integer

Total Roman-Catholic population.


### pop_1897_tot_l  
integer

Total Lutheran population.


### info  
character

For selected units additional information is provided, such as changes in names, dates of foundation, and modern names of centers