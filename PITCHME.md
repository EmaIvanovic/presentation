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
### Prakticni primeri
![](images/git.jpg)

