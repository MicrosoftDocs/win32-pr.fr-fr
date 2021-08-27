---
description: Composition
ms.assetid: b5f607b2-9cca-4eef-9c63-d2015bd10469
title: Composition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f5973b478f442187645fbd73e8fca88ebfe71f247aea0e9065356583b6748ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084279"
---
# <a name="composition"></a>Composition

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

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

 

 



