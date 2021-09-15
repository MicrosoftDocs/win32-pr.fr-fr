---
description: Nuanceur appelé lorsqu’il est activé et que l’accès le plus proche a été déterminé ou que la recherche d’intersection de rayon s’est terminée.
ms.assetid: ''
title: Nuanceur de correspondance le plus proche
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: 347ad66dce0a81b929d5dc3c82051bf84226e723
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521761"
---
# <a name="closest-hit-shader"></a>Nuanceur de correspondance le plus proche

Nuanceur appelé lorsqu’il est activé et que l’accès le plus proche a été déterminé ou que la recherche d’intersection de rayon s’est terminée. Ce nuanceur est l’endroit où l’ombrage de surface et la génération de rayons supplémentaires se produisent généralement.  Les nuanceurs atteints les plus proches doivent déclarer un paramètre de charge utile, suivi d’un paramètre d’attributs.  Chaque doit être un type de structure défini par l’utilisateur correspondant aux types utilisés pour [**TraceRay**](traceray-function.md) et [**ReportHit**](reporthit-function.md) respectivement, ou la [**structure d’attributs d’intersection**](intersection-attributes.md) quand l’intersection de triangle de fonction fixe est utilisée.

## <a name="shader-type-attribute"></a>Attribut de type Shader


```
[shader("closesthit")]
```



## <a name="example"></a>Exemple

```
[shader("closesthit")]
void closesthit_main(inout MyPayload payload, in MyAttributes attr)
{
    CallShader( ... );  // maybe
    // update payload for surface
    // trace reflection
    float3 worldRayOrigin = WorldRayOrigin() + WorldRayDirection() * RayTCurrent();
    float3 worldNormal = mul(attr.normal, (float3x3)ObjectToWorld3x4());
    RayDesc reflectedRay = { worldRayOrigin, SceneConstants.Epsilon,
                             ReflectRay(WorldRayDirection(), worldNormal),
                             SceneConstants.TMax };
    TraceRay(MyAccelerationStructure,
             SceneConstants.RayFlags,
             SceneConstants.InstanceInclusionMask,
             SceneConstants.RayContributionToHitGroupIndex,
             SceneConstants.MultiplierForGeometryContributionToHitGroupIndex,
             SceneConstants.MissShaderIndex,
             reflectedRay,
             payload);
    // Combine final contributions into ray payload
    // this ray query is now complete.
    // Alternately, could look at data in payload result based on that make other TraceRay
    // calls.  No constraints on the code structure.
}

```

 

 




