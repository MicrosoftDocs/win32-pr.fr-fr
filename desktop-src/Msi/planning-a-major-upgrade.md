---
description: si Windows Installer est utilisé pour l’installation et la configuration d’une application, les mises à niveau ultérieures de cette application peuvent être gérées par l’installation d’un package de mise à niveau.
ms.assetid: 69ad4928-e750-47c2-8668-c9e3deff8066
title: Planification d’une mise à niveau majeure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07ece8acf0dbc37ecdfddaa3505e5e54a283a8e8efd7b4eb0dc1a0a365a461e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118377370"
---
# <a name="planning-a-major-upgrade"></a>Planification d’une mise à niveau majeure

si Windows Installer est utilisé pour l’installation et la configuration d’une application, les mises à niveau ultérieures de cette application peuvent être gérées par l’installation d’un package de mise à niveau. Les développeurs du programme d’installation peuvent choisir de créer un package de mise à niveau en modifiant le package d’installation d’origine. Cette approche est illustrée par l’exemple de mise à niveau suivant.

L’installation du produit d’origine, MNP2000, suivie de l’installation du package de mise à niveau, fournit à l’utilisateur les fichiers suivants requis par le produit MNP2001.



| Fichier          | Description                                                    | Chemin de la source                                    | Chemin d’accès à la cible                                          |
|---------------|----------------------------------------------------------------|---------------------------------------------------|---------------------------------------------------------|
| Redpark.exe   | Fichier exécutable de l’éditeur de texte. Non modifié par rapport aux produits précédents. | C : \\ exemple de \\ Bloc-notes \\Redpark.exe                  | \[\] \\Redpark.exe de \_ parc \\ rouge d’ProgramFilesFolder          |
| Lisezmoi.txt    | Fichier d’informations. Non modifié par rapport aux produits précédents.         | C : \\ exemple de \\ Bloc-notes \\Readme.txt                   | \[\] \\Readme.txt de \_ parc \\ rouge d’ProgramFilesFolder           |
| Help.txt      | Manuel d’aide. Non modifié par rapport aux produits précédents.                 | C : \\ exemple de \\ Bloc-notes \\Help.txt                     | Non installé. Toujours exécuter à partir de la source.                  |
| Baseba01.txt  | Planification de jeu de baseball pour l’année 2001.                          | C : \\ exemple \\ d' \\ événements de Bloc-notes \\Baseba01.txt         | \[\] \\Baseball.txt de \_ \\ sports de sport Red Park \\ |
| Footba01.txt  | Calendrier de jeu de football pour l’année 2001.                          | C : \\ exemple \\ d' \\ événements de Bloc-notes \\Footba01.txt         | \[\] \\Football.txt de \_ \\ sports de sport Red Park \\ |
| Basket01.txt  | Programme de jeu de basket pour l’année 2001.                        | C : \\ exemple \\ d' \\ événements de Bloc-notes \\Basket01.txt         | \[\] \\Basket01.txt de \_ \\ sports de sport Red Park \\ |
| Dance01.txt   | Performances des danses pour l’année 2001.                              | C : \\ exemple \\ d' \\ événements de Bloc-notes \\Dance01.txt          | \[ProgramFilesFolder- \] \\ \_ Arts Red Park \\ Arts \\Dance.txt      |
| Concert01.txt | Musique les performances de l’année 2001.                              | C : \\ exemple \\ d' \\ événements de Bloc-notes \\Concer01.txt         | \[ProgramFilesFolder- \] \\ \_ Arts Red Park \\ Arts \\Concert.txt    |
| Opera01.txt   | Performances Opera pour l’année 2001.                              | C : \\ exemple \\ d' \\ événements de Bloc-notes \\Opera01.txt          | \[ProgramFilesFolder- \] \\ \_ Arts Red Park \\ Arts \\Opera01.txt    |
| Januar01.txt  | Les admission en janvier de l’année 2001.                            | C : \\ exemple \\ de \\ porte de Bloc-notes \\Januar01.txt           | \[January.txt de la \] \\ \_ porte Red Park \\ porte \\    |
| NewYea01.txt  | Les admissions sur le jour des nouveaux années de l’année 2001.                      | C : \\ exemple de fêtes de Bloc-notes de la \\ \\ porte \\ \\NewYea01.txt | \[NewYears.txt de la \] \\ \_ porte Red Park \\ porte \\   |
| Memori01.txt  | Les admissions sur le jour du souvenir de l’année 2001.                       | C : \\ exemple de fêtes de Bloc-notes de la \\ \\ porte \\ \\Memori01.txt | \[Memori01.txt de la \] \\ \_ porte Red Park \\ porte \\   |



 

