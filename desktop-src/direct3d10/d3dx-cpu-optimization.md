---
description: Spécifie que le jeu d’instructions D3DX est actuellement optimisé pour.
ms.assetid: 5fc97028-4a9d-4bc7-9c90-236a70e570e1
title: Énumération D3DX_CPU_OPTIMIZATION (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX_CPU_OPTIMIZATION
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 208422604e79b3ef7a87b548e7d71eceedd9fb78
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522579"
---
# <a name="d3dx_cpu_optimization-enumeration"></a>Énumération de l’optimisation de l' \_ UC D3DX \_

Spécifie que le jeu d’instructions D3DX est actuellement optimisé pour.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _D3DX_CPU_OPTIMIZATION { 
  D3DX_NOT_OPTIMIZED    = 0,
  D3DX_3DNOW_OPTIMIZED  = 1,
  D3DX_SSE2_OPTIMIZED   = 2,
  D3DX_SSE_OPTIMIZED    = 3
} D3DX_CPU_OPTIMIZATION;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX_NOT_OPTIMIZED"></span><span id="d3dx_not_optimized"></span>**D3DX \_ non \_ optimisé**
</dt> <dd>

N’optimisez pas.

</dd> <dt>

<span id="D3DX_3DNOW_OPTIMIZED"></span><span id="d3dx_3dnow_optimized"></span>**D3DX \_ 3DNow \_ optimisé**
</dt> <dd>

Optimiser pour un 3DNow ! ensemble d’instructions.

</dd> <dt>

<span id="D3DX_SSE2_OPTIMIZED"></span><span id="d3dx_sse2_optimized"></span>**D3DX \_ SSE2 \_ optimisé**
</dt> <dd>

Optimiser pour un jeu d’instructions SSE2.

</dd> <dt>

<span id="D3DX_SSE_OPTIMIZED"></span><span id="d3dx_sse_optimized"></span>**D3DX \_ SSE \_ optimisé**
</dt> <dd>

Optimiser pour un jeu d’instructions SSE.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




