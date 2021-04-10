---
description: Définit un correctif de \# contrôle p&233 ;. Le tableau définit les points de contrôle pour le correctif.
ms.assetid: vs|directx_sdk|~\patch.htm
title: Correctif
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 480457b3dd3800aca8b23210e3fe653b4e713e94
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845738"
---
# <a name="patch"></a>Correctif

Définit un correctif de contrôle de Bézier. Le tableau définit les points de contrôle pour le correctif.

``` syntax
template Patch
{
    < A3EB5D44-FC22-429D-9AFB-3221CB9719A6 >
    DWORD nControlIndices;
    array DWORD controlIndices[nControlIndices];
} 
```

Où :

-   nControlIndices : nombre d’index du point de contrôle.
-   Tableau DWORD controlIndices \[ nControlIndices \] -tableau d’index du point de contrôle.

Le type de correctif est défini par le nombre de points de contrôle, comme indiqué dans le tableau suivant.



| Nombre de points de contrôle | Type                              |
|--------------------------|-----------------------------------|
| 10                       | Correctif triangulaire de la Bézier cubique     |
| 15                       | Correctif triangulaire de Bézier quart   |
| 16                       | Correctif du rectangle à quatre rectangles de Bézier cubique |



 

L’ordre des points de contrôle est indiqué dans un motif en spirale, comme indiqué dans les diagrammes suivants pour les correctifs triangulaires et rectangulaires.

Les correctifs triangulaires utilisent le modèle suivant.

![diagramme du modèle pour les correctifs triangulaires](images/tripatch.png)

Les correctifs rectangulaires utilisent le modèle suivant.

![diagramme du modèle pour les correctifs rectangulaires](images/quadpatch.png)

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Modèles](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



