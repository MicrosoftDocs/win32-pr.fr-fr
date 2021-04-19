---
description: Nuanceur utilisé pour implémenter des primitives d’intersection personnalisées pour les rayons qui croisent un volume englobant associé (cadre englobant).
ms.assetid: ''
title: Nuanceur d’intersection
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
ms.openlocfilehash: f20d9ceb90b716ca5e5c04fb796a8b20f535825d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514952"
---
# <a name="intersection-shader"></a><span data-ttu-id="cc2e4-103">Nuanceur d’intersection</span><span class="sxs-lookup"><span data-stu-id="cc2e4-103">Intersection Shader</span></span>

<span data-ttu-id="cc2e4-104">Nuanceur utilisé pour implémenter des primitives d’intersection personnalisées pour les rayons qui croisent un volume englobant associé (cadre englobant).</span><span class="sxs-lookup"><span data-stu-id="cc2e4-104">A shader that is used to implement custom intersection primitives for rays intersecting an associated bounding volume (bounding box).</span></span> 

<span data-ttu-id="cc2e4-105">Le nuanceur d’intersection n’a pas accès à la charge utile de rayon, mais définit les attributs d’intersection pour chaque accès via un appel à [**ReportHit**](reporthit-function.md).</span><span class="sxs-lookup"><span data-stu-id="cc2e4-105">The intersection shader does not have access to the ray payload, but defines the intersection attributes for each hit through a call to [**ReportHit**](reporthit-function.md).</span></span>  <span data-ttu-id="cc2e4-106">La gestion des **ReportHit** peut arrêter le nuanceur d’intersection tôt si l’indicateur Ray drapeau **ray \_ \_ accepte \_ First \_ HIT_ \AND \_ \END \_ Search** est défini, ou [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md) est appelé à partir d’un nuanceur de correspondance.</span><span class="sxs-lookup"><span data-stu-id="cc2e4-106">The handling of **ReportHit** may stop the intersection shader early, if the ray flag **RAY\_FLAG\_ACCEPT\_FIRST\_HIT_\AND\_\END\_SEARCH** is set, or [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md) is called from an any hit shader.</span></span>  <span data-ttu-id="cc2e4-107">Sinon, elle retourne true si l’accès a été accepté ou false si l’accès a été rejeté.</span><span class="sxs-lookup"><span data-stu-id="cc2e4-107">Otherwise, it returns true if the hit was accepted or false if the hit was rejected.</span></span>  <span data-ttu-id="cc2e4-108">Cela signifie qu’un nuanceur de correspondance, le cas échéant, doit s’exécuter avant que le contrôle ne retourne de manière conditionnelle au nuanceur d’intersection.</span><span class="sxs-lookup"><span data-stu-id="cc2e4-108">This means that an any hit shader, if present, must execute before control conditionally returns to the intersection shader.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="cc2e4-109">Attribut de type Shader</span><span class="sxs-lookup"><span data-stu-id="cc2e4-109">Shader Type attribute</span></span>


```
[shader("intersection")]
```



## <a name="example"></a><span data-ttu-id="cc2e4-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="cc2e4-110">Example</span></span>

```
struct CustomPrimitiveDef { ... };
struct MyAttributes { ... };
struct CustomIntersectionIterator {...};
void InitCustomIntersectionIterator(CustomIntersectionIterator it) {...}
bool IntersectCustomPrimitiveFrontToBack(
    CustomPrimitiveDef prim,
    inout CustomIntersectionIterator it,
    float3 origin, float3 dir,
    float rayTMin, inout float curT,
    out MyAttributes attr);

[shader("intersection")]
void intersection_main()
{
    float THit = RayTCurrent();
    MyAttributes attr;
    CustomIntersectionIterator it;
    InitCustomIntersectionIterator(it); 
    while(IntersectCustomPrimitiveFrontToBack(
            CustomPrimitiveDefinitions[LocalConstants.PrimitiveIndex],
            it, ObjectRayOrigin(), ObjectRayDirection(), 
            RayTMin(), THit, attr))
    {
        // Exit on the first hit.  Note that if the ray has
        // RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH or an
        // anyhit shader is used and calls AcceptHitAndEndSearch(),
        // that would also fully exit this intersection shader (making
        // the “break” below moot in that case).        
        if (ReportHit(THit, /*hitKind*/ 0, attr) && (RayFlags() &  RAY_FLAG_FORCE_OPAQUE))
            break;
    }
}
```

 

 




