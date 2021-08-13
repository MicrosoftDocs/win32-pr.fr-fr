---
description: avertit le Windows Installer d’utiliser le gestionnaire de redémarrage pour arrêter toutes les applications qui ont des fichiers en cours d’utilisation et les redémarrer à la fin de l’installation.
ms.assetid: bfa19cc8-4cf7-42ed-9e94-acaeca8d707a
title: RmShutdownAndRestart ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f483e485eeefc2d3a761a3d9c9ff95989a3150dcfd8fff6a36bfb6211504e95e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625889"
---
# <a name="rmshutdownandrestart-controlevent"></a>RmShutdownAndRestart ControlEvent,

cet événement avertit le Windows Installer d’utiliser le [gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) pour arrêter toutes les applications qui ont des fichiers en cours d’utilisation et les redémarrer à la fin de l’installation.

Ce ControlEvent, n’a aucun effet si l’une des conditions suivantes est vraie.

-   le système d’exploitation qui exécute l’installation n’est pas Windows Vista ni Windows Server 2008.
-   Les interactions avec le [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) ont été désactivées par la propriété [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) ou la stratégie [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) .
-   Aucune session du gestionnaire de [redémarrage](../rstmgr/restart-manager-portal.md) n’est actuellement ouverte.
-   tous les appels de la Windows Installer au [gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) retourne un échec.

## <a name="typical-use"></a>Utilisation courante

L’événement de contrôle RMShutdownAndRestart est publié uniquement par un contrôle [PUSHBUTTON](pushbutton-control.md) dans la boîte de [dialogue MsiRMFilesInUse](msirmfilesinuse-dialog.md) .

 

 
