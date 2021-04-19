---
description: Nuanceur qui appelle TraceRay pour générer des rayons.
ms.assetid: ''
title: Nuanceur de création de rayon
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
ms.openlocfilehash: 75d67293e489eee0f1d100002965c017de7c682c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515580"
---
# <a name="ray-generation-shader"></a><span data-ttu-id="13dd6-103">Nuanceur de création de rayon</span><span class="sxs-lookup"><span data-stu-id="13dd6-103">Ray Generation Shader</span></span>

<span data-ttu-id="13dd6-104">Nuanceur qui appelle [**TraceRay**](traceray-function.md) pour générer des rayons.</span><span class="sxs-lookup"><span data-stu-id="13dd6-104">A shader that calls [**TraceRay**](traceray-function.md) to generate rays.</span></span> <span data-ttu-id="13dd6-105">La charge utile de rayon initiale définie par l’utilisateur pour chaque rayon est fournie au site d’appel **TraceRay** .</span><span class="sxs-lookup"><span data-stu-id="13dd6-105">The initial user-defined ray payload for each ray is provided to the **TraceRay** call site.</span></span>  <span data-ttu-id="13dd6-106">[**CallShader**](callshader-function.md) peut également être utilisé dans les nuanceurs de génération de rayon pour appeler des [nuanceurs pouvant](callable-shader.md)être appelés.</span><span class="sxs-lookup"><span data-stu-id="13dd6-106">[**CallShader**](callshader-function.md) may also be used in ray generation shaders to invoke [callable shaders](callable-shader.md).</span></span>

<span data-ttu-id="13dd6-107">**DispatchRays** appelle une grille d’appels de nuanceur de génération de rayon.</span><span class="sxs-lookup"><span data-stu-id="13dd6-107">**DispatchRays** invokes a grid of ray generation shader invocations.</span></span>  <span data-ttu-id="13dd6-108">Chaque appel (thread) d’un nuanceur de Ray connaît son emplacement dans la grille globale, peut générer des rayons arbitraires via [**TraceRay**](traceray-function.md)et fonctionne indépendamment d’autres appels.</span><span class="sxs-lookup"><span data-stu-id="13dd6-108">Each invocation (thread) of a ray generation shader knows its location in the overall grid, can generate arbitrary rays via [**TraceRay**](traceray-function.md), and operates independently of other invocations.</span></span> <span data-ttu-id="13dd6-109">Il n’existe aucun ordre défini d’exécution des threads par rapport à l’autre.</span><span class="sxs-lookup"><span data-stu-id="13dd6-109">There is no defined order of execution of threads with respect to each other.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="13dd6-110">Attribut de type Shader</span><span class="sxs-lookup"><span data-stu-id="13dd6-110">Shader Type attribute</span></span>


```
[shader("raygeneration")]
```



## <a name="example"></a><span data-ttu-id="13dd6-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="13dd6-111">Example</span></span>

```
struct SceneConstantStructure { ... };
ConstantBuffer<SceneConstantStructure> SceneConstants;
RaytracingAccelerationStructure MyAccelerationStructure : register(t3);
struct MyPayload { ... };

[shader("raygeneration")]
void raygen_main()
{
    RayDesc myRay = {
        SceneConstants.CameraOrigin,
        SceneConstants.TMin,
        computeRayDirection(SceneConstants.LensParams, DispatchRaysIndex(), 
                            DispatchRaysDimensions()),
        SceneConstants.TMax};
    MyPayload payload = { ... };    // init payload
    TraceRay(
        MyAccelerationStructure,
        SceneConstants.RayFlags,
        SceneConstants.InstanceInclusionMask,
        SceneConstants.RayContributionToHitGroupIndex,
        SceneConstants.MultiplierForGeometryContributionToHitGroupIndex,
        SceneConstants.MissShaderIndex,
        myRay,
        payload);
    WriteFinalPixel(DispatchRaysIndex(), payload);
}
```

 

 




