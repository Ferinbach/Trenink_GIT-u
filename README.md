# Trénink GIT-u

Git / GitHub od základov (yablko)

Spoznávanie a osvojovanie si rôznych funkcií **GIT-u**, 
za účelom jeho pochopenia tým pádom správneho používania v rámci vlastných, alebo firemných projektov / produktov.  
GIT je celkom zauímavý nástroj pričom je hneď niekoľko verzii / platforiem, kde je s ním možné pracovať.  
Počas tohto kurzu som vyskúšal používanie hneď  4 verzie GIT-u= 3 terminály ( originál Git, cmder- v podstate nešiel a vo VS Visual Code vstavaný terminál ) 
a taktiež vo VS Visual Code vstavané povely / funkcie GIT-u.  
A príde mi to ako len o trochu komplikovanejší spôsob ukladania dát ako je tomu napr. u videohier :D

**Celý yablkov SK video-kurz je zadara na [Youtube](https://www.youtube.com/watch?v=0v5K4GvK4Gs&t=939s) ;)**

Toto sú príkazy, ktoré sú podrobné odprezentované 
a vysvetlené v kurze:

---

### Inštalácia:

Pre Windows yablko odporúča [cmder](https://cmder.app/)

Na Mac-Os spustite 1. príkaz cez terminál 
a nemali by ste mať problém s inštaláciou GIT-u 
a ak aj predsa, tak použite aj 2. príkaz ;)

```
git --version
xcode-select --install
```


Ak sa nedarí, nainštaluj [odtiaľto](https://git-scm.com/download/).

---
### GIT NASTAVENIA

Nastavte si meno a heslo (v prípade, že už používate Github, _tak samozrejme použijete údaje z Vášho GIT-hub účtu_ ;).

```
git config --global user.name "tvojemeno"
git config --global user.email "tvoj@email"
```

---

### GIT- základy:

Aktivácia GIT-u pre vaše projekty

```
git init
```

Následne skontrolujte stav / pozrite sa či a čo sa zmenilo.

```
git status
```

Ak vykonáte zmenu v súbore **a chcete ju preniesť do novej verzie projektu označte ho!**

```
git add (napr.)index.html
```

Následne vytesajte zmenu do "kameňa" ( GIT-u :D)
a to tak, **že po každej zmene pridáte stručný popis zmeny / vykonanej akcie.**

```
git commit -m (napr.)"Pridanie index.html"
```

Taktiež si pozrite vývoj celého projektu- jednotlivé pridané zmeny aj s komentármi (git add a git commit -m).

```
git log
```

Vyššie uvedené povely opakujte s každou zmenou /
úpravou kódu vo Vašich súboroch, ktorú chcete uchovať ;)

---

### KÚSOK GITU NAVYŠE

Označ všetky **.png** súbory z adresá **images**.

```
git add images/*.png
```

Označ všetky z tohoto adresára (okrem vymazaných súborov).

```
git add .
```

Označ všetky z tohoto adresára (vrátane vymazaných súborov).  
  
```
git add -A
```
  
Ak chceš zrušiť označenie súborov.

```
git restore --staged .
```

Commitni všetky **zmenené** (nie nové) súbory.  
Hneď pridaj komentár.

```
git commit -a
git commit -am "upravil som kód, a teraz je dobrý"
```

Vypimpuj log.
Daj ho na jeden riadok.

```
git log --graph --decorate --abbrev-commit --all
git log --graph --decorate --abbrev-commit --all --pretty=oneline
```

Ak uložíš **index.html**, ale pokašľal si to. A chceš sa vrátiť na verziu z gitu.

```
git checkout -- index.html
```

Cez _git log_ nájdeš hash commitu. Skopči prvých pár znakov (napr. **c10e47f**) a takto môžeš skočiť na staršiu verziu projektu.

```
git checkout c10e47f
```

Vráť sa naspať na aktuálnu verziu.

```
git checkout master
```

---

### AKO VYPNÚŤ VIM;)

```
- stlač "i"
- napíš text
- esc
- :wq
- enter
- ;)
```

A šípky **hore/dole** a **q**, ak git log je pridhlý.

---

### REMOTE SERVER (GitHub v mojom prípade) GIT PUSH/PULL

Naklonuj projekt do adresára **hemingway**.

```
git clone https://github.com/yablko/hemingwayovatoro-rotator.git hemingway
```

Vytvor odkaz na externý server (resp. konkrétny repozitár).

```
git remote add origin https://github.com/ty/odkaz-na-tvoj-projekt.git
```

Natlač zmeny z tvojho počítača na server. (Zadaj github meno/heslo.)

```
git push origin master
```

Naťahaj zmeny zo servera do tvojho počítača.

```
git pull origin master
```

Čekni, či na serveri nenastali zmeny.

```
git remote update
git status
```

Plus mínus aké zmeny to boli?

```
git whatchanged origin/master -n 1
```

---

### GIT KONFLIKT !!!

Pozri si kurz;)

