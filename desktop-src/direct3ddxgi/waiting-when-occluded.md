---
description: Les applications peuvent attendre un événement lorsque le rendu à l’écran est inutile (c’est-à-dire, alors qu’ils sont bloqués).
ms.assetid: B9EC23C9-A311-4BD9-BBE8-908A1334A541
title: En attente d’un événement lorsque le rendu est inutile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b553ef52e812c5117e5d9669ba13b47b9f4280c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106519173"
---
# <a name="waiting-on-an-event-when-rendering-is-unnecessary"></a>En attente d’un événement lorsque le rendu est inutile

Les applications peuvent attendre un événement lorsque le rendu à l’écran est inutile (c’est-à-dire, alors qu’ils sont bloqués). Lorsque le Gestionnaire de fenêtrage (DWM) ou une application est bloqués, aucun rendu n’est nécessaire et le système d’exploitation peut rester dans des États d’alimentation inférieurs pendant des périodes plus longues. Cela économise de l’énergie et augmente la durée de vie de la batterie.

Une application peut attendre un événement dans les cas suivants :

-   Toutes les analyses sont désactivées.
-   La session dans laquelle l’application s’exécute est déconnectée.
-   L’application s’exécute en mode plein écran exclusivement sur une configuration de moniteur unique.
-   L’application s’exécute sur un bureau autre que le bureau actif et n’est pas autorisée à effectuer un rendu sur le bureau actif.

Le système d’exploitation déclenche l’événement lorsque l’application peut effectuer un rendu à nouveau. L’événement n’est pas effacé au cours d’une mise à niveau du pilote, ou de la procession de détection et de récupération du délai d’attente (TDR). Toutefois, il est effacé lorsque la nouvelle carte et les moniteurs deviennent actifs.

Si vous souhaitez que votre application soit avertie des modifications de l’état d’occlusion, l’application doit s’inscrire pour ces modifications. Une application peut s’inscrire pour être avertie des modifications de l’état d’occlusion par le biais d’un message dans une fenêtre ou par le biais d’une signalisation d’événement. Pour s’inscrire afin de recevoir des messages de notification dans une fenêtre sur les modifications de l’état d’occlusion, une application appelle la méthode [**IDXGIFactory2 :: RegisterOcclusionStatusWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow) . Pour s’inscrire afin de recevoir la notification des modifications d’état d’occlusion via la signalisation d’événement, une application appelle la méthode [**IDXGIFactory2 :: RegisterOcclusionStatusEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent) . Les deux méthodes retournent un pointeur vers une valeur de clé que l’application peut utiliser pour annuler l’inscription de la notification. Pour annuler l’inscription de la notification, l’application passe cette valeur de clé à la méthode [**IDXGIFactory2 :: UnregisterOcclusionStatus**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Améliorations de DXGI 1,2](dxgi-1-2-improvements.md)
</dt> </dl>

 

 



