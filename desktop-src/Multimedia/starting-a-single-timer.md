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
# <a name="starting-a-single-timer-event"></a>Démarrage d’un événement de minuterie unique

> [!Note]  
> Cette rubrique décrit une fonction obsolète. Les nouvelles applications doivent utiliser la fonction [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) pour créer des minuteries.

 

Pour démarrer un événement à minuterie unique, appelez la fonction [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) , en spécifiant la durée avant le rappel, la résolution, l’adresse de la fonction de rappel (voir [**TimeProc**](/previous-versions//dd757631(v=vs.85))) et les données utilisateur à fournir avec la fonction de rappel. Une application peut utiliser une fonction comme celle qui suit pour démarrer un événement à minuterie unique.


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



Pour obtenir un exemple de la fonction de rappel OneShotCallback, consultez [écriture d’une fonction de rappel de minuterie](writing-a-timer-callback-function.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de minuteurs multimédias](using-multimedia-timers.md)
</dt> </dl>

 

 