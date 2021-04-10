---
title: Obtention de l’état d’une opération du gestionnaire de redémarrage
description: Lorsque de nombreuses applications et services doivent être arrêtés ou redémarrés, l’opération du gestionnaire de redémarrage peut prendre un certain temps. La méthode suivante peut être utilisée pour obtenir l’état de l’opération en cours.
ms.assetid: 0df9de1f-df37-46a5-8010-6c8b34429376
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afa5f329a8f21aa625c5c7b61a3e65b2c907bbf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102176"
---
# <a name="getting-the-status-of-a-restart-manager-operation"></a><span data-ttu-id="0dbe1-104">Obtention de l’état d’une opération du gestionnaire de redémarrage</span><span class="sxs-lookup"><span data-stu-id="0dbe1-104">Getting the Status of a Restart Manager Operation</span></span>

<span data-ttu-id="0dbe1-105">Lorsque de nombreuses applications et services doivent être arrêtés ou redémarrés, l’opération du gestionnaire de redémarrage peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="0dbe1-105">When many applications and services must be shut down or restarted, the Restart Manager operation can take an extended period of time.</span></span> <span data-ttu-id="0dbe1-106">La méthode suivante peut être utilisée pour obtenir l’état de l’opération en cours.</span><span class="sxs-lookup"><span data-stu-id="0dbe1-106">The following method can be used to obtain the status of the current operation.</span></span>

<span data-ttu-id="0dbe1-107">**Pour connaître l’état de l’opération du gestionnaire de redémarrage en cours**</span><span class="sxs-lookup"><span data-stu-id="0dbe1-107">**To get the status of the current Restart Manager operation**</span></span>

1.  <span data-ttu-id="0dbe1-108">Le programme d’installation doit implémenter une fonction de [**\_ rappel d' \_ état \_ d’écriture RM**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) qui détermine l’état des applications qui ont été arrêtées ou redémarrées.</span><span class="sxs-lookup"><span data-stu-id="0dbe1-108">The installer should implement a [**RM\_WRITE\_STATUS\_CALLBACK**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) function that determines the status of the applications that have been shut down or restarted.</span></span> <span data-ttu-id="0dbe1-109">La fonction peut fournir les informations à l’interface utilisateur ou au journal.</span><span class="sxs-lookup"><span data-stu-id="0dbe1-109">The function can provide the information to the user interface or log.</span></span>
2.  <span data-ttu-id="0dbe1-110">Le programme d’installation passe le pointeur vers la fonction de [**rappel d’état d' \_ écriture \_ \_ RM**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) lors de l’appel de la fonction [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) ou [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) .</span><span class="sxs-lookup"><span data-stu-id="0dbe1-110">The installer passes the pointer to the [**RM\_WRITE\_STATUS\_CALLBACK**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) function when calling the [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) or [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) function.</span></span>

 

 