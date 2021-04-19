---
description: Avertit le Windows Installer d’utiliser le gestionnaire de redémarrage pour arrêter toutes les applications qui ont des fichiers en cours d’utilisation et les redémarrer à la fin de l’installation.
ms.assetid: bfa19cc8-4cf7-42ed-9e94-acaeca8d707a
title: RmShutdownAndRestart ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc91d1de52f516c0728e8d6469fb8cddc2e50cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518157"
---
# <a name="rmshutdownandrestart-controlevent"></a>RmShutdownAndRestart ControlEvent,

Cet événement avertit le Windows Installer d’utiliser le [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) pour arrêter toutes les applications qui ont des fichiers en cours d’utilisation et les redémarrer à la fin de l’installation.

Ce ControlEvent, n’a aucun effet si l’une des conditions suivantes est vraie.

-   Le système d’exploitation qui exécute l’installation n’est pas Windows Vista ou Windows Server 2008.
-   Les interactions avec le [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) ont été désactivées par la propriété [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) ou la stratégie [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) .
-   Aucune session du gestionnaire de [redémarrage](../rstmgr/restart-manager-portal.md) n’est actuellement ouverte.
-   Tous les appels de la Windows Installer au [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) retourne un échec.

## <a name="typical-use"></a>Utilisation courante

L’événement de contrôle RMShutdownAndRestart est publié uniquement par un contrôle [PUSHBUTTON](pushbutton-control.md) dans la boîte de [dialogue MsiRMFilesInUse](msirmfilesinuse-dialog.md) .

 

 
