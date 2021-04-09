---
description: Le Windows Installer installe et supprime les blocs de ressources référencés en tant que composants Windows Installer. Pour plus d’informations, consultez groupe de tables principales et composants et fonctionnalités.
ms.assetid: e51dffed-d1cb-4a12-8615-0c0f612f993b
title: Spécification des composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98cb254498236b85ab5c2bc0df3bd32892227b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862910"
---
# <a name="specifying-components"></a>Spécification des composants

Le Windows Installer installe et supprime les blocs de ressources référencés en tant que [composants Windows Installer](windows-installer-components.md). Pour plus d’informations, consultez [groupe de tables principales](core-tables-group.md) et [composants et fonctionnalités](components-and-features.md).

Dans cette section, vous allez ajouter des informations sur les composants utilisés par l’exemple du bloc-notes à la [table des composants](component-table.md) que vous avez créée lors de l' [importation d’une base de données vide](importing-a-blank-database.md). Pour plus d’informations, consultez [Organisation des applications dans des composants](organizing-applications-into-components.md) et définition des composants du programme d' [installation](defining-installer-components.md).

L’exemple Notepad utilise huit composants pour contrôler les ressources.



| Composant | Ressources                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| Chaussures  | Baseball.txt, sBaseball                                                                                               |
| Concert   | Concert.txt, sConcert                                                                                                 |
| Jongl     | Dance.txt, sDance                                                                                                     |
| Terrain  | Football.txt, sFootball                                                                                               |
| Aide      | Help.txt, sHelp                                                                                                       |
| Janvier   | January.txt, sJanuary                                                                                                 |
| NewYears  | NewYears.txt, sNewYears                                                                                               |
| Bloc-notes   | Redpark.exe, Readme.txt, sReadme, sNotepad, **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **Notepad Sample** |



 

Chaque composant doit être identifié avec un [GUID](guid.md)d’ID de composant unique. Si vous reproduisez l’exemple, ne réutilisez pas les mêmes GUID d’ID de composant dans le tableau suivant. Utilisez plutôt un utilitaire tel que Guidgen.exe pour générer de nouveaux GUID pour vos composants.

Veillez à utiliser une chaîne GUID cohérente avec le type de données GUID Windows Installer. Pour plus d’informations, consultez [modification du code du composant](changing-the-component-code.md) et [que se passe-t-il si les règles des composants sont rompues ?](what-happens-if-the-component-rules-are-broken.md)

Utilisez Orca ou un autre éditeur de base de données pour entrer les données suivantes dans la [table des composants](component-table.md) vide de MNP2000.msi. Ne réutilisez pas les GUID indiqués ci-dessous dans la colonne ComponentId de votre exemple.



| Composant | ComponentId                            | Répertoire\_ | Attributs | Condition | KeyPath      |
|-----------|----------------------------------------|-------------|------------|-----------|--------------|
| Chaussures  | {F54ABAC0-33F2-11D3-91D7-00C04FD70856} | SPORTDIR    | 2          |           | Baseball.txt |
| Concert   | {76FA7A80-33F6-11D3-91D8-00C04FD70856} | ARTSDIR     | 2          |           | Concert.txt  |
| Jongl     | {CCF834A1-33F8-11D3-91D8-00C04FD70856} | ARTSDIR     | 2          |           | Dance.txt    |
| Terrain  | {CCF834A0-33F8-11D3-91D8-00C04FD70856} | SPORTDIR    | 2          |           | Football.txt |
| Aide      | {AD10EB50-33C1-11D3-91D6-00C04FD70856} | NOTEPADDIR  | 2          |           | Help.txt     |
| Janvier   | {CF0BC690-33C9-11D3-91D6-00C04FD70856} | MONDIR      | 2          |           | January.txt  |
| NewYears  | {A42D9140-33D8-11D3-91D6-00C04FD70856} | HOLDIR      | 2          |           | NewYears.txt |
| Bloc-notes   | {19BED232-30AB-11D3-91D3-00C04FD70856} | NOTEPADDIR  | 2          |           | Redpark.exe  |



 

Les répertoires source et cible de chaque composant sont spécifiés par la valeur entrée dans la \_ colonne répertoire. Le programme d’installation résout l’emplacement de ce répertoire à l’aide des informations contenues dans la table Directory. Le programme d’installation utilise les fichiers de chemin d’accès de clé spécifiés dans la colonne keyPath pour détecter chaque composant. Les attributs d’exécution distante sont définis dans l’exemple afin que les composants puissent être exécutés à partir de la source ou de l’exécution locale.

[Continuer](specifying-files-and-file-attributes.md)

 

 



