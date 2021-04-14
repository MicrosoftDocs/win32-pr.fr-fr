---
title: Paramètres du registre de surveillance des dossiers
description: Paramètres du registre de surveillance des dossiers
ms.assetid: 563aeaec-0759-4b0c-a8e9-a9a2b3092515
keywords:
- Lecteur Windows Media, paramètres du registre de surveillance des dossiers
- Lecteur Windows Media, paramètres du registre de surveillance du dossier de fichiers
- Lecteur Windows Media, registre
- Registre, paramètres de surveillance des dossiers
- Registre, paramètres d’analyse des dossiers de fichiers
- Registre, paramètres pour le lecteur Windows Media
- paramètres du registre de surveillance des dossiers
- paramètres du registre de surveillance du dossier de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233076d1fc807dd5cdd79e9b4985ef752fba0815
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383088"
---
# <a name="folder-monitoring-registry-settings"></a>Paramètres du registre de surveillance des dossiers

Le lecteur Windows Media série 9 ou une version ultérieure peut surveiller les dossiers de fichiers pour les nouveaux fichiers multimédias numériques. Lorsque le lecteur détecte un nouveau fichier dans un dossier surveillé, il ajoute automatiquement le fichier à la bibliothèque. Pour le lecteur Windows Media 9 jusqu’au lecteur Windows Media 11, les utilisateurs peuvent modifier la liste des dossiers surveillés en cliquant sur **surveiller les dossiers** sous l’onglet Bibliothèque de la boîte de dialogue **options** . Pour le lecteur Windows Media 12, un utilisateur peut modifier la liste des dossiers surveillés en suivant les instructions de la rubrique [Ajouter des éléments à la bibliothèque du lecteur Windows Media](https://windows.microsoft.com/windows7/Add-items-to-the-Windows-Media-Player-Library). Pour le lecteur Windows Media 9 jusqu’au lecteur Windows Media 11, vous pouvez ajouter par programmation un dossier à analyser en ajoutant une valeur au registre. Pour le lecteur Windows Media 12, vous ne pouvez pas utiliser le registre pour ajouter ou supprimer par programmation des dossiers à analyser.

Pour le lecteur Windows Media 9 jusqu’au lecteur Windows Media 11, pour ajouter un dossier à surveiller, vous devez d’abord créer ou modifier deux valeurs dans la clé de Registre suivante :

**HKEY \_ \_ logiciel utilisateur \\ actuel \\ \\ Préférences Microsoft MediaPlayer \\\\**

Les nouvelles valeurs doivent être nommées comme suit.



| Nom                           | Type           | Description                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **TrackFoldersDirectories**    | **\_valeur DWORD reg** | Valeur **DWORD** qui représente le nombre de dossiers à surveiller. Cela doit correspondre au nombre de valeurs **TrackFoldersDirectories ** * * X.                                                                                                                                         |
| **TrackFoldersDirectories * * * X* | **SZ de REG \_**    | Valeur de chaîne qui représente le chemin d’accès du dossier à surveiller. Chaque dossier à surveiller requiert une valeur distincte. Le suffixe *X* est un entier qui doit toujours commencer à 0, puis être incrémenté de 1. Le lecteur Windows Media surveille également les sous-dossiers du dossier spécifié. |



 

Par exemple, pour ajouter le premier dossier à surveiller, ajoutez la valeur suivante :


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories0" = "c:\MyPath\MyFolder"

```



Ensuite, créez la valeur de nombre :


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000001

```



Pour ajouter un deuxième dossier à surveiller, ajoutez la valeur suivante :


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories1" = "c:\MyPath\MyFolder2"

```



Incrémentez ensuite la valeur Count :


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000002

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Paramètres du Registre**](registry-settings.md)
</dt> </dl>

 

 




