---
title: earlydepthstencil
description: Force le test des stencils de profondeur avant l’exécution d’un nuanceur.
ms.assetid: f8a9fee7-4a8a-4a34-bf7c-56906592caac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ed108d4f8e9d8d719d36fc859d5cc01a2317db4756bfbc6b0a548b669d9ca025
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986169"
---
# <a name="earlydepthstencil"></a>earlydepthstencil

Force le test des stencils de profondeur avant l’exécution d’un nuanceur.


```
earlydepthstencil   
```



## <a name="remarks"></a>Remarques

Le test des stencils de profondeur est normalement effectué lors du traitement des pixels par un nuanceur de pixels. En forçant le test des stencils à profondeur précoce, le test est effectué avant l’exécution du nuanceur. l’objectif est d’améliorer les performances par pixel en éliminant/réduisant/évitant le traitement des pixels inutiles.

Une application peut forcer le test des stencils de profondeur précoce en fournissant l’attribut ou le matériel peut exécuter des tests de stencil de profondeur à condition qu’aucune valeur de profondeur ne soit écrite et qu’aucune opération d’accès non triée ne soit exécutée dans un nuanceur en tant qu’optimisation.

Cet attribut est pris en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attributs du modèle de nuanceur 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




