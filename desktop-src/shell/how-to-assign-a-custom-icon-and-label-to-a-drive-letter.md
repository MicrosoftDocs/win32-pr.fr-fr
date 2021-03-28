---
description: Spécifiez une icône et une étiquette personnalisées pour un lecteur.
ms.assetid: B6EF7F84-7747-4689-B740-A91CA8E394D7
title: Affecter une icône et une étiquette personnalisées à une lettre de lecteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 848c076db443c502a667d67e0b7b49ce51db4ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973187"
---
# <a name="how-to-assign-a-custom-icon-and-label-to-a-drive-letter"></a>Comment attribuer une icône et une étiquette personnalisées à une lettre de lecteur

Spécifiez une icône et une étiquette personnalisées pour un lecteur.

## <a name="instructions"></a>Instructions

### <a name="step-1-replacing-the-standard-drive-icon-with-a-custom-icon-in-windows-2000"></a>Étape 1 : remplacement de l’icône de lecteur standard par une icône personnalisée dans Windows 2000

Pour remplacer l’icône de lecteur standard par une icône personnalisée dans Windows 2000, ajoutez une sous-clé nommée pour la lettre de lecteur à la clé suivante.

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
```

L’exemple suivant spécifie une icône et une étiquette personnalisées pour le lecteur E :. L’icône se trouve dans le fichier C : \\ MyDir \\MyDrive.exe avec un index de base zéro de trois.

Pour Windows 2000 :

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
            E
               DefaultIcon
                  (Default) = C:\MyDir\MyDrive.exe,3
               DefaultLabel
                  (Default) = MyDrive
```

### <a name="step-2-replacing-the-standard-drive-icon-with-a-custom-icon-in-all-other-versions-of-windows"></a>Étape 2 : remplacement de l’icône de lecteur standard par une icône personnalisée dans toutes les autres versions de Windows

Pour remplacer l’icône de lecteur standard par une icône personnalisée dans toutes les versions de Windows autres que Windows 2000, ajoutez une sous-clé nommée pour la lettre de lecteur à la clé suivante.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
```

L’exemple suivant spécifie une icône et une étiquette personnalisées pour le lecteur E :. L’icône se trouve dans le fichier C : \\ MyDir \\MyDrive.exe avec un index de base zéro de trois.

Pour toutes les autres versions de Windows :

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
                     E
                        DefaultIcon
                           (Default) = C:\MyDir\MyDrive.exe,3
                        DefaultLabel
                           (Default) = MyDrive
```

### <a name="step-3-calling-the-shupdateimage-event"></a>Étape 3 : appel de l’événement SHUpdateImage

Dans toutes les versions de Windows, si vous modifiez un type de fichier ou une icône de lecteur, vous devez également appeler SHUpdateImage pour notifier à l’interpréteur de mise à jour toutes les icônes qui sont actuellement affichées.

## <a name="remarks"></a>Notes

La lettre de lecteur ne doit pas être suivie d’un signe deux-points ( :). Ajoutez une sous-clé **DefaultIcon** à la sous-clé de lecteur et définissez sa valeur par défaut sur une chaîne qui contient l’emplacement de l’icône. La première partie de la chaîne contient le chemin d’accès complet du fichier de l’icône. Si le fichier contient plusieurs icônes, le chemin d’accès est suivi d’une virgule, puis de l’index de base zéro de l’icône.

 

 



