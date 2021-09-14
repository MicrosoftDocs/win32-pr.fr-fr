---
description: ICE91 publie un avertissement si un fichier, un fichier .ini ou un fichier de raccourci est installé dans un répertoire par utilisateur uniquement.
ms.assetid: 1834d841-b1d9-4646-8057-a41dd88310b6
title: ICE91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f5723369c21894817dacbc1755430a31f17199
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021462"
---
# <a name="ice91"></a>ICE91

ICE91 publie un avertissement si un fichier, un fichier .ini ou un fichier de raccourci est installé dans un répertoire par utilisateur uniquement. Ces avertissements sont inoffensifs si le package est utilisé uniquement pour l’installation dans le [contexte d’installation](installation-context.md) par utilisateur et jamais pour les installations par ordinateur.

Les fichiers, les fichiers de .ini ou les raccourcis des répertoires par utilisateur uniquement sont installés dans un profil utilisateur particulier. Même si l’utilisateur définit la propriété [**ALLUSERS**](allusers.md) pour les installations par ordinateur, les fichiers, les fichiers de .ini ou les raccourcis dans les répertoires par utilisateur uniquement ne sont pas copiés dans le profil « tous les utilisateurs » et ne sont pas disponibles pour d’autres utilisateurs. Les répertoires par utilisateur uniquement ne varient pas avec la propriété **ALLUSERS** . Voici une liste des répertoires par utilisateur uniquement :

-   AppDataFolder
-   FavoritesFolder
-   NetHoodFolder
-   PersonalFolder
-   PrintHoodFolder
-   RecentFolder
-   SendToFolder
-   MyPicturesFolder
-   LocalAppDataFolder

## <a name="result"></a>Résultats

ICE91 publie les avertissements suivants.



| AVERTISSEMENT ICE91                                                                                                                                                                                                                            | Description                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Le fichier « \[ 1 \] » sera installé dans le répertoire par utilisateur « \[ 2 \] » qui ne varie pas en fonction de la valeur de [**ALLUSERS**](allusers.md) . Ce fichier ne sera pas copié dans le profil de chaque utilisateur même si une installation par ordinateur est souhaitée.     | Le fichier est installé dans un répertoire par utilisateur uniquement. Il n’est pas installé dans le profil de chaque utilisateur au cours d’une installation par ordinateur.      |
| Le IniFile « \[ 1 \] » sera installé dans le répertoire par utilisateur « \[ 2 \] » qui ne varie pas en fonction de la valeur de [**ALLUSERS**](allusers.md) . Ce fichier ne sera pas copié dans le profil de chaque utilisateur même si une installation par ordinateur est souhaitée.  | Le fichier .ini est installé dans un répertoire par utilisateur uniquement. Il n’est pas installé dans le profil de chaque utilisateur au cours d’une installation par ordinateur. |
| Le raccourci « \[ 1 \] » sera installé dans le répertoire par utilisateur « \[ 2 \] » qui ne varie pas en fonction de la valeur de [**ALLUSERS**](allusers.md) . Ce fichier ne sera pas copié dans le profil de chaque utilisateur même si une installation par ordinateur est souhaitée. | Le raccourci est installé dans un répertoire par utilisateur uniquement. Il n’est pas installé dans le profil de chaque utilisateur au cours d’une installation par ordinateur.  |



 

## <a name="example"></a>Exemple

ICE91 signale les avertissements suivants pour l’exemple :

``` syntax
The file 'File1' will be installed to the per user directory 'MyPicturesFolder' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The IniFile 'IniFile1' will be installed to the per user directory 'MyIniDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The shortcut 'Shortcut1' will be installed to the per user directory 'MyShortcutDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.
```

[Table de fichiers](file-table.md) (partielle)



| Fichier  | Composant\_ |
|-------|-------------|
| Fichier1 | C1          |



 

[Table de composants](component-table.md) (partielle) (partielle) (partielle)



| Composant | Répertoire\_ |
|-----------|-------------|
| C1        | MyDir       |



 

[Table IniFile](inifile-table.md)



| IniFile  | DirProperty |
|----------|-------------|
| IniFile1 | MyIniDir    |



 

[Tableau de raccourcis](shortcut-table.md)



| Raccourci  | Répertoire\_   |
|-----------|---------------|
| Shortcut1 | MyShortcutDir |



 

[Table de répertoire](directory-table.md)



| Répertoire     | Répertoire \_ parent  |
|---------------|--------------------|
| MyDir         | FavoritesFolder    |
| MyIniDir      | LocalAppDataFolder |
| MyShortcutDir | PersonalFolder     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



