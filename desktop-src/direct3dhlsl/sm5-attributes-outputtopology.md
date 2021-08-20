---
title: outputtopology
description: Définit le type de la primitive de sortie pour le du paveur.
ms.assetid: 4aba65e5-b005-43fd-a844-c7fbb1b7406c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8d718b11c23fcf77f452e224a51439f7d6f422d3c81d5238167cbf87c7c3014a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725413"
---
# <a name="outputtopology"></a>outputtopology

Définit le type de la primitive de sortie pour le du paveur.


```
outputtopology(X)      
```



## <a name="remarks"></a>Remarques

X doit être un [**point**](dx-graphics-hlsl-geometry-shader.md), une **ligne**, un **triangle \_** ou un **rectangle \_ CCW** et doit être placé entre guillemets. Voici les options valides pour cet attribut :


```
[outputtopology("point")]
[outputtopology("line")]
[outputtopology("triangle_cw")]
[outputtopology("triangle_ccw")]
```



Cet attribut est pris en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attributs du modèle de nuanceur 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




