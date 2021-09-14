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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012915"
---
# <a name="ray-generation-shader"></a>Nuanceur de création de rayon

Nuanceur qui appelle [**TraceRay**](traceray-function.md) pour générer des rayons. La charge utile de rayon initiale définie par l’utilisateur pour chaque rayon est fournie au site d’appel **TraceRay** .  [**CallShader**](callshader-function.md) peut également être utilisé dans les nuanceurs de génération de rayon pour appeler des [nuanceurs pouvant](callable-shader.md)être appelés.

**DispatchRays** appelle une grille d’appels de nuanceur de génération de rayon.  Chaque appel (thread) d’un nuanceur de Ray connaît son emplacement dans la grille globale, peut générer des rayons arbitraires via [**TraceRay**](traceray-function.md)et fonctionne indépendamment d’autres appels. Il n’existe aucun ordre défini d’exécution des threads par rapport à l’autre.

## <a name="shader-type-attribute"></a>Attribut de type Shader


```
[shader("raygeneration")]
```



## <a name="example"></a>Exemple

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

 

 




