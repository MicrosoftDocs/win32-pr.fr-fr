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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119589"
---
# <a name="obtaining-and-setting-timer-resolution"></a>Obtention et définition de la résolution de la minuterie

L’exemple suivant appelle la fonction [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) pour déterminer les résolutions minimale et maximale des minuteries prises en charge par les services du minuteur. Avant de configurer des événements de minuteur, l’exemple établit la résolution de minuteur minimale à l’aide de la fonction [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) .


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de minuteurs multimédias](using-multimedia-timers.md)
</dt> </dl>

 

 




