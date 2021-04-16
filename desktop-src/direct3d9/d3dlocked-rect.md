---
description: Décrit une zone rectangulaire verrouillée.
ms.assetid: ee5d2ea6-bf98-4b09-bc67-b808ffcb23c6
title: Structure D3DLOCKED_RECT (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_RECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9242a267085579cce52e66f2b9326a8e6298c87c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530957"
---
# <a name="d3dlocked_rect-structure"></a>D3DLOCKED \_ Rect, structure

Décrit une zone rectangulaire verrouillée.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DLOCKED_RECT {
  INT  Pitch;
  void *pBits;
} D3DLOCKED_RECT, *LPD3DLOCKED_RECT;
```



## <a name="members"></a>Membres

<dl> <dt>

**Inclinaison**
</dt> <dd>

Type : **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre d’octets dans une ligne de la surface.

</dd> <dt>

**pBits**
</dt> <dd>

Type : **void \***

</dd> <dd>

Pointeur vers les bits verrouillés. Si un [**Rect**](/previous-versions//dd162897(v=vs.85)) a été fourni à l’appel [**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) , pBits sera correctement décalé à partir du début de l’aire.

</dd> </dl>

## <a name="remarks"></a>Notes

Le pas pour les formats DXTn est différent de ce qui a été retourné dans DirectX 7. Il fait maintenant référence au nombre d’octets dans une ligne de blocs. Par exemple, si vous avez une largeur de 16, vous obtiendrez un pas de 4 blocs (4 \* 8 pour DXT1, 4 \* pour DXT2-5).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DCubeTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**IDirect3DSurface9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect)
</dt> <dt>

[**IDirect3DTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
</dt> </dl>

 

 
