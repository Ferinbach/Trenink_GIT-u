# Trénink GIT-u

Git / GitHub od základov (yablko)

Spoznávanie a osvojovanie si rôznych funkcií **GIT-u**, 
za účelom jeho pochopeniaa tým pádom jeho správneho používania v rámci vlastných, 
alebo firemných projektov / produktov.
Pričom GIT je celkom zauímavý nástroj- hlavne možnosti a spôsoby jeho využitia, pričom jeho verzii je hneď niekoľko.
Sám som vyskúšal používať  hneď  4  jeho verzie ( 3 terminály z toho 1 vo VS Code )
a potom taktiež vo VS Code vstavané povely, resp. funkcie GIT-u.
Je to len trochu komplikovanejší spôsob ukladania ako  napr. u videohier na konzolách :D

**Celý yablkov SK video-kurz je zadara na [Youtube](https://www.youtube.com/watch?v=0v5K4GvK4Gs&t=939s) ;)**

Toto sú príkazy, ktoré sú podrobné odprezentované 
a vysvetlené v kurze:

---

### Inštalácia:

Pre Windows yablko odporúča [cmder](http://cmder.net/)

Na Mac-Os spustite 1. príkaz cez terminál 
a nemali by ste mať problém s inštaláciou GIT-u 
a ak aj predsa áno, tak použite aj 2. príkaz ;)

```
git --version
xcode-select --install
```

Nastavte si meno a heslo (v prípade, že už používate Github, _tak samozrejme použijete údaje z Vášho GIT-hub účtu_).

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

Následne skontrolujte stav / pozrite či a čo sa zmenilo.

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