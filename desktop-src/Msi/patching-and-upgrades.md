---
description: étant donné qu’un package d’installation peut contenir les fichiers qui composent une application, ainsi que les informations nécessaires à leur installation, Windows Installer peut être utilisé pour mettre à jour l’application.
ms.assetid: da946739-9efc-4bf0-8a9a-6f6ead3c4a34
title: Correctifs et mises à niveau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aad2b5564309e2faaa43c322da93834d4c8fe174e373b61707a853b56b097e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042409"
---
# <a name="patching-and-upgrades"></a>Correctifs et mises à niveau

étant donné qu’un package d’installation peut contenir les fichiers qui composent une application, ainsi que les informations nécessaires à leur installation, Windows Installer peut être utilisé pour mettre à jour l’application. Le programme d’installation peut mettre à jour les informations dans les parties suivantes du package d’installation :

-   Fichier .msi.
-   Fichiers de l’application.
-   informations d’inscription de Windows Installer.

Le type de mise à jour peut être caractérisé par les modifications apportées par la mise à jour au code du produit, à la version du produit et au code du package de l’application. La version du produit de l’application est stockée dans la propriété [**ProductVersion**](productversion.md) . Le code du produit de l’application est stocké dans la propriété [**ProductCode**](productcode.md) . Le code du [package](package-codes.md) de l’application est stocké dans la propriété [**Résumé du numéro de révision**](revision-number-summary.md) .

Une mise à jour qui modifie l’application en un autre produit est nécessaire pour modifier la valeur [**ProductCode**](productcode.md) de l’application. Pour plus d’informations sur les mises à jour qui nécessitent la modification de la **ProductCode** , consultez [modification du code du produit](changing-the-product-code.md). La mise à jour peut modifier le [**ProductVersion**](productversion.md) et ne pas modifier la valeur **ProductCode** si les versions ultérieures de l’application doivent faire la différence entre les versions mises à jour et non mises à jour du produit actuel. Le [Code du package](package-codes.md) identifie de façon unique le package d’installation et doit toujours être modifié chaque fois que la mise à niveau ou la mise à niveau modifie toutes les informations contenues dans le package d’installation.

Lorsque vous décidez de modifier la version du produit, vous devez envisager si les versions ultérieures de l’application devront faire la différence entre les versions mises à jour et non mises à jour du produit actuel. Pour garantir une différenciation à l’avenir, une [mise à niveau mineure](minor-upgrades.md) doit être utilisée à la place d’une [petite mise à jour](small-updates.md).

-   Si une mise à jour modifie le fichier d' .msi et les fichiers d’application, mais ne modifie pas la propriété [**ProductCode**](productcode.md) ou la propriété [**ProductVersion**](productversion.md) , elle est appelée [petite mise à jour](small-updates.md).
-   Si la mise à jour modifie le [**ProductVersion**](productversion.md), mais ne modifie pas la [**ProductCode**](productcode.md), une [mise à niveau mineure](minor-upgrades.md)est appelée.
-   Si la mise à jour change l’installation en un produit entièrement différent, le [**ProductCode**](productcode.md) doit changer et la mise à jour est appelée [mise à niveau majeure](major-upgrades.md).

> [!Note]  
> Pour garantir la différenciation des versions du produit actuel à l’avenir, une [mise à niveau mineure](minor-upgrades.md) doit être utilisée à la place d’une [petite mise à jour](small-updates.md).

 

Le tableau suivant résume les différents types de mises à jour.



| Type de mise à jour                       | ProductCode | ProductVersion | Description                                                                                                                                                                                                                                                                                                           |
|--------------------------------------|-------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Petite mise à jour](small-updates.md)    | Aucun changement   | Aucun changement      | Mise à jour d’un ou de deux fichiers trop petits pour justifier la modification du [**ProductVersion**](productversion.md). Le code du package dans la propriété [**Résumé du numéro de révision**](revision-number-summary.md) change. Peut être fourni sous la forme d’un package d’installation complète ou d’un [package de correctifs](patch-packages.md). |
| [Mise à niveau mineure](minor-upgrades.md)  | Aucun changement   | Modifié        | Une petite mise à jour qui apporte des modifications suffisamment significatives pour justifier la modification de la propriété [**ProductVersion**](productversion.md) . Peut être fourni sous la forme d’un package d’installation complète ou d’un [package de correctifs](patch-packages.md).                                                                                                |
| [Mises à niveau majeures](major-upgrades.md) | Modifié     | Modifié        | Une mise à jour complète du produit justifiant une modification de la propriété [**ProductCode**](productcode.md) . Fourni en tant que [package correctif](patch-packages.md) ou en tant que package d’installation complète du produit.                                                                                                             |



 

> [!Note]  
> la Windows Installer peut installer une application, ou une mise à jour, pour tous les utilisateurs d’un ordinateur (contexte par ordinateur) ou pour un utilisateur particulier (contexte par utilisateur) en fonction des privilèges d’accès de l’utilisateur, de la valeur de la propriété [**ALLUSERS**](allusers.md) et de la version du système d’exploitation. Les développeurs d’applications doivent prendre en compte les mises à jour de contexte qui seront installées. Si les contextes de l’application et de la mise à jour sont différents, l’application peut ne pas être mise à jour comme prévu.

 

les utilisateurs peuvent effectuer une mise à jour vers une application en réinstallant un package Windows Installer pour l’application. Notez que les [mises à niveau mineures](minor-upgrades.md) peuvent être appliquées de la même façon que les [petites mises à jour](small-updates.md). Pour plus d’informations sur la mise à jour d’une application en réinstallant l’application, consultez les sections suivantes :

-   [Application de petites mises à jour en réinstallant le produit](applying-small-updates-by-reinstalling-the-product.md)
-   [Application de mises à niveau majeures en installant le produit](applying-major-upgrades-by-installing-the-product.md)

une mise à jour d’une application peut être fournie aux utilisateurs en tant que package correctif Windows Installer. Un correctif peut contenir un fichier entier ou uniquement les bits de fichier nécessaires à la mise à jour d’une partie d’un fichier. Cela signifie que l’utilisateur peut télécharger un correctif de mise à niveau qui est plus petit que l’ensemble du produit et qui préserve les personnalisations de l’utilisateur via la mise à niveau. Notez que les [mises à niveau mineures](minor-upgrades.md) peuvent être appliquées de la même façon que les [petites mises à jour](small-updates.md). Pour plus d’informations sur la mise à jour d’une application à l’aide d’un correctif, consultez les sections suivantes :

-   [Application de correctifs](patching.md)
-   [Création d’un correctif de mise à jour de petite taille](creating-a-small-update-patch.md)
-   [Application de petites mises à jour en appliquant des correctifs à l’installation locale du produit](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
-   [Application de petites mises à jour en corrigeant une image administrative](applying-small-updates-by-patching-an-administrative-image.md)
-   [Application de mises à niveau majeures en appliquant des correctifs à l’installation locale du produit](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)

 

 