L’installation du package de mise à niveau supprime toutes les fonctionnalités installées avec le produit d’origine qui ne sont pas utilisées par le produit mis à niveau.

Par exemple, lors de la mise à niveau à partir de MNP2000, l’installation de la mise à niveau supprime les fichiers suivants de l’ordinateur de l’utilisateur :

-   Baseball.txt
-   Football.txt
-   Dance.txt
-   Concert.txt
-   January.txt
-   NewYears.txt

L’installation du package de mise à niveau écrit les valeurs suivantes dans le registre de l’utilisateur sous :

**HKEY \_ exemple \_** de logiciel d’ordinateur LOCAL \\  \\ **Microsoft** \\ **Bloc-notes**



| Nom             | Valeur    |
|------------------|----------|
| lfCharSet        | 0        |
| lfClipPrecision  | 2        |
| lfFaceName       | FixedSys |
| lfItalic         | 0        |
| lfOrientation    | 0        |
| lfOutPrecision   | 1        |
| fSavePageSetting | 0        |
| lfPitchAndFamily | 49       |
| iPointSize       | 120      |
| lfQuality        | 2        |
| lfStrikeOut      | 0        |
| lfWeight         | 400      |
| fWrap            | 0        |



 

La mise à niveau met à jour les anciens raccourcis vers les raccourcis suivants. L’un de ces raccourcis peut être sélectionné lors de l’installation en tant que raccourci publié afin que l’utilisateur puisse installer à la demande la fonctionnalité de baseball.



| Nom        | Emplacement du raccourci                         | Cible de raccourci                                           |
|-------------|-------------------------------------------|-----------------------------------------------------------|
| sNotepad    | \[\] \\ Menu de \_ parc Red Park \\\\ | \[\] \\Redpark.exe de \_ parc \\ rouge d’ProgramFilesFolder            |
| sReadme     | \[\] \\ Menu de \_ parc Red Park \\\\ | \[\] \\Readme.txt de \_ parc \\ rouge d’ProgramFilesFolder             |
| sHelp       | \[\] \\ Menu de \_ parc Red Park \\\\ | \[Bloc-notes de l' \] \\ exemple ProgramFilesFolder \\ \\Help.txt         |
| sBaseball   | \[\] \\ Menu de \_ parc Red Park \\\\ | \[\] \\Baseba01.txt de \_ \\ sports de sport Red Park \\   |
| sFootball   | \[\] \\ Menu de \_ parc Red Park \\\\ | \[\] \\Footba01.txt de \_ \\ sports de sport Red Park \\   |
| sBasketball | \[\] \\ Menu de \_ parc Red Park \\\\ | \[\] \\Basketba01.txt de \_ \\ sports de sport Red Park \\ |
| sDance      | \[\] \\ Menu de \_ parc Red Park \\\\ | \[ProgramFilesFolder- \] \\ \_ Arts Red Park \\ Arts \\Dance01.txt      |
| sConcert    | \[\] \\ Menu de \_ parc Red Park \\\\ | \[ProgramFilesFolder- \] \\ \_ Arts Red Park \\ Arts \\Concer01.txt     |
| sOpera      | \[\] \\ Menu de \_ parc Red Park \\\\ | \[ProgramFilesFolder- \] \\ \_ Arts Red Park \\ Arts \\Opera01.txt      |
| sJanuary    | \[\] \\ Menu de \_ parc Red Park \\\\ | \[Januar01.txt de la \] \\ \_ porte Red Park \\ porte \\     |
| sNewYears   | \[\] \\ Menu de \_ parc Red Park \\\\ | \[NewYea01.txt de la \] \\ \_ porte Red Park \\ porte \\     |
| sMemorial   | \[\] \\ Menu de \_ parc Red Park \\\\ | \[Memori01.txt de la \] \\ \_ porte Red Park \\ porte \\     |



 

lorsqu’un utilisateur désinstalle le package de mise à niveau, Windows Installer supprime complètement toutes les versions du produit de l’ordinateur de l’utilisateur. L’utilisateur n’a pas de partie de MNP2000 ou MNP2001.

[Continuer](importing-original-installation-database.md)

 

 



