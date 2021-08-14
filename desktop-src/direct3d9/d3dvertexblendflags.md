---
description: Définit les indicateurs utilisés pour contrôler le nombre ou les matrices que le système applique lors de la fusion de vertex multimatrix.
ms.assetid: 5314f455-ce5f-4ff5-81fc-d3dffc8705b7
title: Énumération D3DVERTEXBLENDFLAGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBLENDFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: ecc7f99e26088ff03b626604279bffe5c64ddb82b95a6f6219b637b3fce5a59b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527303"
---
# <a name="d3dvertexblendflags-enumeration"></a>Énumération D3DVERTEXBLENDFLAGS

Définit les indicateurs utilisés pour contrôler le nombre ou les matrices que le système applique lors de la fusion de vertex multimatrix.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DVERTEXBLENDFLAGS { 
  D3DVBF_DISABLE   = 0,
  D3DVBF_1WEIGHTS  = 1,
  D3DVBF_2WEIGHTS  = 2,
  D3DVBF_3WEIGHTS  = 3,
  D3DVBF_TWEENING  = 255,
  D3DVBF_0WEIGHTS  = 256
} D3DVERTEXBLENDFLAGS, *LPD3DVERTEXBLENDFLAGS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DVBF_DISABLE"></span><span id="d3dvbf_disable"></span>**Désactivation de D3DVBF \_**
</dt> <dd>

Désactiver la fusion de vertex ; Appliquez uniquement la matrice universelle définie par la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , où la valeur d’index de l’état de la transformation est 0.

</dd> <dt>

<span id="D3DVBF_1WEIGHTS"></span><span id="d3dvbf_1weights"></span>**D3DVBF \_ 1WEIGHTS**
</dt> <dd>

Activez la fusion de vertex entre les deux matrices définies par la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , où la valeur d’index pour les États de transformation est 0 et 1.

</dd> <dt>

<span id="D3DVBF_2WEIGHTS"></span><span id="d3dvbf_2weights"></span>**D3DVBF \_ 2WEIGHTS**
</dt> <dd>

Activez la fusion de vertex entre les trois matrices définies par la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , où la valeur d’index pour les États de transformation est 0, 1 et 2.

</dd> <dt>

<span id="D3DVBF_3WEIGHTS"></span><span id="d3dvbf_3weights"></span>**D3DVBF \_ 3WEIGHTS**
</dt> <dd>

Activez la fusion de vertex entre les quatre matrices définies par la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , où la valeur d’index pour les États de transformation est 0, 1, 2 et 3.

</dd> <dt>

<span id="D3DVBF_TWEENING"></span><span id="d3dvbf_tweening"></span>**\_Interpolation D3DVBF**
</dt> <dd>

La fusion de vertex s’effectue à l’aide de la valeur assignée à D3DRS \_ TWEENFACTOR.

</dd> <dt>

<span id="D3DVBF_0WEIGHTS"></span><span id="d3dvbf_0weights"></span>**D3DVBF \_ 0WEIGHTS**
</dt> <dd>

Utilisez une matrice unique avec un poids de 1,0.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les membres de ce type sont utilisés avec l' \_ État de rendu D3DRS VERTEXBLEND.

La fusion géométrique (mélange de vertex multimatrix) requiert que votre application utilise un format de vertex qui a des poids de fusion (bêta) pour chaque vertex.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> <dt>

[**D3DTS \_ World**](d3dts-world.md)
</dt> <dt>

[**D3DTS \_ worldn**](d3dts-worldn.md)
</dt> <dt>

[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)
</dt> </dl>

 

 
