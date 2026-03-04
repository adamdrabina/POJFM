[[SQL]]
###### Integritni omezeni
- entitni PK
- domenove = datovy typ
- referencni PK-FK

###### Rozdeleni klicu
- Superklic
	- slozeny
	- cislo, jmeno, prijmeni, datum narozeni
	- cislo, prijmeni, mail
- Kandidatni klic
	- vybiram kanditaty na PK
	- cislo, mail, rodne cislo
- Primarni klic
	- vyberu vhodny PK
	- musim vybrat jeden

###### Kardinalita (vztahy)
vzdy si rict z obou stran
- 1:1
	- rodne cislo, clovek
	- prezident, stat
	- vin kod, auto
- 1:N
	- majitele, auta
- M:N
	- dum, majitel
###### Normalizace
spojitost s navrhovanim databazi
staci dojit k 3NF (treti normalni formy)

[[1. NF]]
	- splnuje tehdy, kdyz jsou vsechny atributy atomicke (kazdy atribut obsahuje jedinou hodnotu) napr jmeno a prijmeni, ulice a cislo popisne jsou rozdeleny
	- rozdeluju SLOZENE atributy = jmeno a prijmeni, ulice a cislo popisne
	- VICEHODNOTOVY atribut, napr kurzy word, excel, outlook
		- vytvorim druhou tabulku pouze s kurzy
		- a taky propojovaci tabulku, kvuli relaci M:N, kde budou pouze pole s primarnimi klici (ID) obou tabulek