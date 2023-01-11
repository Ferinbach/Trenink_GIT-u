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

Pre Windows yablko odporúča [cmder](http://cmder.net/)

Na Mac-Os spustite 1. príkaz cez terminál 
a nemali by ste mať problém s inštaláciou GIT-u 
a ak aj predsa, tak použite aj 2. príkaz ;)

```
git --version
xcode-select --install
```

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