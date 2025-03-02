# Mercedes-Benz Citaro C2G Diesel - Palme d'Or

Sur ce document, vous trouverez toutes les informations nécessaires pour le bon fonctionnement du mod.

## Table des matières

- [Mercedes-Benz Citaro C2G Diesel - Palme d'Or](#mercedes-benz-citaro-c2g-diesel---palme-dor)
  - [Table des matières](#table-des-matières)
- [1. Introduction](#1-introduction)
  - [Les nouveautés sur le véhicule](#les-nouveautés-sur-le-véhicule)
- [2. Installation](#2-installation)
- [3. Setvars](#3-setvars)
    - [Ailes avant sur le toit](#ailes-avant-sur-le-toit)
    - [Pubs](#pubs)
    - [Vignette assurance](#vignette-assurance)
    - [Logos](#logos)
- [4. Crédits](#4-crédits)
- [5. Changelog](#5-changelog)

# 1. Introduction
Dans ce mod, vous pouvez conduire la version diesel du Mercedes-Benz Citaro C2G €6 du DLC Saint-Servan avec plusieurs nouveaux éléments à bord du véhicule, dont une augmentation de la capacité à bord et la montée par "toutes les portes". 

À cause de notre limitation à modifier les scripts du véhicule, les passagers vont principalement monter par la 1re et 2e porte, il sera rare de les voir monter par les portes de derrière. De plus, le DEV de la porte 4 ne marche pas. Par ailleurs, lorsque les passagers montent et que le DEV est activé pour la descente des passagers, la porte se refermera même si les passagers montent.

Les templates sont dans le dossier "Addons/AgoProjects - Mercedes-Benz Citaro C2G Palme dOr".

Une version IA du C2G n'est pas prévu à cause de différents bugs rencontrés.

## Les nouveautés sur le véhicule
Suppression des feux de gabarits à l'avant, ils sont sur les clignotants avant :
![](https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/OLLt470eqG.png?raw=true=1280x)

Ajout du boîtier du répéteur de l'arrêt demandé "RAD.V3.P.RB" de Vignal :
![](https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/image%2031.png?raw=true=1280x)

Ajout de boutons "Arrêt demandé" pour les places prioritaire et PMR de la marque Mafelec, dont des pictogrammes : 
![](https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/image%2034.png?raw=true=1280x)

Ajout de boutons "Self service" sur les portes :
![](https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/image%2030.png?raw=true=1280x)

Ajout de plusieurs autres éléments :
| | |
| :--------: | :--------: |
| <img width="70%" height="50%" src="https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/image%2033.png?raw=true">     | <img width="70%" height="50%" src="https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/image%2032.png?raw=true">     |

# 2. Installation
Décompresser l'archive dans votre dossier "OMSI 2".

Puis lors de la sélection du véhicule, dans le fabricant sélectionner "AgoProjects - Saint-Servan" puis le véhicule "C2G".

# 3. Setvars
Voici un tableau récapitulatif des setvars présents sur le véhicule.

> Les photos servent uniquement d'illustration, d'où le fait que certains éléments sont différents.

### Ailes avant sur le toit

```
[setvar]
svr_ailes
0
```

| 0 - Par défaut | 1 - Activé |
| :--------: | :--------: |
| <img width="70%" height="50%" src="https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/image%2019.png?raw=true">     | <img width="70%" height="50%" src="https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/image%2020.png?raw=true">     |

### Pubs

Seulement pour les setvars `vis_cadres_pubs_avant_gauche`, `vis_cadres_pubs_avant_droite` et `vis_cadres_pubs_avant_droite`

```
[setvar]
vis_cadres_pubs_avant_gauche
0

[setvar]
vis_cadres_pubs_avant_droite
0

[setvar]
vis_cadres_pubs_arriere_gauche
0
```
| 0 - Par défaut | 1 - Cadre | 2 - Cadre + pub |
| :--------: | :--------: | :--------: |
| <img width="70%" height="50%" src="https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/image%2021.png?raw=true">     | <img width="70%" height="50%" src="https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/image%2022.png?raw=true">     | <img width="70%" height="50%" src="https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/image%2023.png?raw=true">     |

Seulement pour le setvar `vis_cadres_pubs_arriere`

```
[setvar]
vis_cadres_pubs_arriere
0
```
| 0 - Par défaut | 1 - Cadre (petit) | 2 - Cadre | 3 - Cadre + pub |
| :--------: | :--------: | :--------: | :--------: |
| <img width="70%" height="50%" src="https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/image%2024.png?raw=true">     | <img width="70%" height="50%" src="https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/image%2025.png?raw=true">     | <img width="70%" height="50%" src="https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/image%2026.png?raw=true">     | <img width="70%" height="50%" src="https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/image%2027.png?raw=true">     |

### Vignette assurance

```
[setvar]
vis_vignette_assurance
0
```
| 0 - Par défaut | 1 - Activé |
| :--------: | :--------: |
| <img width="70%" height="50%" src="https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/image%2017.png?raw=true">     | <img width="70%" height="50%" src="https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/image%2018.png?raw=true">     |


### Témoins de serrage

```
[setvar]
svr_temoins_serrage_avant
0

[setvar]
svr_temoins_serrage_milieu
0

[setvar]
svr_temoins_serrage_arriere
0
```

| 0 - Par défaut | 1 - Activé |
| :--------: | :--------: |
| <img width="70%" height="50%" src="https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/i4URSY6gvL.png?raw=true">     | <img width="70%" height="50%" src="https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/Y5no8K0KJf.png?raw=true">     |

### Enjoliveurs
Pour ce setvar, il est conseillé d'enlever les témoins de serrage.
```
[setvar]
svr_enjoliveurs_avant
0

[setvar]
svr_enjoliveurs_milieu
1

[setvar]
svr_enjoliveurs_arriere
0
```

| 0 - Par défaut | 1 - Activé |
| :--------: | :--------: |
| <img width="70%" height="50%" src="https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/i4URSY6gvL.png?raw=true">     | <img width="70%" height="50%" src="https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/MeqU8vzRTF.png?raw=true">     |

> Il est possible que dans une prochaine version, les setvars ci-dessous changent.

### Logos

Logo bluetec
```
[setvar]
svr_logo_bluetec
0
```
| 0 - Par défaut | 1 - Activé |
| :--------: | :--------: |
| <img width="70%" height="50%" src="https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/image%2015.png?raw=true">     | <img width="70%" height="50%" src="https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/image%2016.png?raw=true">     |

Emblême Mercedes-Benz
```
[setvar]
svr_logo_embleme
0
```
| 0 - Par défaut | 1 - Activé |
| :--------: | :--------: |
| <img width="70%" height="50%" src="https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/image%2013.png?raw=true">     | <img width="70%" height="50%" src="https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/image%2014.png?raw=true">     |

Étoile Mercedes-Benz à l'arrière
```
[setvar]
svr_logo_etoile_arriere
0
```
| 0 - Par défaut | 1 - Activé |
| :--------: | :--------: |
| <img width="70%" height="50%" src="https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/image%2028.png?raw=true">     | <img width="70%" height="50%" src="https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/C2GPDO/image%2029.png?raw=true">     |

# 4. Crédits
- Modèles 3D : DLC Saint-Servan, Showtc
- Scripts (Passagers, portes) : Klarky, TheFmrr
- Textures : DLC Saint-Servan, Showtc
- Repaints : Klarky
- Bêta test : Groupe Ago'Projects

Merci à QB, Jihem et Nerosy pour les autorisations et différentes aides.
Merci @zenon_zz, et @deleteduser39530a65 d'avoir remonté des bugs.

# 5. Changelog

16/11/2024 - 1.01 : 
```diff
+ Ajout des fichiers manquants
- Suppression d'un objet présent dans le cfg provenant d'un autre véhicule
```

14/11/2024 - 1.1 : 
```diff
+ Modification du logo Mercedes-Benz (l'étoile)
+ Ajout des enjoliveurs
+ Ajout de setvars pour les témoins de serrage
```

13/10/2024 - 1.0 :
```diff
+ Sortie initiale
```

> Ago'Projects - Mercedes-Benz Citaro C2G Diesel - Palme d'Or