---
title: Annulation d’un événement de minuterie
description: Annulation d’un événement de minuterie
ms.assetid: 4c1be031-e3d5-4d7c-b197-c40c61fc4e2f
keywords:
- minuteries multimédias, événements
- minuteries, événements
- timeKillEvent fonction)
- annulation des événements du minuteur
- minuteries multimédias, annulation d’événements
- minuteries, annuler des événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1380b2868596e0177e806f5df5217bb839abe61c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031203"
---
# <a name="canceling-a-timer-event"></a><span data-ttu-id="6a2c0-109">Annulation d’un événement de minuterie</span><span class="sxs-lookup"><span data-stu-id="6a2c0-109">Canceling a Timer Event</span></span>

> [!Note]  
> <span data-ttu-id="6a2c0-110">Cette rubrique décrit une fonction obsolète.</span><span class="sxs-lookup"><span data-stu-id="6a2c0-110">This topic describes an obsolete function.</span></span> <span data-ttu-id="6a2c0-111">Les nouvelles applications doivent utiliser la fonction [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) pour créer des minuteries.</span><span class="sxs-lookup"><span data-stu-id="6a2c0-111">New applications should use the [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function to create timers.</span></span>

 

<span data-ttu-id="6a2c0-112">Pour chaque minuteur périodique créant en appelant [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)), l’application doit annuler la minuterie en appelant la fonction [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) avant de libérer la mémoire qui contient la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="6a2c0-112">For every periodic timer creating by calling [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)), the application must cancel the timer by calling the [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) function before it frees the memory that contains the callback function.</span></span> <span data-ttu-id="6a2c0-113">Pour annuler un événement de minuteur, il peut appeler la fonction suivante.</span><span class="sxs-lookup"><span data-stu-id="6a2c0-113">To cancel a timer event, it might call the following function.</span></span>


```C++
void DestroyTimer(NPSEQ npSeq)
{
    if(npSeq->wTimerID) {                // is timer event pending?
        timeKillEvent(npSeq->wTimerID);  // cancel the event
        npSeq->wTimerID = 0;
    }
} 
```



## <a name="related-topics"></a><span data-ttu-id="6a2c0-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6a2c0-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a2c0-115">Utilisation de minuteurs multimédias</span><span class="sxs-lookup"><span data-stu-id="6a2c0-115">Using Multimedia Timers</span></span>](using-multimedia-timers.md)
</dt> </dl>

 

 