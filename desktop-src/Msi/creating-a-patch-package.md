---
description: Les développeurs créent un package de correctifs en générant un fichier de création de correctifs et en utilisant Msimsp.exe pour appeler la fonction UiCreatePatchPackageEx dans Patchwiz.dll.
ms.assetid: 8a163653-6ba1-46ea-9832-f998749d29ae
title: Création d’un package de correctifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2561cb6729dc7b4e0e48acd13b6338f08a8ba943
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091886"
---
# <a name="creating-a-patch-package"></a>Création d’un package de correctifs

Les développeurs créent un package de correctifs en générant un fichier de création de correctifs et en utilisant [Msimsp.exe](msimsp-exe.md) pour appeler la fonction [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) dans [Patchwiz.dll](patchwiz-dll.md). Msimsp.exe et Patchwiz.dll sont fournis dans le kit de développement logiciel (SDK) Windows Installer. Pour plus d’informations, consultez [un exemple de mise à jour corrective de petite taille](a-small-update-patching-example.md).

étant donné que l’application d’un correctif à un package Windows Installer entraîne l’installation des sources d’origine à l’aide d’un nouveau fichier .msi, le nouveau fichier de .msi doit rester compatible avec la disposition de la source d’origine.

Lorsque vous créez un package de correctifs, vous devez utiliser une image d’installation non compressée pour créer un correctif, par exemple une image administrative ou une image d’installation non compressée à partir d’un CD-ROM. Vous devez également respecter les restrictions suivantes :

-   Ne déplacez pas les fichiers d’un dossier vers un autre.
-   Ne déplacez pas les fichiers d’un fichier CAB vers un autre.
-   Ne modifiez pas l’ordre des fichiers dans un fichier CAB.
-   Ne modifiez pas le numéro de séquence des fichiers existants. Le numéro de séquence est la valeur spécifiée dans la colonne séquence de la [table file](file-table.md).
-   Tout nouveau fichier ajouté par le correctif doit être placé à la fin de la séquence de fichiers existante. Le numéro de séquence de tout nouveau fichier dans l’image mise à niveau doit être supérieur au numéro de séquence le plus élevé des fichiers existants dans l’image cible.
-   Ne modifiez pas les clés primaires dans la [table de fichiers](file-table.md) entre les versions d’origine et des nouvelles versions de fichiers .msi.
    > [!Note]  
    > Le fichier doit avoir la même clé dans la [table de fichiers](file-table.md) de l’image cible et de l’image mise à jour. Les valeurs de chaîne dans la colonne file des deux tables doivent être identiques, y compris le cas.

     

-   Ne créez pas de package avec des clés de [table de fichiers](file-table.md) qui diffèrent uniquement par la casse, par exemple, évitez l’exemple de table suivant.

    

    | Fichier       | Composant\_ | FileName   |
    |------------|-------------|------------|
    | readme.txt | COMP1       | readme.txt |
    | ReadMe.txt | COMP2       | readme.txt |

    

     

    les Windows Installer peuvent autoriser l’exemple de table précédent lorsque Comp1 et Comp2 sont installés sur des répertoires différents, mais que vous ne pouvez pas utiliser [Msimsp.exe](msimsp-exe.md) ou [Patchwiz.dll](patchwiz-dll.md) pour générer un correctif pour le package. Msimsp.exe et Patchwiz.dll appel de Makecab.exe, qui ne respecte pas la casse et qui échoue.

    Lorsque vous utilisez des modules de fusion dans le programme d’installation, assurez-vous que les numéros de séquence et la disposition des fichiers adhèrent aux indications ci-dessus.

 

 



