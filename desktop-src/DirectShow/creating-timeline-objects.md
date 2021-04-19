---
description: Création d’objets Timeline
ms.assetid: fb369b32-a54b-4d8a-8358-5f05aa48f853
title: Création d’objets Timeline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929fffb6a953e198b6e7ed9b17250d45e84f7932
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106536094"
---
# <a name="creating-timeline-objects"></a>Création d’objets Timeline

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

L’exemple de code présenté dans cet article commence par une chronologie vide, mais les mêmes étapes s’appliquent si vous chargez un projet existant et souhaitez y ajouter des objets.

Pour créer tout type d’objet dans la chronologie, appelez la méthode [**IAMTimeline :: CreateEmptyNode**](iamtimeline-createemptynode.md) . Par exemple, le code suivant crée un nouveau groupe :


```C++
IAMTimelineObj *pGroupObj = NULL;
pTL->CreateEmptyNode(&pGroupObj, TIMELINE_MAJOR_TYPE_GROUP);
```



Le deuxième paramètre est un membre de l’énumération de [**\_ \_ type principal**](timeline-major-type.md) de la chronologie. Elle spécifie le type d’objet de chronologie à créer, tel qu’un groupe ou une piste.

La méthode **CreateEmptyNode** crée l’objet et retourne un pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de l’objet. Il incrémente également le nombre de références sur l’interface **IAMTimelineObj** . vous devez donc libérer l’interface lorsque vous avez fini de l’utiliser. N’appelez pas la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) . Au lieu de cela, utilisez toujours **CreateEmptyNode** pour créer un objet Timeline, car il initialise le nouvel objet pour une utilisation dans une chronologie.

L’interface [**IAMTimelineObj**](iamtimelineobj.md) est une interface générique. Il fournit des méthodes qui sont communes à tous les types d’objets Timeline. Chaque type d’objet expose également d’autres interfaces. Par exemple, les groupes exposent l’interface [**IAMTimelineGroup**](iamtimelinegroup.md) , entre autres. Vous pouvez obtenir des pointeurs vers les autres interfaces en appelant **QueryInterface**.

Une fois que vous avez créé un objet, il ne fait pas encore partie de la chronologie. La méthode pour ajouter un objet à la chronologie dépend du type d’objet. La section suivante décrit comment ajouter des groupes, des compositions et des suivis à la chronologie.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Construction d’une chronologie](constructing-a-timeline.md)
</dt> </dl>

 

 
