---
description: Selon l’application, la localisation peut nécessiter la modification ou l’ajout de ressources telles que des fichiers ou des clés de registre.
ms.assetid: f5af0ecd-cb57-4858-88b4-4608893004f6
title: Ajout de ressources localisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de37bfd3c216018f6c4a6f6866206020576153e55383a9d6b36e67533bbb3b6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829239"
---
# <a name="adding-localized-resources"></a>Ajout de ressources localisées

Selon l’application, la localisation peut nécessiter la modification ou l’ajout de ressources telles que des fichiers ou des clés de registre. La localisation de l’exemple d’application MNP2000 nécessite l’ajout d’un fichier supplémentaire au package, Fre.txt et les versions françaises de deux fichiers existants : Help.txt et Readme.txt.

Dans ce cas, la meilleure pratique consiste à localiser le package de sorte que les versions en anglais et en français puissent coexister en toute sécurité sur l’ordinateur. Cela comprend l’installation de deux fichiers différents avec des noms de fichiers identiques dans le même répertoire. Étant donné que Help.txt et Readme.txt ont des noms de fichiers identiques dans les deux versions linguistiques, le package français doit installer ces fichiers dans un répertoire différent de l’anglais.

Le package français installe Help.txt dans un nouveau sous-répertoire du dossier RedPark, français. Étant donné que l’ajout d' Fre.txt ajoute une ressource au composant d’aide d’origine, le code du composant d’aide doit être différent dans les packages français et anglais. Consultez les règles relatives aux codes de composant dans [modification du code du composant](changing-the-component-code.md).

Le package français installe Readme.txt dans le répertoire français, de sorte que ce nom de fichier ne peut pas entrer en conflit avec la version anglaise. le Readme.txt de fichier est installé avec le composant Bloc-notes, mais les règles de composant ne nécessitent pas la modification du code du composant. dans cet exemple, le code de composant de Bloc-notes ne doit pas être modifié, car RedPark.exe, les valeurs de registre spécifiées dans la [table du registre](registry-table.md), sont partagées par les deux versions de langage. Consultez [Ajout d’informations de Registre](adding-registry-information.md).

Supprimez les versions anglaises de Help.txt et Readme.txt des fichiers sources, puis ajoutez les nouvelles versions françaises de Help.txt, Readme.txt et Fre.txt. Le package localisé doit mapper l’installation des fichiers de la source à la cible comme suit.



| Fichier        | Description                  | Chemin de la source                   | Chemin d’accès à la cible                                         |
|-------------|------------------------------|----------------------------------|--------------------------------------------------------|
| Redpark.exe | Fichier exécutable de l’éditeur de texte. | C : \\ exemple de \\ Bloc-notes \\Redpark.exe | \[ProgramFilesFolder \] \\ Red \_ Park \\ \\Redpark.exe français |
| Lisezmoi.txt  | Fichier d’information.       | C : \\ exemple de \\ Bloc-notes \\Readme.txt  | \[ProgramFilesFolder \] \\ Red \_ Park \\ \\Readme.txt français  |
| Help.txt    | Manuel d’aide                  | C : \\ exemple de \\ Bloc-notes \\Help.txt    | \[ProgramFilesFolder \] \\ Red \_ Park \\ \\Help.txt français    |
| Fre.txt     | liste de Téléphone                   | C : \\ exemple de \\ Bloc-notes \\Fre.txt     | \[ProgramFilesFolder \] \\ Red \_ Park \\ \\Fre.txt français     |



 

Utilisez l’éditeur de base de données Orca fourni avec le kit de développement logiciel (SDK), ou un autre éditeur, pour ouvrir la table de répertoire et ajouter un enregistrement pour l’installation du nouveau répertoire, français.

[Table de répertoire](directory-table.md)



