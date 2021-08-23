---
description: Une action encapsule une fonction typique effectuée pendant l’installation ou la maintenance d’une application. Windows Le programme d’installation comporte de nombreuses actions standard intégrées. Les développeurs de packages d’installation peuvent également créer leurs propres actions personnalisées.
ms.assetid: 33651988-e371-4258-96a7-bcd7d6762161
title: Actions standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e95c3ab95a7bddc1f23dd38108b2cb10978ad5316da60397e6f3ba019a415ac4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627619"
---
# <a name="standard-actions"></a>Actions standard

Une action encapsule une fonction typique effectuée pendant l’installation ou la maintenance d’une application. Windows Le programme d’installation comporte de nombreuses actions standard intégrées. Les développeurs de packages d’installation peuvent également créer leurs propres [actions personnalisées](custom-actions.md).

Voici quelques exemples d’actions standard du programme d’installation :

-   [Action CreateShortcuts](createshortcuts-action.md): gère la création de raccourcis vers des fichiers installés avec l’application actuelle. Cette action utilise la [table de raccourcis](shortcut-table.md) pour ses données.
-   [Action InstallFiles](installfiles-action.md): copie les fichiers sélectionnés du répertoire source vers le répertoire de destination. Cette action utilise la [table de fichiers](file-table.md) pour ses données.
-   [Action WriteRegistryValues](writeregistryvalues-action.md): configure les informations de Registre requises par l’application dans le registre. Cette action utilise la [table de Registre](registry-table.md) pour ses données.

Les sections suivantes traitent des actions standard.

-   [À propos des actions standard](about-standard-actions.md)
-   [Utilisation d’actions standard](using-standard-actions.md)
-   [Informations de référence sur les actions standard](standard-actions-reference.md)

 

 



