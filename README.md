# INF1070ETE2024-LAB7

# Preparation 

On cree une  variable locale ! 

```sh 
dict="/usr/share/dict/french"
```
# 1 : francais

1) 
```sh 
grep titi $dict
compétitif
compétitifs
compétition
compétitions
compétitive
compétitives
compétitivité
...
```

2) 
```sh
grep ren.ren $dict
égrenèrent
rengrener
rentrent
```

3) 
```sh
grep k.*w $dict
kilowatt
kilowatts
kiwi
kiwis
knock-down
kwas
talkies-walkies
talkie-walkie
```

4) 
```sh 
grep -e k.*w -e w.*k $dict
kilowatt
kilowatts
kiwi
kiwis
knock-down
kwas
patchwork
patchworks
...
```

5) 
```sh
grep latif$ $dict
ablatif
contemplatif
corrélatif
législatif
récapitulatif
relatif
spéculatif
superlatif
```

6)

```sh
grep ^dé.*dé$ $dict
débandé
débordé
décédé
décidé
décodé
...
```

7)
```sh
grep ^.......ent$ $dict
abattaient
abattement
abattirent
abolissent
abondaient
...
```

```sh
grep "^.\{7\}ent$" $dict
abattaient
abattement
abattirent
abolissent
abondaient
```

8) 
```sh
grep "^[^st]*st$" $dict
ballast
check-list
christ
compost
...
```

9)
```sh
grep ".*-.*-.*-.*" $dict
je-ne-sais-quoi
qu'en-dira-t-on
```

10) 
```sh
grep "[[=e=]]t\+[[=e=]]t\+[[=e=]]" $dict
étêtement
étêtements
étêter
...
```

11) 
```sh
grep -o ".$" $dict | sort | uniq -c | sort -n | tail -1
50571 s
```

12) 
```sh 
grep -o "..$" $dict | grep -o "^." | sort | uniq -c | sort -n | tail -1
  38068 n
```

explication : premier grep donne les deux dernières lettres, le deuxième extrait la première parmis les 2 dernières. Le reste est similaire à la commande précédente. !

# Exercice 2 : 

La correction est déjà sur le site ! 

# Exercice 3 : 


Dans le man ! 
```sh
/--[a-z]+-[a-z]+=[A-Z]+
```
