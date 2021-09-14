---
description: La boîte de dialogue MsiRMFilesInUse peut être créée pour afficher une liste des processus en cours d’exécution des fichiers qui doivent être remplacés ou supprimés par l’installation.
ms.assetid: e8d93310-388e-4a08-9bce-04c31c33a665
title: Boîte de dialogue MsiRMFilesInUse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bba73cab51f4b3d8321b15001dbb72c638176b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119701"
---
# <a name="msirmfilesinuse-dialog"></a>Boîte de dialogue MsiRMFilesInUse

La boîte de dialogue MsiRMFilesInUse peut être créée pour afficher une liste des processus en cours d’exécution des fichiers qui doivent être remplacés ou supprimés par l’installation. L’utilisateur peut choisir entre les options « fermer automatiquement les applications et les redémarrer » ou «ne pas fermer les applications. (Un redémarrage sera nécessaire.)» Si l’utilisateur sélectionne l’option « fermer automatiquement les applications et les redémarrer », un contrôle de bouton de commande dans cette boîte de dialogue peut être créé pour publier l’événement de contrôle RMShutdownAndRestart et le [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) peut fermer les applications et les redémarrer à la fin de l’installation. Cela permet d’éliminer ou de réduire la nécessité de redémarrer l’ordinateur. Pour plus d’informations, consultez [redémarrages du système](system-reboots.md).

La boîte de dialogue **MsiRMFilesInUse** s’affiche au cours d’une installation uniquement si tous les éléments suivants sont vrais. lorsque l’un de ces deux est false, la Windows Installer ignore la boîte de dialogue **MsiRMFilesInUse** .

-   une version de Windows Installer qui n’est pas antérieure à la version 4,0 et un système d’exploitation qui n’est pas antérieur à Windows Vista ou Windows Server 2008 exécute l’installation.
-   Le niveau complet de l' [interface utilisateur](user-interface-levels.md) de l’interface utilisateur est utilisé.
-   Les interactions avec le [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) n’ont pas été désactivées par la propriété [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) ou la stratégie [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) .
-   La boîte de dialogue **MsiRMFilesInUse** est présente dans le package d’installation.
-   tous les appels de la Windows Installer au [gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) réussissent.

Cette boîte de dialogue est créée comme requis par l' [action InstallValidate](installvalidate-action.md).

 

 
