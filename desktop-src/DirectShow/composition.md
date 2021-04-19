---
description: Composition
ms.assetid: b5f607b2-9cca-4eef-9c63-d2015bd10469
title: Composition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e030e02ab77ec54e1e340d72db7210665d649bfb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515120"
---
# <a name="composition"></a>Composition

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L’objet composition est un conteneur pour les pistes. Il peut également contenir d’autres compositions (pour l’imbrication des pistes), des effets et des transitions. Pour créer cet objet, appelez la méthode [**IAMTimeline :: CreateEmptyNode**](iamtimeline-createemptynode.md) .

L’objet composition expose les interfaces suivantes :

-   [**IAMTimelineComp**](iamtimelinecomp.md)
-   [**IAMTimelineEffectable**](iamtimelineeffectable.md)
-   [**IAMTimelineObj**](iamtimelineobj.md)
-   [**IAMTimelineTransable**](iamtimelinetransable.md)
-   [**IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèle de chronologie](the-timeline-model.md)
</dt> <dt>

[Construction d’une chronologie](constructing-a-timeline.md)
</dt> </dl>

 

 