| Répertoire                                        | Répertoire \_ parent                                | DefaultDir        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [**TARGETDIR**](targetdir.md)                   |                                                  | SourceDir         |
| [**ProgramFilesFolder**](programfilesfolder.md) | [**TARGETDIR**](targetdir.md)                   | .                 |
| ARTSDIR                                          | NOTEPADDIR                                       | Arts : événements       |
| HOLDIR                                           | MONDIR                                           | . : Jours fériés        |
| MENUDIR                                          | NOTEPADDIR                                       | Menu              |
| MONDIR                                           | NOTEPADDIR                                       | Porte              |
| NOTEPADDIR                                       | [**ProgramFilesFolder**](programfilesfolder.md) | \_parc rouge : Bloc-notes |
| SPORTDIR                                         | NOTEPADDIR                                       | Sports : événements     |
| FRENCHDIR                                        | NOTEPADDIR                                       | Français:.          |



 

Utilisez votre éditeur de table pour remplacer l’ID de l’élément dans le composant d’aide dans MNPFren.msi par un nouveau GUID.

[Table des composants](component-table.md)



| Composant | ComponentId                            | Répertoire\_ | Attributs | Condition | KeyPath      |
|-----------|----------------------------------------|-------------|------------|-----------|--------------|
| Chaussures  | {F54ABAC0-33F2-11D3-91D7-00C04FD70856} | SPORTDIR    | 2          |           | Baseball.txt |
| Concert   | {76FA7A80-33F6-11D3-91D8-00C04FD70856} | ARTSDIR     | 2          |           | Concert.txt  |
| Jongl     | {CCF834A1-33F8-11D3-91D8-00C04FD70856} | ARTSDIR     | 2          |           | Dance.txt    |
| Terrain  | {CCF834A0-33F8-11D3-91D8-00C04FD70856} | SPORTDIR    | 2          |           | Football.txt |
| Aide      | {9ED21229-FE3C-4FE9-B01D-57E00224FD0B} | NOTEPADDIR  | 2          |           | Help.txt     |
| Janvier   | {CF0BC690-33C9-11D3-91D6-00C04FD70856} | MONDIR      | 2          |           | January.txt  |
| NewYears  | {A42D9140-33D8-11D3-91D6-00C04FD70856} | HOLDIR      | 2          |           | NewYears.txt |
| Bloc-notes   | {19BED232-30AB-11D3-91D3-00C04FD70856} | FRENCHDIR   | 2          |           | Redpark.exe  |



 

Utilisez votre éditeur de table pour ajouter des Fre.txt à la [table de fichiers](file-table.md) de MNPFren.msi. Entrez l’ID de langue pour le français dans le champ langue pour les fichiers localisés. Toutes les autres choses sont égales, si le fichier en cours d’installation a une langue différente de celle du fichier sur l’ordinateur, le programme d’installation privilégie le fichier avec la langue qui correspond au produit en cours d’installation. Les fichiers indépendants de la langue sont traités comme une autre langue, de sorte que le produit en cours d’installation est privilégié. Pour plus d’informations, consultez règles de contrôle de [version de fichier](file-versioning-rules.md).

[Table de fichier](file-table.md)



| Fichier         | Composant\_ | FileName     | FileSize | Version | Langage | Attributs | Séquence |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseball.txt | Chaussures    | Baseball.txt | 1 000     |         |          | 0          | 1        |
| Concert.txt  | Concert     | Concert.txt  | 1 000     |         |          | 0          | 1        |
| Dance.txt    | Jongl       | Dance.txt    | 1 000     |         |          | 0          | 1        |
| Football.txt | Terrain    | Football.txt | 1 000     |         |          | 0          | 1        |
| Help.txt     | Aide        | Help.txt     | 1 000     |         | 1036     | 0          | 1        |
| January.txt  | Janvier     | January.txt  | 1 000     |         |          | 0          | 1        |
| NewYears.txt | NewYears    | NewYears.txt | 1 000     |         |          | 0          | 1        |
| Redpark.exe  | Bloc-notes     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Lisezmoi.txt   | Bloc-notes     | Lisezmoi.txt   | 1 000     |         | 1036     | 0          | 1        |
| Fre.txt      | Aide        | Fre.txt      | 1 000     |         | 1036     | 0          | 1        |



 

Cela termine l’exemple de localisation.

 

 



