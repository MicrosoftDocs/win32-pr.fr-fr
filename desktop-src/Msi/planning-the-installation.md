---
description: lorsque l’installation d’une application existante est déplacée vers Windows Installer à partir d’une autre technologie d’installation, le développeur du programme d’installation peut commencer à créer un package Windows Installer à l’aide des images fichier source et cible de l’installation existante.
ms.assetid: 8b0fb473-e19f-4427-b2a1-d0721cde9d38
title: Planification de l’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d406ec97fd5edb34468586eb9f707eff32b289df3dc88b803b8c55d4aad10cd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042359"
---
# <a name="planning-the-installation"></a>Planification de l’installation

lorsque l’installation d’une application existante est déplacée vers Windows Installer à partir d’une autre technologie d’installation, le développeur du programme d’installation peut commencer à créer un package Windows Installer à l’aide des images fichier source et cible de l’installation existante. Un plan détaillé de la façon dont les fichiers et autres ressources sont organisés au niveau de la source et de la cible est également un bon point de départ pour le développement d’un package pour une nouvelle application.

L’exemple de package d’installation prend les fichiers suivants qui sont stockés à l’emplacement source de l’application et les installe sur la cible sur l’ordinateur de l’utilisateur.



| Fichier         | Description                               | Chemin de la source                                    | Chemin d’accès à la cible                                          |
|--------------|-------------------------------------------|---------------------------------------------------|---------------------------------------------------------|
| Redpark.exe  | Fichier exécutable de l’éditeur de texte.              | C : \\ exemple de \\ Bloc-notes \\Redpark.exe                  | \[\] \\Redpark.exe de \_ parc \\ rouge d’ProgramFilesFolder          |
| Lisezmoi.txt   | Fichier d’information.                    | C : \\ exemple de \\ Bloc-notes \\Readme.txt                   | \[\] \\Readme.txt de \_ parc \\ rouge d’ProgramFilesFolder           |
| Help.txt     | Manuel d’aide                               | C : \\ exemple de \\ Bloc-notes \\Help.txt                     | Non installé. Toujours exécuter à partir de la source.                  |
| Baseball.txt | Planification de jeu de baseball pour l’année 2000.     | C : \\ exemple \\ d' \\ événements de Bloc-notes \\Baseball.txt         | \[\] \\Baseball.txt de \_ \\ sports de sport Red Park \\ |
| Football.txt | Calendrier de jeu de football pour l’année 2000.     | C : \\ exemple \\ d' \\ événements de Bloc-notes \\Football.txt         | \[\] \\Football.txt de \_ \\ sports de sport Red Park \\ |
| Dance.txt    | Performances des danses pour l’année 2000.         | C : \\ exemple \\ d' \\ événements de Bloc-notes \\Dance.txt            | \[ProgramFilesFolder- \] \\ \_ Arts Red Park \\ Arts \\Dance.txt      |
| Concert.txt  | Musique les performances de l’année 2000.         | C : \\ exemple \\ d' \\ événements de Bloc-notes \\Concert.txt          | \[ProgramFilesFolder- \] \\ \_ Arts Red Park \\ Arts \\Concert.txt    |
| January.txt  | Les admission en janvier de l’année 2000.       | C : \\ exemple \\ de \\ porte de Bloc-notes \\January.txt            | \[January.txt de la \] \\ \_ porte Red Park \\ porte \\    |
| NewYears.txt | Les admissions sur le jour des nouveaux années de l’année 2000. | C : \\ exemple de fêtes de Bloc-notes de la \\ \\ porte \\ \\NewYears.txt | \[NewYears.txt de la \] \\ \_ porte Red Park \\ porte \\   |



 

l’exemple écrit les valeurs suivantes dans le registre de l’utilisateur sous **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Bloc-notes sample**.



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



 

L’exemple installe les raccourcis suivants. L’un de ces raccourcis peut être sélectionné lors de l’installation en tant que raccourci publié afin que l’utilisateur puisse installer à la demande la fonctionnalité de baseball.



| Nom      | Emplacement du raccourci                         | Cible de raccourci                                         |
|-----------|-------------------------------------------|---------------------------------------------------------|
| sNotepad  | \[\] \\ Menu de \_ parc Red Park \\\\ | \[\] \\Redpark.exe de \_ parc \\ rouge d’ProgramFilesFolder          |
| sReadme   | \[\] \\ Menu de \_ parc Red Park \\\\ | \[\] \\Readme.txt de \_ parc \\ rouge d’ProgramFilesFolder           |
| sHelp     | \[\] \\ Menu de \_ parc Red Park \\\\ | \[Bloc-notes de l' \] \\ exemple ProgramFilesFolder \\ \\Help.txt       |
| sBaseball | \[\] \\ Menu de \_ parc Red Park \\\\ | \[\] \\Baseball.txt de \_ \\ sports de sport Red Park \\ |
| sFootball | \[\] \\ Menu de \_ parc Red Park \\\\ | \[\] \\Football.txt de \_ \\ sports de sport Red Park \\ |
| sDance    | \[\] \\ Menu de \_ parc Red Park \\\\ | \[ProgramFilesFolder- \] \\ \_ Arts Red Park \\ Arts \\Dance.txt      |
| sConcert  | \[\] \\ Menu de \_ parc Red Park \\\\ | \[ProgramFilesFolder- \] \\ \_ Arts Red Park \\ Arts \\Concert.txt    |
| sJanuary  | \[\] \\ Menu de \_ parc Red Park \\\\ | \[January.txt de la \] \\ \_ porte Red Park \\ porte \\    |
| sNewYears | \[\] \\ Menu de \_ parc Red Park \\\\ | \[NewYears.txt de la \] \\ \_ porte Red Park \\ porte \\   |



 

Pour reproduire l’exemple, commencez par créer la structure de répertoire source indiquée dans le premier tableau. Vous pouvez effectuer une copie du fichier Notepad.exe de votre système, puis renommer cette copie Redpark.exe. utilisez l’éditeur de Bloc-notes pour créer les fichiers texte restants. La structure de répertoires de la cible, les valeurs de Registre et les raccourcis sont ajoutés en créant la base de données d’installation.

[Continuer](importing-a-blank-database.md)

 

 



