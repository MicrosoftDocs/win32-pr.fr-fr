---
description: Chronologie
ms.assetid: a3b8bff2-8593-483c-af49-a975ab2dc330
title: Chronologie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6ac73b84409629f63ad4be469edf6b943f9e64
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009993"
---
# <a name="the-timeline"></a>Chronologie

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

La chronologie expose l’interface [**IAMTimeline**](iamtimeline.md) . Cette interface contient des méthodes pour définir des propriétés sur la chronologie ; pour ajouter des groupes à la chronologie ; et pour créer des objets Timeline, tels que des groupes, des pistes et des sources. Pour créer une nouvelle chronologie, appelez la fonction **CoCreateInstance** standard comme suit :


```C++
IAMTimeline *pTL = NULL;
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
        IID_IAMTimeline, (void**)&pTL);
```



La Nouvelle chronologie est vide. à ce stade, vous pouvez charger un fichier projet existant (voir [chargement et aperçu d’un Project](loading-and-previewing-a-project.md)), ou développer la chronologie en créant et en insérant de nouveaux objets (consultez [construction d’une chronologie](constructing-a-timeline.md)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble des composants de la chronologie](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