---

### GIT VO VISUAL STUDIO CODE

Pozri si kurz;)

---

### GIT BRANCH/MERGE (rozvetvi sa)

Ak robíš **bugfix**, sprav si **bugfix vetvu**. Ak robíš novú **login** fičúru, sprav si **login vetvu**.

```
git branch login
```

Prepni sa do novej login vetvy. Commity o logine rob do nej.

```
git checkout login
```

Vytvor a _okamžite sa prepni_ do novej bugfix vetvy. Commity o bugixerob rob do nej.

```
git checkout -b bugfix
```

Keď máš login fičúru hotovú, prepni sa do hlavnej vetvy.

```
git checkout master
```

A zlúč zmeny z loginu do nej.

```
git merge login
```

Ak chceš nevedieť, kde ti hlava stojí, prečítaj si o [merge vs rebase](https://www.atlassian.com/git/tutorials/merging-vs-rebasing).

---

### CHEAT SHEETS

- https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf  
- https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet  
- https://www.git-tower.com/blog/git-cheat-sheet/  
- https://devhints.io/git-tricks  

---

### ODKAZY Z KURZU, BIBLIOGRAFIA

GIT  
:: https://git-scm.com/  

GIT OFICIÁLNY ONLINE BOOK  
:: https://git-scm.com/book/en/v2  

GIT OFICIÁLNE VIDEÁ  
:: https://git-scm.com/videos  

OFICIÁLNY CHEAT SHEET (pdf)  
:: https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf  

CAMBRIDGE Lecture 6: Version Control (git) (2020)  
:: https://www.youtube.com/watch?v=2sjqTHE0zok  

---

GIT KRAKEN  
:: https://www.gitkraken.com  

SUBLIME MERGE  
:: https://www.sublimemerge.com   
   
GITLAB    
:: https://about.gitlab.com  

BITBUCKET  
:: https://bitbucket.org/product  

---

GITHUB TRENDING  
:: https://github.com/trending  

HEMINGWAYOVÁTORO-ROTÁTOR™  
:: https://github.com/yablko/hemingwayovatoro-rotator  
  
---
    
HYPER (Mac terminal)  
:: https://hyper.is/  

CMDER (pre Win)  
:: https://cmder.net/  

GIT INŠTALÁTOR  
:: https://git-scm.com/book/en/v2/Getting-Started-Installing-Git  

---

Using Version Control in VS Code  
:: https://code.visualstudio.com/Docs/editor/versioncontrol  

Git version control in VS Code (VIDEO)   
:: https://code.visualstudio.com/docs/introvideos/versioncontrol  

How to use Git Integration in Visual Studio Code  
:: https://www.digitalocean.com/community/tutorials/how-to-use-git-integration-in-visual-studio-code  

---

MERGE vs REBASE  
:: https://www.atlassian.com/git/tutorials/merging-vs-rebasing  
:: https://derekgourlay.com/blog/git-when-to-merge-vs-when-to-rebase/  
:: https://www.reddit.com/r/git/comments/56ie0x/git_fastforward_merge_vs_git_rebase_same_thing/  

---

.gitignore  
:: https://git-scm.com/docs/gitignore  
:: https://www.atlassian.com/git/tutorials/saving-changes/gitignore  
:: https://docs.github.com/en/github/using-git/ignoring-files  

.gitignore GENERÁTOR  
:: https://www.toptal.com/developers/gitignore  

---

MARKDOWN SYNTAX  
:: https://www.markdownguide.org/basic-syntax  
:: https://daringfireball.net/projects/markdown/syntax   
