---
title: Énumération D3DX11_NORMALMAP_FLAG (D3DX11tex. h)
description: 'remarque : la bibliothèque de l’utilitaire d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Options de mappage normales. Vous pouvez combiner n’importe quel nombre de ces indicateurs à l’aide d’une opération or au niveau du bit.'
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
ms.openlocfilehash: dbea7c787ac2e2aa7d988e052e2ca548a49a338c9b9f981ce73d51c40e0b4edd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300648"
---
# <a name="d3dx11_normalmap_flag-enumeration"></a>D3DX11 \_ NORMALMAP \_ Flag (énumération)

> [!Note]  
> la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.

 

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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





