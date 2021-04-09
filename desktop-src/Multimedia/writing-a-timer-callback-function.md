---
title: Écriture d’une fonction de rappel de minuterie
description: Écriture d’une fonction de rappel de minuterie
ms.assetid: 85260b6b-42de-43f4-83b7-94edbf660006
keywords:
- minuteries multimédias, fonctions de rappel
- minuteries, fonctions de rappel
- écriture de fonctions de rappel de minuterie
- minuteries multimédias, écrire des fonctions de rappel
- minuteries, écrire des fonctions de rappel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 609cf2dda455897fb6cae0f3c48252016ba54cb9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940899"
---
# <a name="writing-a-timer-callback-function"></a><span data-ttu-id="f53c2-108">Écriture d’une fonction de rappel de minuterie</span><span class="sxs-lookup"><span data-stu-id="f53c2-108">Writing a Timer Callback Function</span></span>

> [!Note]  
> <span data-ttu-id="f53c2-109">Cette rubrique décrit une fonction obsolète.</span><span class="sxs-lookup"><span data-stu-id="f53c2-109">This topic describes an obsolete function.</span></span> <span data-ttu-id="f53c2-110">Les nouvelles applications doivent utiliser la fonction [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) pour créer des minuteries.</span><span class="sxs-lookup"><span data-stu-id="f53c2-110">New applications should use the [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function to create timers.</span></span>

 

<span data-ttu-id="f53c2-111">La fonction de rappel suivante, OneShotTimer, invalide l’identificateur pour l’événement de minuterie unique et appelle une routine de minuterie pour gérer les tâches spécifiques à l’application.</span><span class="sxs-lookup"><span data-stu-id="f53c2-111">The following callback function, OneShotTimer, invalidates the identifier for the single timer event and calls a timer routine to handle the application-specific tasks.</span></span> <span data-ttu-id="f53c2-112">Pour plus d’informations, consultez [**TimeProc**](/previous-versions//dd757631(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f53c2-112">For more information, see [**TimeProc**](/previous-versions//dd757631(v=vs.85)).</span></span>


```C++
void CALLBACK OneShotTimer(UINT wTimerID, UINT msg, 
    DWORD dwUser, DWORD dw1, DWORD dw2) 
{ 
    NPSEQ npSeq;             // pointer to sequencer data 
    npSeq = (NPSEQ)dwUser;
    npSeq->wTimerID = 0;     // invalidate timer ID (no longer in use)
    TimerRoutine(npSeq);     // handle tasks 
} 
```



## <a name="related-topics"></a><span data-ttu-id="f53c2-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f53c2-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f53c2-114">Utilisation de minuteurs multimédias</span><span class="sxs-lookup"><span data-stu-id="f53c2-114">Using Multimedia Timers</span></span>](using-multimedia-timers.md)
</dt> </dl>

 

 