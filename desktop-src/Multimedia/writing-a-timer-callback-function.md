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
ms.openlocfilehash: f5b8680fc4d697c33514276276daaa2a4d75577bfbd78fa3caffc7f426ca9d70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891779"
---
# <a name="writing-a-timer-callback-function"></a>Écriture d’une fonction de rappel de minuterie

> [!Note]  
> Cette rubrique décrit une fonction obsolète. Les nouvelles applications doivent utiliser la fonction [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) pour créer des minuteries.

 

La fonction de rappel suivante, OneShotTimer, invalide l’identificateur pour l’événement de minuterie unique et appelle une routine de minuterie pour gérer les tâches spécifiques à l’application. Pour plus d’informations, consultez [**TimeProc**](/previous-versions//dd757631(v=vs.85)).


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de minuteurs multimédias](using-multimedia-timers.md)
</dt> </dl>

 

 