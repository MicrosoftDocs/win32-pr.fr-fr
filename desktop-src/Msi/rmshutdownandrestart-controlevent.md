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
# <a name="rmshutdownandrestart-controlevent"></a><span data-ttu-id="55ca3-103">RmShutdownAndRestart ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="55ca3-103">RmShutdownAndRestart ControlEvent</span></span>

<span data-ttu-id="55ca3-104">Cet événement avertit le Windows Installer d’utiliser le [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) pour arrêter toutes les applications qui ont des fichiers en cours d’utilisation et les redémarrer à la fin de l’installation.</span><span class="sxs-lookup"><span data-stu-id="55ca3-104">This event notifies the Windows Installer to use the [Restart Manager](../rstmgr/restart-manager-portal.md) to shutdown all applications that have files in use and to restart them at the end of the installation.</span></span>

<span data-ttu-id="55ca3-105">Ce ControlEvent, n’a aucun effet si l’une des conditions suivantes est vraie.</span><span class="sxs-lookup"><span data-stu-id="55ca3-105">This ControlEvent has no effect if any of the following are true.</span></span>

-   <span data-ttu-id="55ca3-106">Le système d’exploitation qui exécute l’installation n’est pas Windows Vista ou Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="55ca3-106">The operating system running the installation is not Windows Vista or Windows Server 2008.</span></span>
-   <span data-ttu-id="55ca3-107">Les interactions avec le [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) ont été désactivées par la propriété [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) ou la stratégie [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="55ca3-107">Interactions with the [Restart Manager](../rstmgr/restart-manager-portal.md) have been disabled by the [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) property or the [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) policy.</span></span>
-   <span data-ttu-id="55ca3-108">Aucune session du gestionnaire de [redémarrage](../rstmgr/restart-manager-portal.md) n’est actuellement ouverte.</span><span class="sxs-lookup"><span data-stu-id="55ca3-108">There is currently no open [Restart Manager](../rstmgr/restart-manager-portal.md) session.</span></span>
-   <span data-ttu-id="55ca3-109">Tous les appels de la Windows Installer au [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) retourne un échec.</span><span class="sxs-lookup"><span data-stu-id="55ca3-109">Any calls from the Windows Installer to the [Restart Manager](../rstmgr/restart-manager-portal.md) returns a failure.</span></span>

## <a name="typical-use"></a><span data-ttu-id="55ca3-110">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="55ca3-110">Typical Use</span></span>

<span data-ttu-id="55ca3-111">L’événement de contrôle RMShutdownAndRestart est publié uniquement par un contrôle [PUSHBUTTON](pushbutton-control.md) dans la boîte de [dialogue MsiRMFilesInUse](msirmfilesinuse-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="55ca3-111">The RMShutdownAndRestart control event is published only by a [PushButton](pushbutton-control.md) control on the [MsiRMFilesInUse Dialog](msirmfilesinuse-dialog.md) box.</span></span>

 

 
