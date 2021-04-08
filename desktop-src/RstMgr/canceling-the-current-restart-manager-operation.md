---
title: Annulation de l’opération de redémarrage du gestionnaire en cours
description: Lorsqu’une action de l’utilisateur indique au programme d’installation d’effectuer une action différente, la méthode suivante peut être utilisée pour annuler l’opération du gestionnaire de redémarrage en cours.
ms.assetid: 87c8cf27-cd77-46fb-8298-cccbf4b1071a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633882cc723f19823c6b832ee6927c5a3aacaab7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675973"
---
# <a name="canceling-the-current-restart-manager-operation"></a><span data-ttu-id="3fda0-103">Annulation de l’opération de redémarrage du gestionnaire en cours</span><span class="sxs-lookup"><span data-stu-id="3fda0-103">Canceling the Current Restart Manager Operation</span></span>

<span data-ttu-id="3fda0-104">Lorsqu’une action de l’utilisateur indique au programme d’installation d’effectuer une action différente, la méthode suivante peut être utilisée pour annuler l’opération du gestionnaire de redémarrage en cours.</span><span class="sxs-lookup"><span data-stu-id="3fda0-104">When a user action directs the installer to perform a different action, the following method can be used to cancel the current Restart Manager operation.</span></span>

<span data-ttu-id="3fda0-105">**Pour annuler l’opération du gestionnaire de redémarrage en cours**</span><span class="sxs-lookup"><span data-stu-id="3fda0-105">**To cancel the current Restart Manager operation**</span></span>

-   <span data-ttu-id="3fda0-106">Le programme d’installation peut appeler la fonction [**RMCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) à partir d’un autre thread pour annuler l’opération [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) ou [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) en cours.</span><span class="sxs-lookup"><span data-stu-id="3fda0-106">The installer can call the [**RMCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) function from another thread to cancel the current [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) or [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) operation.</span></span> <span data-ttu-id="3fda0-107">Le gestionnaire de redémarrage peut annuler l’opération en fonction de la mesure dans laquelle l’opération est terminée lorsque la fonction **RMCancelCurrentTask** est appelée.</span><span class="sxs-lookup"><span data-stu-id="3fda0-107">The Restart Manager may cancel the operation depending on the extent to which the operation has completed when the **RMCancelCurrentTask** function is called.</span></span>

 

 




