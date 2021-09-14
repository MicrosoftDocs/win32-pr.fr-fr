---
description: Passé à la fonction TraceRay pour définir l’origine, la direction et les étendues du rayon.
ms.assetid: ''
title: RayDesc, structure
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
ms.openlocfilehash: a5fd6e041fc476c24ff926c9c8f99f05699f5e41
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012909"
---
# <a name="raydesc-structure"></a>RayDesc, structure

Passé à la fonction [**TraceRay**](traceray-function.md) pour définir l’origine, la direction et les étendues du rayon.

## <a name="syntax"></a>Syntaxe


```
struct RayDesc
{
    float3 Origin;
    float  TMin;
    float3 Direction;
    float  TMax;
};

```



## <a name="fields"></a>Champs

<dl> <dt>

<span id="Origin"></span><span id="origin"></span>**Lancé**
</dt> <dd>

Origine du rayon.

</dd> <dt>

<span id="TMin"></span><span id="tmin"></span>**TMin**
</dt> <dd>

L’étendue minimale du rayon.


</dd> <dt>

<span id="Direction"></span><span id="direction"></span>**Direction**
</dt> <dd>

Direction du rayon.


</dd> <dt>

<span id="TMax"></span><span id="tmax"></span>**TMax**
</dt> <dd>

Étendue maximale du rayon.


</dd>

## <a name="requirements"></a>Spécifications



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence HLSL Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




