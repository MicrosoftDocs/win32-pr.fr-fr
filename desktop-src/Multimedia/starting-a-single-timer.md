---
title: Démarrage d’un événement de minuterie unique
description: Démarrage d’un événement de minuterie unique
ms.assetid: 56010877-1a02-4a7b-b58c-9f96b169acb2
keywords:
- minuteries multimédias, événements
- minuteries, événements
- minuteries multimédias, événements de démarrage
- minuteries, événements de démarrage
- timeSetEvent fonction)
- démarrage des événements du minuteur
- événements à une seule minuterie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9d0024e3dfa9b0bda79f209abd9b81e89ad11c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381834"
---
# <a name="starting-a-single-timer-event"></a><span data-ttu-id="3ac09-110">Démarrage d’un événement de minuterie unique</span><span class="sxs-lookup"><span data-stu-id="3ac09-110">Starting a Single Timer Event</span></span>

> [!Note]  
> <span data-ttu-id="3ac09-111">Cette rubrique décrit une fonction obsolète.</span><span class="sxs-lookup"><span data-stu-id="3ac09-111">This topic describes an obsolete function.</span></span> <span data-ttu-id="3ac09-112">Les nouvelles applications doivent utiliser la fonction [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) pour créer des minuteries.</span><span class="sxs-lookup"><span data-stu-id="3ac09-112">New applications should use the [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function to create timers.</span></span>

 

<span data-ttu-id="3ac09-113">Pour démarrer un événement à minuterie unique, appelez la fonction [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) , en spécifiant la durée avant le rappel, la résolution, l’adresse de la fonction de rappel (voir [**TimeProc**](/previous-versions//dd757631(v=vs.85))) et les données utilisateur à fournir avec la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="3ac09-113">To start a single timer event, call the [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) function, specifying the amount of time before the callback occurs, the resolution, the address of the callback function (see [**TimeProc**](/previous-versions//dd757631(v=vs.85))), and the user data to supply with the callback function.</span></span> <span data-ttu-id="3ac09-114">Une application peut utiliser une fonction comme celle qui suit pour démarrer un événement à minuterie unique.</span><span class="sxs-lookup"><span data-stu-id="3ac09-114">An application can use a function like the following to start a single timer event.</span></span>


```C++
UINT SetTimerCallback(NPSEQ npSeq,  // sequencer data
    UINT msInterval)                // event interval
{ 
    npSeq->wTimerID = timeSetEvent(
        msInterval,                    // delay
        wTimerRes,                     // resolution (global variable)
        OneShotCallback,               // callback function
        (DWORD)npSeq,                  // user data
        TIME_ONESHOT );                // single timer event
    if(! npSeq->wTimerID)
        return ERR_TIMER;
    else
        return ERR_NOERROR;
} 

```



<span data-ttu-id="3ac09-115">Pour obtenir un exemple de la fonction de rappel OneShotCallback, consultez [écriture d’une fonction de rappel de minuterie](writing-a-timer-callback-function.md).</span><span class="sxs-lookup"><span data-stu-id="3ac09-115">For an example of the callback function OneShotCallback, see [Writing a Timer Callback Function](writing-a-timer-callback-function.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ac09-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3ac09-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ac09-117">Utilisation de minuteurs multimédias</span><span class="sxs-lookup"><span data-stu-id="3ac09-117">Using Multimedia Timers</span></span>](using-multimedia-timers.md)
</dt> </dl>

 

 