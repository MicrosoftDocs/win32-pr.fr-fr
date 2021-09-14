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
ms.openlocfilehash: 00db0eb46e8c011e5b31f773679e19ca6dd4a7a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012906"
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

 

 




