#HSLIDE
### Sistemi za verzionisanje (VCS)

#HSLIDE

### Sta su sistemi za verzionisanje programa / koda?

Alati koji nam omogucavaju vodnjenje evidnecije izmenama nad projektom bilo da radimo sami ili u grupi. 

#HSLIDE

### Koji sve tipovi sistema postoje?
 Lokalni | Centralizovani | Distribuirani

![](images/vcs.png)

#HSLIDE
### Uvod u Git
![](images/uvod.png)

#HSLIDE

###Zasto git?
Jer se u odnosu na druge istakao svojom brzinom, integritetom nad podatcima, distribuiranoscu i mogucnoscu za ne linearnim tokom rada.

#HSLIDE
###Kako je zamisljen?
Kao mreza zasebnih repozitorijuma koji se mogu medjusobno sinhronizovati (distribuiranost), iz toga proistice da svaka izmena koja je napravljena utice samo na lokalni repozitorijum sve dok se ne izvrsi sinhronizacija sa drugim repozitorijumom.

#HSLIDE
###Kako se najcesce koristi?
Kao kombinaciju centralizovane i distribuirane mreze gde se sve izmene sinhronizuju preko jednog udaljenog repozitoriujma (Github, Bitbcuket, Gitlab...)

#HSLIDE
### Repozitoriujum
Mesto na kome se cuvaju svi commit-ovi sa promenama koje smo do napravil. Moze biti lokalni ili udaljeni. Nalazi se u nasem projektu u `.git` dorektorijumu.

#HSLIDE
### Commit

Commit predstavlja stanje projekta u odredjenom trenutku kada samo ga nacinilo. Vise povezanih commit-ova formira graf koji predstavlja istoriju naseg projekta.

#HSLIDE
### Dobra praksa  

Commit-ove treba cesto praviti, gde svaki od njih predstavlja jednu ideju ili promenu koja je jednostavna za citanje i laka za naknadno uklanjanje

#HSLIDE
### Linerano istorija koda

Idealna situacija u kojoj su se izmene desavale sekvencialno jedna za drugom. Projekat je zapocet sa stanjem a, pa se napravljene izmjene b, c, . . . sve do prve verzije.U ovo me nam dosta pomaze rebase koji cemo kasnije spomenuti.

![](images/linearno.png)

#HSLIDE
### Grafovi, grananje i spajanje grana

TODO fix Nelinearno verzionisanje koda je zgodan pristup koji nam omogucava podelu tok razvoja na vise paralelnih grana gde bi se u svakoj razvijala tacno odredjena stvar bez remecenja 

![](images/grananje.png)

#HSLIDE
### Prakticni rad
![](images/git.jpg)

#HSLIDE

###Rukovanje

```
# command
git <command> <option 1> <option 2> …

# help
git help <command> …
```

#HSLIDE
###Inicializacija repozitoriuma

```
# initialize new repo
$ cd <repo name>
$ git init

# clone existing repo
$ git clone <https link> or <ssh link>
$ cd <repo name>
```

#HSLIDE
###Konfiguracija

globalna | lokalna | sistemska

```
git config --global
git config config user.name
git config user.email 
...
```

#HSLIDE
###.gitignore

Datoteka u kojoj su navedeni svi direktorijumi i datotoeke koje zelimo da izuzmeo iz verzionisanja (.idea, /log, /*.yml...)

#HSLIDE
###Index
Mesto gde se pripremaju izmene za commit
![](images/index.png)

#HSLIDE
```
# dodavanje datoteke za pracanje
$ git add <name>
# prikazivanje trenutnog statusa
$ git status
# prvi commit
$ git commit -m 'Prva izmena'
$ git status
# prikazivanje istorije projekta
$ git log
```

#HSLIDE