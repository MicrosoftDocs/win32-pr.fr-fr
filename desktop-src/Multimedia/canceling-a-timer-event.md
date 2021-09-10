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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364475"
---
# <a name="canceling-a-timer-event"></a>Annulation d’un événement de minuterie

> [!Note]  
> Cette rubrique décrit une fonction obsolète. Les nouvelles applications doivent utiliser la fonction [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) pour créer des minuteries.

 

Pour chaque minuteur périodique créant en appelant [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)), l’application doit annuler la minuterie en appelant la fonction [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) avant de libérer la mémoire qui contient la fonction de rappel. Pour annuler un événement de minuteur, il peut appeler la fonction suivante.


```C++
void DestroyTimer(NPSEQ npSeq)
{
    if(npSeq->wTimerID) {                // is timer event pending?
        timeKillEvent(npSeq->wTimerID);  // cancel the event
        npSeq->wTimerID = 0;
    }
} 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de minuteurs multimédias](using-multimedia-timers.md)
</dt> </dl>

 

 