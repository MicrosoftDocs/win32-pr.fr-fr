---
title: Énumération D3DX11_NORMALMAP_FLAG (D3DX11tex. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Options de mappage normales. Vous pouvez combiner n’importe quel nombre de ces indicateurs à l’aide d’une opération or au niveau du bit.'
ms.assetid: cc9c8a54-be1e-4594-8274-9955562a6fa8
keywords:
- Énumération D3DX11_NORMALMAP_FLAG Direct3D 11
- Pointeur d’énumération LPD3DX11_NORMALMAP_FLAG Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_NORMALMAP_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37f5d9669370e6df03d783ae1cb82a5eeb5a9142
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211948"
---
# <a name="d3dx11_normalmap_flag-enumeration"></a>D3DX11 \_ NORMALMAP \_ Flag (énumération)

> [!Note]  
> La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.

 

Options de mappage normales. Vous pouvez combiner n’importe quel nombre de ces indicateurs à l’aide d’une opération or au niveau du bit.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DX11_NORMALMAP_FLAG { 
  D3DX11_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX11_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX11_NORMALMAP_MIRROR             = (3 << 16),
  D3DX11_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX11_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX11_NORMALMAP_FLAG, *LPD3DX11_NORMALMAP_FLAG;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX11_NORMALMAP_MIRROR_U"></span><span id="d3dx11_normalmap_mirror_u"></span>**D3DX11 \_ NORMALMAP \_ miroir \_ U**
</dt> <dd>

Indique que les pixels du bord de la texture sur l’axe des U doivent être mis en miroir, pas renvoyés à la ligne.

</dd> <dt>

<span id="D3DX11_NORMALMAP_MIRROR_V"></span><span id="d3dx11_normalmap_mirror_v"></span>**D3DX11 \_ NORMALMAP \_ miroir \_ V**
</dt> <dd>

Indique que les pixels du bord de la texture sur l’axe V doivent être mis en miroir, pas renvoyés à la ligne.

</dd> <dt>

<span id="D3DX11_NORMALMAP_MIRROR"></span><span id="d3dx11_normalmap_mirror"></span>**\_Miroir D3DX11 NORMALMAP \_**
</dt> <dd>

Identique à D3DX11 \_ NORMALMAP \_ miroir \_ U \| D3DX11 \_ NORMALMAP \_ MIRROR \_ V.

</dd> <dt>

<span id="D3DX11_NORMALMAP_INVERTSIGN"></span><span id="d3dx11_normalmap_invertsign"></span>**D3DX11 \_ NORMALMAP \_ INVERTSIGN**
</dt> <dd>

Inverse la direction de chaque normal.

</dd> <dt>

<span id="D3DX11_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx11_normalmap_compute_occlusion"></span>**\_Occlusion de \_ calcul D3DX11 \_ NORMALMAP**
</dt> <dd>

Calcule le terme d’occlusion par pixel et l’encode en alpha. Une valeur alpha de 1 signifie que le pixel n’est pas masqué de quelque façon que ce soit, et une valeur alpha de 0 signifie que le pixel est complètement masqué.

</dd> </dl>

## <a name="remarks"></a>Notes

Ces indicateurs sont utilisés par [**D3DX11ComputeNormalMap**](d3dx11computenormalmap.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





