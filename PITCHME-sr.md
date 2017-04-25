#HSLIDE
### Sistemi za verzionisanje (VCS)

#HSLIDE

### Šta su sistemi za verzionisanje programa / koda?

Alati koji nam omogućavaju vodjnjenje evidnecije izmenama nad projektom bilo da radimo sami ili u grupi. 

#HSLIDE

### Koji sve tipovi sistema postoje?
 Lokalni | Centralizovani | Distribuirani

![](images/vcs.png)

#HSLIDE
### Uvod u Git
![](images/uvod.png)

#HSLIDE
###Zašto git?
U odnosu na druge se istakao svojom brzinom, integritetom nad podatcima, distribuiranošću i mogucnošću za nelinearnim tokom rada.

#HSLIDE
###Kako je zamišljen?
Kao mreža zasebnih repozitorijuma koji se mogu medjusobno sinhronizovati (distribuiranost), iz toga proističe da svaka izmena koja je napravljena utiče samo na lokalni repozitorijum sve dok se ne izvrši sinhronizacija sa drugim repozitorijumom.

#HSLIDE
###Git VS SVN
![](images/gvs.png)

#HSLIDE
###Kako se najčešce koristi?
Kao kombinacija centralizovane i distribuirane mreže gde se sve izmene sinhronizuju preko jednog udaljenog repozitoriujma (Github, Bitbcuket, Gitlab...)git-a

#HSLIDE
### Repozitoriujum
Mesto na kome se cuvaju svi commit-ovi sa promenama koje smo do sada napravili. Moze biti lokalni ili udaljeni. Nalazi se u našem projektu u `.git` dorektorijumu.

#HSLIDE
### Commit

Commit predstavlja stanje projekta u odredjenom trenutku. Više povezanih commit-ova formira graf koji predstavlja istoriju našeg projekta.

#HSLIDE
###Index i commit
Mesto gde se pripremaju izmene za commit
![](images/index.png)

#HSLIDE
### Dobra praksa  

Commit-ove treba često praviti, gde svaki od njih predstavlja jedinstvenu celinu koja je jednostavna za razumevanje i laka za uklanjanje.

#HSLIDE
### HEAD  
HEAD je tag koji predstavlja pointer na odredjeni commit obicno je to vrh grane ali moze predstavljati bilo koji commit kroz istoriju.

#HSLIDE
### Linerana istorija koda

Idealna situacija u kojoj su se izmene dešavale sekvencialno jedna za drugom. Projekat je zapocet sa stanjem , `a` pa su napravljene izmene `b`, `c`, . . . sve do prve verzije. U ovome nam dosta pomaze komanda `rebase` koju ćemo kasnije opisati.

![](images/linearno.png)

#HSLIDE
### Grafovi i grananje

Grananje predstavlja nelinearno verzionisanje i ono se predstavlja putem grafova.

![](images/grananje.png)

#HSLIDE
### Udaljeni repozitorijum

![](images/remote repo.png)


#HSLIDE
###.gitignore

Datoteka u kojoj su navedeni svi direktorijumi i datotoeke koje želimo da izuzmeo iz verzionisanja (.idea, /log, /*.yml...)

#HSLIDE
### Prakticni rad
![](images/git.jpg)