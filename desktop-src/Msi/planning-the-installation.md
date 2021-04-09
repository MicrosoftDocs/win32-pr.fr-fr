---
description: Lorsque l’installation d’une application existante est déplacée vers Windows Installer à partir d’une autre technologie d’installation, le développeur du programme d’installation peut commencer à créer un package Windows Installer à l’aide des images fichier source et cible de l’installation existante.
ms.assetid: 8b0fb473-e19f-4427-b2a1-d0721cde9d38
title: Planification de l’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb98368c5c5c8e13a8f9b03a44805a8cff6e517
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866085"
---
# <a name="planning-the-installation"></a>Planification de l’installation

Lorsque l’installation d’une application existante est déplacée vers Windows Installer à partir d’une autre technologie d’installation, le développeur du programme d’installation peut commencer à créer un package Windows Installer à l’aide des images fichier source et cible de l’installation existante. Un plan détaillé de la façon dont les fichiers et autres ressources sont organisés au niveau de la source et de la cible est également un bon point de départ pour le développement d’un package pour une nouvelle application.

L’exemple de package d’installation prend les fichiers suivants qui sont stockés à l’emplacement source de l’application et les installe sur la cible sur l’ordinateur de l’utilisateur.



| Fichier         | Description                               | Chemin de la source                                    | Chemin d’accès à la cible                                          |
|--------------|-------------------------------------------|---------------------------------------------------|---------------------------------------------------------|
| Redpark.exe  | Fichier exécutable de l’éditeur de texte.              | C : \\ exemple de \\ bloc-notes \\Redpark.exe                  | \[\] \\Redpark.exe de \_ parc \\ rouge d’ProgramFilesFolder          |
| Lisezmoi.txt   | Fichier d’information.                    | C : \\ exemple de \\ bloc-notes \\Readme.txt                   | \[\] \\Readme.txt de \_ parc \\ rouge d’ProgramFilesFolder           |
| Help.txt     | Manuel d’aide                               | C : \\ exemple de \\ bloc-notes \\Help.txt                     | Non installé. Toujours exécuter à partir de la source.                  |
| Baseball.txt | Planification de jeu de baseball pour l’année 2000.     | C : \\ exemples d' \\ événements du bloc-notes \\ \\Baseball.txt         | \[\] \\Baseball.txt de \_ \\ sports de sport Red Park \\ |
| Football.txt | Calendrier de jeu de football pour l’année 2000.     | C : \\ exemples d' \\ événements du bloc-notes \\ \\Football.txt         | \[\] \\Football.txt de \_ \\ sports de sport Red Park \\ |
| Dance.txt    | Performances des danses pour l’année 2000.         | C : \\ exemples d' \\ événements du bloc-notes \\ \\Dance.txt            | \[ProgramFilesFolder- \] \\ \_ Arts Red Park \\ Arts \\Dance.txt      |
| Concert.txt  | Performances musicales pour l’année 2000.         | C : \\ exemples d' \\ événements du bloc-notes \\ \\Concert.txt          | \[ProgramFilesFolder- \] \\ \_ Arts Red Park \\ Arts \\Concert.txt    |
| January.txt  | Les admission en janvier de l’année 2000.       | C : \\ exemple \\ de \\ porte Notepad \\January.txt            | \[January.txt de la \] \\ \_ porte Red Park \\ porte \\    |
| NewYears.txt | Les admissions sur le jour des nouveaux années de l’année 2000. | C : \\ exemple de fêtes de la \\ \\ porte Notepad \\ \\NewYears.txt | \[NewYears.txt de la \] \\ \_ porte Red Park \\ porte \\   |



 

L’exemple écrit les valeurs suivantes dans le registre de l’utilisateur sous **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Notepad Sample**.



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
| sHelp     | \[\] \\ Menu de \_ parc Red Park \\\\ | \[\] \\ Exemple de \\ bloc-notes \\Help.txt       |
| sBaseball | \[\] \\ Menu de \_ parc Red Park \\\\ | \[\] \\Baseball.txt de \_ \\ sports de sport Red Park \\ |
| sFootball | \[\] \\ Menu de \_ parc Red Park \\\\ | \[\] \\Football.txt de \_ \\ sports de sport Red Park \\ |
| sDance    | \[\] \\ Menu de \_ parc Red Park \\\\ | \[ProgramFilesFolder- \] \\ \_ Arts Red Park \\ Arts \\Dance.txt      |
| sConcert  | \[\] \\ Menu de \_ parc Red Park \\\\ | \[ProgramFilesFolder- \] \\ \_ Arts Red Park \\ Arts \\Concert.txt    |
| sJanuary  | \[\] \\ Menu de \_ parc Red Park \\\\ | \[January.txt de la \] \\ \_ porte Red Park \\ porte \\    |
| sNewYears | \[\] \\ Menu de \_ parc Red Park \\\\ | \[NewYears.txt de la \] \\ \_ porte Red Park \\ porte \\   |



 

Pour reproduire l’exemple, commencez par créer la structure de répertoire source indiquée dans le premier tableau. Vous pouvez effectuer une copie du fichier Notepad.exe de votre système, puis renommer cette copie Redpark.exe. Utilisez l’éditeur du bloc-notes pour créer les fichiers texte restants. La structure de répertoires de la cible, les valeurs de Registre et les raccourcis sont ajoutés en créant la base de données d’installation.

[Continuer](importing-a-blank-database.md)

 

 



