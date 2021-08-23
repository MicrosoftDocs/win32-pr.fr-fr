---
description: Valeur float représentant le point de départ paramétrique actuel pour le rayon.
ms.assetid: ''
title: RayTMin
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTMin
api_type:
- NA
ms.openlocfilehash: 5429574480cfda071dfec93cea771211bab578bdaecb4513c76f43c4d820b22b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989479"
---
# <a name="raytmin"></a>RayTMin

Valeur float représentant le point de départ paramétrique actuel pour le rayon. 

## <a name="syntax"></a>Syntaxe

```
float RayTMin();

```

## <a name="remarks"></a>Notes

**RayTMin** définit le point de départ du rayon en fonction de la formule suivante : Origin + (direction * RayTMin).  L' *origine* et la *direction* peuvent être dans le monde ou dans l’espace d’objet, ce qui se traduit par un point de départ ou un espace d’objet.

**RayTMin** est spécifié dans l’appel à [**TraceRay**](traceray-function.md)et est constant pour la durée de cet appel.




Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants :

* [**Tout nuanceur de correspondance**](any-hit-shader.md)
* [**Nuanceur de correspondance le plus proche**](closest-hit-shader.md)
* [**Nuanceur d’intersection**](intersection-shader.md)
* [**Nuanceur manque**](miss-shader.md)





## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence HLSL Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




