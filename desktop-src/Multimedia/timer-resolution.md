---
title: Résolution de la minuterie
description: Résolution de la minuterie
ms.assetid: 2e5e94fe-8175-417f-8c59-9d5cf052ea89
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
- timeEndPeriod fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e96f1b410f2e18203af794ea124bb6b83bccce
ms.sourcegitcommit: a0b531d335bc691100149830b256d5af7e136c24
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/28/2019
ms.locfileid: "103670861"
---
# <a name="timer-resolution"></a><span data-ttu-id="0c634-114">Résolution de la minuterie</span><span class="sxs-lookup"><span data-stu-id="0c634-114">Timer Resolution</span></span>

<span data-ttu-id="0c634-115">Pour déterminer les résolutions minimale et maximale des minuteries prises en charge par les services du minuteur, utilisez la fonction [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="0c634-115">To determine the minimum and maximum timer resolutions supported by the timer services, use the [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) function.</span></span> <span data-ttu-id="0c634-116">Cette fonction remplit les membres **wPeriodMin** et **wPeriodMax** de la structure [**TIMECAPS**](/windows/desktop/api/TimeAPI/ns-timeapi-timecaps) avec les résolutions minimale et maximale.</span><span class="sxs-lookup"><span data-stu-id="0c634-116">This function fills the **wPeriodMin** and **wPeriodMax** members of the [**TIMECAPS**](/windows/desktop/api/TimeAPI/ns-timeapi-timecaps) structure with the minimum and maximum resolutions.</span></span> <span data-ttu-id="0c634-117">Cette plage peut varier entre les ordinateurs et les plateformes Windows.</span><span class="sxs-lookup"><span data-stu-id="0c634-117">This range can vary across computers and Windows platforms.</span></span>

<span data-ttu-id="0c634-118">Une fois que vous avez déterminé les résolutions minimale et maximale disponibles du minuteur, vous devez définir la résolution minimale que votre application doit utiliser.</span><span class="sxs-lookup"><span data-stu-id="0c634-118">After you determine the minimum and maximum available timer resolutions, you must establish the minimum resolution you want your application to use.</span></span> <span data-ttu-id="0c634-119">Utilisez les fonctions [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) et [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod) pour définir et effacer cette résolution.</span><span class="sxs-lookup"><span data-stu-id="0c634-119">Use the [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) and [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod) functions to set and clear this resolution.</span></span> <span data-ttu-id="0c634-120">Vous devez faire correspondre chaque appel à **timeBeginPeriod** avec un appel à **timeEndPeriod**, en spécifiant la même résolution minimale dans les deux appels.</span><span class="sxs-lookup"><span data-stu-id="0c634-120">You must match each call to **timeBeginPeriod** with a call to **timeEndPeriod**, specifying the same minimum resolution in both calls.</span></span> <span data-ttu-id="0c634-121">Une application peut effectuer plusieurs appels **timeBeginPeriod** , à condition que chaque appel corresponde à un appel à **timeEndPeriod**.</span><span class="sxs-lookup"><span data-stu-id="0c634-121">An application can make multiple **timeBeginPeriod** calls, as long as each call is matched with a call to **timeEndPeriod**.</span></span>

<span data-ttu-id="0c634-122">Dans [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) et [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod), le paramètre *uPeriod* indique la résolution de minuteur minimale, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="0c634-122">In both [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) and [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod), the *uPeriod* parameter indicates the minimum timer resolution, in milliseconds.</span></span> <span data-ttu-id="0c634-123">Vous pouvez spécifier n’importe quelle valeur de résolution de la minuterie dans la plage prise en charge par la minuterie.</span><span class="sxs-lookup"><span data-stu-id="0c634-123">You can specify any timer resolution value within the range supported by the timer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c634-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0c634-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c634-125">À propos des minuteurs multimédias</span><span class="sxs-lookup"><span data-stu-id="0c634-125">About Multimedia Timers</span></span>](about-multimedia-timers.md)
</dt> </dl>

 

 




