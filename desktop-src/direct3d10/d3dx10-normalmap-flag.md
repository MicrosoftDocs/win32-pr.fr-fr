---
description: Ces indicateurs permettent de contrôler la façon dont D3DX10ComputeNormalMap génère des mappages normaux. N’importe quel nombre de ces indicateurs peut être ou, ensemble, dans n’importe quelle combinaison.
ms.assetid: 307936c1-3137-41fe-8bea-7a82e6db0867
title: Énumération D3DX10_NORMALMAP_FLAG (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_NORMALMAP_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: c4b6962561007fbc3e64b471c045e98b2f8328b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531346"
---
# <a name="d3dx10_normalmap_flag-enumeration"></a>D3DX10 \_ NORMALMAP \_ Flag (énumération)

Ces indicateurs permettent de contrôler la façon dont [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) génère des mappages normaux. N’importe quel nombre de ces indicateurs peut être ou, ensemble, dans n’importe quelle combinaison.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DX10_NORMALMAP_FLAG { 
  D3DX10_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX10_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX10_NORMALMAP_MIRROR             = (3 << 16),
  D3DX10_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX10_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX10_NORMALMAP_FLAG, *LPD3DX10_NORMALMAP_FLAG;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_NORMALMAP_MIRROR_U"></span><span id="d3dx10_normalmap_mirror_u"></span>**D3DX10 \_ NORMALMAP \_ miroir \_ U**
</dt> <dd>

Indique que les pixels du bord de la texture sur l’axe des U doivent être mis en miroir, pas renvoyés à la ligne.

</dd> <dt>

<span id="D3DX10_NORMALMAP_MIRROR_V"></span><span id="d3dx10_normalmap_mirror_v"></span>**D3DX10 \_ NORMALMAP \_ miroir \_ V**
</dt> <dd>

Indique que les pixels du bord de la texture sur l’axe V doivent être mis en miroir, pas renvoyés à la ligne.

</dd> <dt>

<span id="D3DX10_NORMALMAP_MIRROR"></span><span id="d3dx10_normalmap_mirror"></span>**\_Miroir d3dx10 NORMALMAP \_**
</dt> <dd>

Identique à D3DX10 \_ NORMALMAP \_ miroir \_ U \| d3dx10 \_ NORMALMAP \_ MIRROR \_ V.

</dd> <dt>

<span id="D3DX10_NORMALMAP_INVERTSIGN"></span><span id="d3dx10_normalmap_invertsign"></span>**D3DX10 \_ NORMALMAP \_ INVERTSIGN**
</dt> <dd>

Inverse la direction de chaque normal.

</dd> <dt>

<span id="D3DX10_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx10_normalmap_compute_occlusion"></span>**\_Occlusion de \_ calcul d3dx10 \_ NORMALMAP**
</dt> <dd>

Calcule le terme d’occlusion par pixel et l’encode en alpha. Une valeur alpha de 1 signifie que le pixel n’est pas masqué de quelque façon que ce soit, et une valeur alpha de 0 signifie que le pixel est complètement masqué.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




