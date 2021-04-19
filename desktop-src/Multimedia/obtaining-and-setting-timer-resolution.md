---
title: Obtention et définition de la résolution de la minuterie
description: Obtention et définition de la résolution de la minuterie
ms.assetid: 237a6770-89b9-4922-b9e9-0e0bf3e0c9b6
keywords:
- minuteurs multimédias, résolution
- minuteries, résolution
- résolution minimale de la minuterie
- résolution maximale de la minuterie
- minuteurs multimédias, résolution maximale
- minuteries, résolution maximale
- minuteurs multimédias, résolution minimale
- minuteries, résolution minimale
- timeGetDevCaps fonction)
- timeBeginPeriod fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af5feca59e6fb4c528d6042b00eb7aa23263245c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106517950"
---
# <a name="obtaining-and-setting-timer-resolution"></a><span data-ttu-id="99d85-113">Obtention et définition de la résolution de la minuterie</span><span class="sxs-lookup"><span data-stu-id="99d85-113">Obtaining and Setting Timer Resolution</span></span>

<span data-ttu-id="99d85-114">L’exemple suivant appelle la fonction [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) pour déterminer les résolutions minimale et maximale des minuteries prises en charge par les services du minuteur.</span><span class="sxs-lookup"><span data-stu-id="99d85-114">The following example calls the [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) function to determine the minimum and maximum timer resolutions supported by the timer services.</span></span> <span data-ttu-id="99d85-115">Avant de configurer des événements de minuteur, l’exemple établit la résolution de minuteur minimale à l’aide de la fonction [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) .</span><span class="sxs-lookup"><span data-stu-id="99d85-115">Before it sets up any timer events, the example establishes the minimum timer resolution by using the [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) function.</span></span>


```C++
#define TARGET_RESOLUTION 1         // 1-millisecond target resolution

TIMECAPS tc;
UINT     wTimerRes;

if (timeGetDevCaps(&tc, sizeof(TIMECAPS)) != TIMERR_NOERROR) 
{
    // Error; application can't continue.
}

wTimerRes = min(max(tc.wPeriodMin, TARGET_RESOLUTION), tc.wPeriodMax);
timeBeginPeriod(wTimerRes); 
```



## <a name="related-topics"></a><span data-ttu-id="99d85-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="99d85-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99d85-117">Utilisation de minuteurs multimédias</span><span class="sxs-lookup"><span data-stu-id="99d85-117">Using Multimedia Timers</span></span>](using-multimedia-timers.md)
</dt> </dl>

 

 




