# Annonces sonores sur les SAE français

Sur ce wiki, vous trouverez toutes les informations nécessaires afin de rajouter les annonces sonores lorsqu'une porte est ouverte avec les SAE français, c'est-à-dire l'INEO et Businfo.

## Table des matières

- [1. Mise en place des annonces](#1-mise-en-place-des-annonces)
- [2. Installation - Businfo Saint-Servan](#2-installation---businfo-saint-servan)
- [3. Installation - Autres SAE français](#3-installation---autres-sae-français)
- [4. Remerciement](#4-remerciement)
- [5. Besoin d'aide?](#5-besoin-daide)

# 1. Mise en place des annonces
Avant de modifier les scripts afin d'avoir une annonce sonore lorsqu'on ouvre les portes, il faut rendre compatible les fichiers sonores.
1. Tout d'abord aller dans le dossier où se trouvent les annonces vocales de la map `Announcements\..` ou Enregistrez une annonce dans le dossier "Announcements" de la map/.hof
2. Renommez ou nommez le fichier sonore de cette manière `Numéro de ligne_Nom du terminus_#target` et faites une copie en remplaçant `_#target` en `_#ext`, `Numéro de ligne_Nom du terminus_#ext`

Le "Nom du terminus" a un format spécial, le nom du terminus doit avoir des espaces autour du nom qui sont définits dans le fichier .hof. Il y a 2 méthodes pour y procéder.

### Méthode 1
1. Ouvrez le fichier .hof dans un éditeur de texte (Exemple : Bloc note, Notepad, mais le plus conseillé est Visual Studio Code car il visualise mieux les TAB et espaces)
2. Descendez vers `[addterminus_list]`
3. Trouvez le terminus associé à l'annonce
4. Normalement vous trouvez ceci `Num. Ligne  Arrêt  ARRÊT`, occupez vous uniquement du 2e nom d'arrêt qui est généralement en majuscule. Par ailleurs il correspond au "Nom du terminus" à mettre dans le nom du fichier.

> i. Lorsque vous allez sélectionner autour du nom de l'arrêt, vous allez avoir 2 types d'espaces
> - Le TAB - espace long : ![Sélection TAB dans le Bloc-notes](https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/TAB_bn.gif) ![Sélection TAB dans Visual Studio Code](https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/TAB_VSCode.gif)
> - L'espace - espace court, le commun : ![Sélection espace dans le Bloc-Notes](https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/Space_Bn.gif) ![Sélection espace dans Visual Studio Code](https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/Space_VSCode.gif)
> Nous allons uniquement nous intéresser aux espaces simples

> i2. Sur Visual Studio Code les TAB sont matérialisés par une flèche, et les espaces par des points centrés.

> Astuce : La sélection entre les espaces et TABS n'ont pas la même sensiblité.

5. A gauche de la première lettre de l'arrêt en majusucle maintenez et glissez votre souris jusqu'à ce que vous buttez sur un TAB tout en comptant le nombre d'espaces simples. Faites de même à droite. Par ailleurs certains hof ont uniquement un TAB à gauche entre l'arrêt sans majuscule et avec majusucle, il y a donc aucun espace.
6. Reportez le nombre d'espace à gauche et à droite que vous avez comptez à mettre dans le nom du fichier.

Exemple, l'arrêt "Clémenceau" a pour nom dans le .hof `279	Clemenceau	CLEMENCEAU      	`, nous allons prendre le CLEMENCEAU qui se situe à la droite du nom de l'arrêt qui suit le numéro de ligne, à gauche de CLEMENCEAU se situe un TAB, donc non comptabilisé pour le nom du fichier final, puis 6 espaces et un TAB à droite de CLEMENCEAU, nous allons donc mettre 6 espaces à droite de CLEMENCEAU dans le fichier final. Ainsi, les fichiers `78_CLEMENCEAU      _#ext.wav` et `78_CLEMENCEAU      _#target.wav` sont les mêmes fichiers avec la même annonce, mais seule la fin change pour les rendre compatibles avec les SAE ; et le numéro de ligne correspond au numéro de ligne présent sur la fiche de service.

### Méthode 2
1. Lancez un service sur OMSI
2. Ouvrez le logfile
3. Repérez la ligne où OMSI indique qu'il manque un fichier sonore terminant soit par `_#target.wav` ou `_#ext.wav` - Exemple : `Warning:       Soundfile vehicles\M-M_GX337G_RATP\sound\..\..\Announcements\ParisGo\78_CLEMENCEAU      _#target.wav does not exist!`
4. Copiez le nom du fichier indiqué par OMSI sur le fichier sonore dans le dossier

De plus, "Numéro de ligne" correspond au numéro de ligne à taper sur l'ibis. ![Ligne à prendre pour le nom de fichier](https://github.com/AgoProjects/agoprojects-omsi2/blob/main/images/Ligne.png)

Ainsi, vous devez avoir 2 mêmes fichiers sonores, un qui finit par `_#target` et un autre par `_#ext`.

# 2. Installation - Businfo Saint-Servan
1. Tout d'abord, munissez-vous du nom du dossier "Announcements" associé au fichier .hof, trouvable soit dans le dossier qui se situe "Announcements", soit le nom du dossier "Announcements" dans le fichier .hof trouvable sur HOF Suite ou sous le chiffre dans le [global-strings]
2. Rendez-vous dans le dossier script d'un des bus du DLC Saint-Servan
3. Allez dans `..\Scripts\Businfo` et ouvrez le fichier `Businfo.osc`
4. Faites `CTRL + F` et tapez `#target`
5. Lorsque vous trouvez ce code
   ```            
        0 (M.V.GetDepotStringGlobal) "St-Servan" $=
        {if}

            l0 (L.$.Businfo_TTLineString) $+ "_" $+
            (M.V.GetTTTerminusIndex) 0 (M.V.GetTerminusString) $+
            "_#target" $+ s0

        {endif}
        {endif}
        {endif}

    {endif}
   ```
6. Copiez la partie `0 (M.V.GetDepotStringGlobal) "St-Servan" $=` et collez-là en faisant un retour à la ligne, puis ajoutez `||`. Remplacez également le nom du dépôt qui se trouvent entre les guillemets par le nom du dossier "Announcements" que vous avez trouvé à l'étape 1. Par exemple :
    ```            
        0 (M.V.GetDepotStringGlobal) "St-Servan" $= 
        0 (M.V.GetDepotStringGlobal) "Grundorf" $= ||
        0 (M.V.GetDepotStringGlobal) "Horizon16" $= ||
        {if}

            l0 (L.$.Businfo_TTLineString) $+ "_" $+
            (M.V.GetTTTerminusIndex) 0 (M.V.GetTerminusString) $+
            "_#ext" $+ s0

        {endif}
        {endif}
        {endif}

    {endif}
    ```
7. Sauvegardez le fichier

# 3. Installation - Autres SAE français
1. Tout d'abord, munissez-vous du nom du dossier "Announcements" associé au fichier .hof, trouvable soit dans le dossier "Announcements", soit le nom du dossier "Announcements" dans le fichier .hof trouvable sur HOF Suite ou sous le chiffre dans le [global-strings]
2. Rendez-vous dans le dossier script d'un des bus contenant un SAE et cherchez le .osc du SAE
3. Ouvrez le fichier .osc
4. Faites `CTRL + F` et tapez `#ext` ou `#target`
5. Lorsque vous trouvez ce code
   ```            
        0 (M.V.GetDepotStringGlobal) "St-Servan" $=
        {if}

            l0 (L.$.Businfo_TTLineString) $+ "_" $+
            (M.V.GetTTTerminusIndex) 0 (M.V.GetTerminusString) $+
            "_#ext" $+ s0

        {endif}
        {endif}
        {endif}

    {endif}
   ```
6. Copiez la partie `0 (M.V.GetDepotStringGlobal) "St-Servan" $=` et collez-là en faisant un retour à la ligne, puis ajoutez `||`. Remplacez également le nom du dépôt qui se trouvent entre les guillemets par le nom du dossier "Announcements" que vous avez trouvé à l'étape 1. Par exemple :
    ```            
        0 (M.V.GetDepotStringGlobal) "St-Servan" $= 
        0 (M.V.GetDepotStringGlobal) "Grundorf" $= ||
        0 (M.V.GetDepotStringGlobal) "Horizon16" $= ||
        {if}

            l0 (L.$.Businfo_TTLineString) $+ "_" $+
            (M.V.GetTTTerminusIndex) 0 (M.V.GetTerminusString) $+
            "_#ext" $+ s0

        {endif}
        {endif}
        {endif}

    {endif}
    ```
7. Sauvegardez le fichier

Par ailleurs si dans le fichier .osc le code est en `_#target` ou `_#ext` ne changez pas le code.

> i. Les extraits de code sont à titre d'exemple.

# 4. Remerciement
Merci Fourkane pour les explications des scripts.

# 5. Besoin d'aide?
Si vous avez besoin d'une aide, vous pouvez nous contacter sur les réseaux (Instagram, Twitter/X) trouvables sur [Ici !](https://github.com/AgoProjects/agoprojects-omsi2) ou sur Discord.