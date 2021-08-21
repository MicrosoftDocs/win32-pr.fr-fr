---
description: Objets Timeline
ms.assetid: da426964-d5bd-45ca-a914-c19062f3564b
title: Objets Timeline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbcf3496770dee7664e08ffabe6537356c7b37ad13abee1dce149698748745e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072303"
---
# <a name="timeline-objects"></a>Objets Timeline

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Chaque type d’objet dans la chronologie (source, suivi, effet, etc.) est un objet COM distinct. Toutefois, une application ne les crée pas à l’aide de la fonction **CoCreateInstance** . Au lieu de cela, il appelle la méthode [**IAMTimeline :: CreateEmptyNode**](iamtimeline-createemptynode.md) . Cette méthode crée un objet du type demandé, l’initialise et retourne un pointeur vers l’objet. Pour plus d’informations, consultez [construction d’une chronologie](constructing-a-timeline.md).

Chaque objet Timeline expose l’interface [**IAMTimelineObj**](iamtimelineobj.md) . En outre, les différents types d’objets prennent en charge leurs propres interfaces spécialisées :

-   Source : [ **IAMTimelineSrc**](iamtimelinesrc.md)
-   Suivi : [ **IAMTimelineTrack**](iamtimelinetrack.md)
-   Composition : [ **IAMTimelineComp**](iamtimelinecomp.md)
-   Groupe : [**IAMTimelineComp**](iamtimelinecomp.md), [**IAMTimelineGroup**](iamtimelinegroup.md)
-   Effet : [ **IAMTimelineEffect**](iamtimelineeffect.md)
-   Transition : [ **IAMTimelineTrans**](iamtimelinetrans.md)

Notez que les groupes sont un type de composition, donc ils prennent en charge [**IAMTimelineComp**](iamtimelinecomp.md), ainsi que leur propre interface [**IAMTimelineGroup**](iamtimelinegroup.md) .

Outre les interfaces listées précédemment, les objets Timeline exposent d’autres interfaces secondaires. Ces interfaces déterminent les relations entre les types d’objets.



| Interface                                                  | Signification                                                                                                       | Exposé par                        |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [**IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md) | L’objet est une piste virtuelle. Les pistes virtuelles peuvent résider dans les compositions et contenir d’autres objets Timeline. | Composition, suivi                |
| [**IAMTimelineEffectable**](iamtimelineeffectable.md)     | L’objet peut avoir des effets.                                                                                  | Composition, suivi, source        |
| [**IAMTimelineTransable**](iamtimelinetransable.md)       | L’objet peut avoir des transitions.                                                                              | Composition, suivi                |
| [**IAMTimelineSplittable**](iamtimelinesplittable.md)     | L’objet peut être fractionné en deux objets.                                                                     | Track, source, Effect, transition |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble des composants de la chronologie](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



