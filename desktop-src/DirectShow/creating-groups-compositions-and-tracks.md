---
description: Création de groupes de compositions et de pistes
ms.assetid: c3bef3cd-5e3c-42c5-850f-b4cb00c414bd
title: Création de groupes de compositions et de pistes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d0fa9812c3f7219882cc93be14f7ff4c0b1a8ae39f96d6798bdc93705cda8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908529"
---
# <a name="creating-groups-compositions-and-tracks"></a>Création de groupes de compositions et de pistes

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Les groupes, les compositions et les suivis sont les couches intermédiaires entre la chronologie et les éléments sources. Ils se distinguent par le type d’objet qu’ils peuvent contenir.

-   Les suivis contiennent des objets sources.
-   Les compositions contiennent des pistes et d’autres compositions, mais pas des objets sources.
-   Les groupes sont des compositions de niveau supérieur. Les groupes contiennent des compositions et des pistes, mais les compositions ne peuvent pas contenir de groupes.
-   Une *piste virtuelle* est un objet qui peut résider dans une composition ou un groupe. Cela comprend les pistes et les compositions.

Ces objets exposent les interfaces suivantes :



| Interface                                                  | Exposé par           |
|------------------------------------------------------------|----------------------|
| [**IAMTimelineTrack**](iamtimelinetrack.md)               | Pistes               |
| [**IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md) | Pistes, compositions |
| [**IAMTimelineComp**](iamtimelinecomp.md)                 | Compositions, groupes |
| [**IAMTimelineGroup**](iamtimelinegroup.md)               | Groupes               |



 

Ces interfaces contiennent les méthodes permettant d’ajouter des objets à la chronologie.

-   [**IAMTimeline :: addgroup**](iamtimeline-addgroup.md): insère un groupe dans la chronologie.
-   [**IAMTimelineComp :: VTrackInsBefore**](iamtimelinecomp-vtrackinsbefore.md): insère une piste virtuelle dans une composition ou un groupe.
-   [**IAMTimelineTrack :: SrcAdd**](iamtimelinetrack-srcadd.md): insère une source dans une piste.

Par exemple, le code suivant insère une nouvelle piste dans un groupe. Comme indiqué dans le tableau précédent, un groupe est considéré comme un type de composition, et une piste est un type de piste virtuelle. Par conséquent, pour insérer la piste dans le groupe, vous devez interroger le groupe pour son interface **IAMTimelineComp** et appeler la méthode **IAMTimelineComp :: VTrackInsBefore** .


```C++
IAMTimelineGroup    *pGroup;
// Create a new group (not shown). 

IAMTimelineComp     *pComp = NULL;
IAMTimelineObj      *pTrackObj = NULL;

pTL->CreateEmptyNode(&pTrackObj, TIMELINE_MAJOR_TYPE_TRACK);
pGroup->QueryInterface(IID_IAMTimelineComp, (void **)&pComp);
pComp->VTrackInsBefore(pTrackObj, 0);
```



Le deuxième paramètre de **VTrackInsBefore** spécifie la priorité de la piste virtuelle. Les niveaux de priorité commencent à zéro. Si vous spécifiez la valeur – 1, la piste virtuelle est insérée à la fin de la liste de priorité. Si vous spécifiez une valeur alors qu’il existe déjà une piste virtuelle, tout ce qui suit descend dans la liste d’un niveau de priorité. N’insérez pas une piste virtuelle à une priorité supérieure au nombre de pistes virtuelles, car elle entraîne un comportement indéfini.

Pour supprimer définitivement un objet de la chronologie, appelez [**IAMTimelineObj :: RemoveAll**](iamtimelineobj-removeall.md) sur l’objet. Cette méthode supprime l’objet et tous ses enfants. Pour supprimer un objet en vue de le réinsérer ailleurs dans la chronologie, appelez [**IAMTimelineObj :: Remove**](iamtimelineobj-remove.md) à la place. Contrairement à **RemoveAll**, cette méthode ne supprime pas les enfants de l’objet. Pour tout supprimer de la chronologie, appelez [**IAMTimeline :: ClearAllGroups**](iamtimeline-clearallgroups.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Construction d’une chronologie](constructing-a-timeline.md)
</dt> </dl>

 

 



