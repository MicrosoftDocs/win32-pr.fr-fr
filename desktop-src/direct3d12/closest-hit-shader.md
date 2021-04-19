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
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544206"
---
# <a name="closest-hit-shader"></a><span data-ttu-id="af766-103">Nuanceur de correspondance le plus proche</span><span class="sxs-lookup"><span data-stu-id="af766-103">Closest Hit Shader</span></span>

<span data-ttu-id="af766-104">Nuanceur appelé lorsqu’il est activé et que l’accès le plus proche a été déterminé ou que la recherche d’intersection de rayon s’est terminée.</span><span class="sxs-lookup"><span data-stu-id="af766-104">A shader that is invoked when it is enabled and the closest hit has been determined or ray intersection search ended.</span></span> <span data-ttu-id="af766-105">Ce nuanceur est l’endroit où l’ombrage de surface et la génération de rayons supplémentaires se produisent généralement.</span><span class="sxs-lookup"><span data-stu-id="af766-105">This shader is where surface shading and additional ray generation will typically occur.</span></span>  <span data-ttu-id="af766-106">Les nuanceurs atteints les plus proches doivent déclarer un paramètre de charge utile, suivi d’un paramètre d’attributs.</span><span class="sxs-lookup"><span data-stu-id="af766-106">Closest hit shaders must declare a payload parameter, followed by an attributes parameter.</span></span>  <span data-ttu-id="af766-107">Chaque doit être un type de structure défini par l’utilisateur correspondant aux types utilisés pour [**TraceRay**](traceray-function.md) et [**ReportHit**](reporthit-function.md) respectivement, ou la [**structure d’attributs d’intersection**](intersection-attributes.md) quand l’intersection de triangle de fonction fixe est utilisée.</span><span class="sxs-lookup"><span data-stu-id="af766-107">Each must be a user-defined structure type matching types used for [**TraceRay**](traceray-function.md) and [**ReportHit**](reporthit-function.md) respectively, or the [**Intersection Attributes Structure**](intersection-attributes.md) when fixed-function triangle intersection is used.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="af766-108">Attribut de type Shader</span><span class="sxs-lookup"><span data-stu-id="af766-108">Shader Type attribute</span></span>


```
[shader("closesthit")]
```



## <a name="example"></a><span data-ttu-id="af766-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="af766-109">Example</span></span>

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

 

 




