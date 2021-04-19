---
description: Valeur float représentant le point de terminaison paramétrique actuel pour le rayon.
ms.assetid: ''
title: RayTCurrent
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTCurrent
api_type:
- NA
ms.openlocfilehash: 4f090bab88c6be671ca0614255fd7bdebb0d1549
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515372"
---
# <a name="raytcurrent"></a>RayTCurrent

Valeur float représentant le point de terminaison paramétrique actuel pour le rayon.  

## <a name="syntax"></a>Syntaxe

```
float RayTCurrent();

```


## <a name="remarks"></a>Notes

**RayTCurrent** définit le point de terminaison actuel du rayon en fonction de la formule suivante : Origin + (direction * RayTCurrent).  L' *origine* et la *direction* peuvent être dans le monde ou dans l’espace d’objet, ce qui donne lieu à un point de terminaison de l’espace d’un monde ou d’un objet.

**RayTCurrent** est initialisé dans l’appel de [**TraceRay**](traceray-function.md) d’appel avec la valeur [**RayDesc :: Tmax**](raydesc.md) , puis est mis à jour pendant la requête de trace lorsque des intersections sont signalées (dans le cas échéant) et acceptées.

Dans le [nuanceur d’intersection](intersection-shader.md), il représente la distance à l’intersection la plus proche trouvée jusqu’à présent.  Il sera mis à jour après () à la valeur cela fournie si l’accès a été accepté.

Dans les [nuanceurs de présence](any-hit-shader.md), il représente la distance à laquelle l’intersection active est signalée.

Dans le [nuanceur de correspondance le plus proche](closest-hit-shader.md), il s’agit de la distance à laquelle l’intersection la plus proche est acceptée.

Dans le [nuanceur d’échecs](miss-shader.md), il est égal à *Tmax* passé à l’appel **TraceRay** .


Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants :

* [**Tout nuanceur de correspondance**](any-hit-shader.md)
* [**Nuanceur de correspondance le plus proche**](closest-hit-shader.md)
* [**Nuanceur d’intersection**](intersection-shader.md)
* [**Nuanceur manque**](miss-shader.md)





## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence HLSL Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




