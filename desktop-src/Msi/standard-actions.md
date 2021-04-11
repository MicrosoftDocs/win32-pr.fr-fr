---
description: Une action encapsule une fonction typique effectuée pendant l’installation ou la maintenance d’une application. Windows Installer possède de nombreuses actions standard intégrées. Les développeurs de packages d’installation peuvent également créer leurs propres actions personnalisées.
ms.assetid: 33651988-e371-4258-96a7-bcd7d6762161
title: Actions standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ed4f9c2a7fc6671442f6b72cd10889e2fcf5e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202400"
---
# <a name="standard-actions"></a>Actions standard

Une action encapsule une fonction typique effectuée pendant l’installation ou la maintenance d’une application. Windows Installer possède de nombreuses actions standard intégrées. Les développeurs de packages d’installation peuvent également créer leurs propres [actions personnalisées](custom-actions.md).

Voici quelques exemples d’actions standard du programme d’installation :

-   [Action CreateShortcuts](createshortcuts-action.md): gère la création de raccourcis vers des fichiers installés avec l’application actuelle. Cette action utilise la [table de raccourcis](shortcut-table.md) pour ses données.
-   [Action InstallFiles](installfiles-action.md): copie les fichiers sélectionnés du répertoire source vers le répertoire de destination. Cette action utilise la [table de fichiers](file-table.md) pour ses données.
-   [Action WriteRegistryValues](writeregistryvalues-action.md): configure les informations de Registre requises par l’application dans le registre. Cette action utilise la [table de Registre](registry-table.md) pour ses données.

Les sections suivantes traitent des actions standard.

-   [À propos des actions standard](about-standard-actions.md)
-   [Utilisation d’actions standard](using-standard-actions.md)
-   [Informations de référence sur les actions standard](standard-actions-reference.md)

 

 



