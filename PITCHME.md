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
### Grafovi i grananje

Grananje predstavlaj nelinearno verzionisanje i ono se moze predstaviti pitem grafova

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
# inicializacija novog repozitorijuma
$ cd <repo name>
$ git init

# kloniranje postojeceg repozitorijuma
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
###Index i prvi commit
Mesto gde se pripremaju izmene za commit
![](images/index.png)

#HSLIDE
```
# dodavanje datoteke u pracanje
$ git add <name>
# prikazivanje trenutnog statusa
$ git status
# prvi commit
$ git commit -m 'Prva izmena'
$ git status
# prikazivanje istorije projekta
$ git log
# formatiran prikaz
$ git log --graph --all --oneline --decorate
```

#HSLIDE
### HEAD
Referenca na 'trenutni' SHA1 commit-a na kome se nalazimo

#HSLIDE
### Detached HEAD
Bilo koji checkout na commit koji nije ime grane dovodi do ovog stanja, cak i na SHA1 koji je poslednji na grani (ovo se moze predstaviti kao anonimna grana). Samo checkout na ime lokalne grane izbegava ovaj slicaj.

```
# fix for deached HEAD
git checkout develop
```

#HSLIDE
### Kretanje kroz commitove

```
git log
git checkout <commit sha> or <tag> or <branch>
git checkout HEAD~5
```

#HSLIDE
### Stash
Mesto za privremeno cuvanje izmena

```
# stash sa dafault imenom
$ git stash
# stash sa specificiranim imenom
$ git stash <-u> <save [name]>
# izlistavanje svih stash-eva
$ git stash list
```

#HSLIDE
### Uklanjanje promena iz indexa

```
# obrisi datoteku
$ git rm <name> 
# Ukloni iz repozitorijuma ali ostavi fizicki
$ git rm --cached <name> 
# Ukloni sve izmene od poslednjeg commit-a
$ git checkout . or <name>
```

#HSLIDE
### Uklanjanje commit-ova iz lokalnog repozitorijuma

```
# obrisi sve commit-ove i njihove promene
$ git reset <commit sha> --hard
# obrisi sve commit-ove ali ostavi njihove izmene u indexu
$ git reset <commit sha> --soft
```

#HSLIDE
### Uklanjanje commit-ova iz udaljenog repozitorijuma
Vrsi se tako sto se napravi novi commit sa izmenama koje negiraju predhodno poslate

```
# kreira novi commit
$ git revert 
$ git push
# brise lokalni commit
$ git reset <sha> --hard
# nasilno prepisuje istoriju udaljenog repozitorijuma
$ git push mathnet -f
```

#HSLIDE
### Cherry pick

Preuzima bilo koji commit i primenjuje ga gde god da se trenutno nalazimo, kao rezulat nasanjenovi commit sa istim izmenama i drugim SHA id-em.

```
# ceo commit
cherry-pich <sha>
# deo commit-a
cherry-pick -n (--no-commit) <sha>
```

#HSLIDE
### Conflict
Nastaju kada git neume sam da razresi dve promene koje su se desila na istoj liniji koda. Tada se od korisnika zahteva da otvori datoteku i rucno da obrise visak izmena i izvrsi commit

```
<<<<<<< HEAD
open an issue
=======
ask your question in IRC.
>>>>>>> branch-a

git add
git commit
```

#HSLIDE
### grananje

```
git branch
git branch <name>
git checkout -b <name>
develop u sadasnju granu
git merge develop (fast forvard)

git rebase develop
```


