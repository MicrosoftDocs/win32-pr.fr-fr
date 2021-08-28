---
description: Décrit une case verrouillée (volume).
ms.assetid: b371fb5e-2d65-453c-acd7-214de8aaa78a
title: Structure D3DLOCKED_BOX (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_BOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: deb83c71eb9fe9fa5c69667e6dc48187144fa5c18e1daf084e4a04c1fd213744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750989"
---
# <a name="d3dlocked_box-structure"></a>\_Structure de la boîte de D3DLOCKED

Décrit une case verrouillée (volume).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DLOCKED_BOX {
  int  RowPitch;
  int  SlicePitch;
  void *pBits;
} D3DLOCKED_BOX, *LPD3DLOCKED_BOX;
```



## <a name="members"></a>Membres

<dl> <dt>

**RowPitch**
</dt> <dd>

Type : **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset d’octet à partir du bord gauche d’une ligne jusqu’au bord gauche de la ligne suivante.

</dd> <dt>

**SlicePitch**
</dt> <dd>

Type : **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Décalage d’octet par rapport à l’angle supérieur gauche d’un secteur à l’angle supérieur gauche du secteur le plus profond suivant.

</dd> <dt>

**pBits**
</dt> <dd>

Type : **void \***

</dd> <dd>

Pointeur vers le début de la zone de volume. Si un [**D3DBOX**](d3dbox.md) a été fourni à l’appel de la boîte postale scellée, pBits sera correctement décalé à partir du début du volume.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les volumes peuvent être visualisés comme étant organisés en secteurs de surfaces 2D de largeur x hauteur empilées pour créer un volume de profondeur x hauteur x profondeur. Pour plus d’informations, consultez [ressources de texture de volume (Direct3D 9)](volume-texture-resources.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DVolume9 :: LockBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**IDirect3DVolumeTexture9 :: LockBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)
</dt> </dl>

 

 
