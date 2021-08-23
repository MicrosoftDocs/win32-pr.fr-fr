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
ms.openlocfilehash: d7f9f81fdedae0fc6f6aa0448e6771c331af9c0d8924ab0f091d281565e4cfa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850879"
---
# <a name="intersection-shader"></a>Nuanceur d’intersection

Nuanceur utilisé pour implémenter des primitives d’intersection personnalisées pour les rayons qui croisent un volume englobant associé (cadre englobant). 

Le nuanceur d’intersection n’a pas accès à la charge utile de rayon, mais définit les attributs d’intersection pour chaque accès via un appel à [**ReportHit**](reporthit-function.md).  La gestion des **ReportHit** peut arrêter le nuanceur d’intersection tôt si l’indicateur Ray drapeau **ray \_ \_ accepte \_ First \_ HIT_ \AND \_ \END \_ Search** est défini, ou [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md) est appelé à partir d’un nuanceur de correspondance.  Sinon, elle retourne true si l’accès a été accepté ou false si l’accès a été rejeté.  Cela signifie qu’un nuanceur de correspondance, le cas échéant, doit s’exécuter avant que le contrôle ne retourne de manière conditionnelle au nuanceur d’intersection.

## <a name="shader-type-attribute"></a>Attribut de type Shader


```
[shader("intersection")]
```



## <a name="example"></a>Exemple

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

 

 




