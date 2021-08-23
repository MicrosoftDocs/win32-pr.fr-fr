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
ms.openlocfilehash: a4fa44e68e8747a0a8366ca2d949290f585d4b70d9e75b4ed2d3b6fdda0d05c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123684"
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

## <a name="requirements"></a>Configuration requise



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence HLSL Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




