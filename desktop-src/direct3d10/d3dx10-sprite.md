---
description: Définit les informations relatives à la position, à la texture et à la couleur d’un sprite.
ms.assetid: 4b8d1ed1-75d5-418c-b809-410c6a44d425
title: Structure D3DX10_SPRITE (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SPRITE
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: b896b8158e84caa841addbac7abae8c972c06acd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922788"
---
# <a name="d3dx10_sprite-structure"></a>D3DX10, \_ structure

Définit les informations relatives à la position, à la texture et à la couleur d’un sprite.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DX10_SPRITE {
  D3DXMATRIX               matWorld;
  D3DXVECTOR2              TexCoord;
  D3DXVECTOR2              TexSize;
  D3DXCOLOR                ColorModulate;
  ID3D10ShaderResourceView *pTexture;
  UINT                     TextureIndex;
} D3DX10_SPRITE;
```



## <a name="members"></a>Membres

<dl> <dt>

**matWorld**
</dt> <dd>

Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)**

</dd> <dd>

Transformation universelle du modèle du sprite. Cela définit la position et l’orientation du sprite dans l’espace universel.

</dd> <dt>

**TexCoord**
</dt> <dd>

Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**

</dd> <dd>

Décalage à partir de l’angle supérieur gauche de la texture indiquant l’emplacement où l’image du sprite doit commencer dans la texture. **TexCoord** est en coordonnées de texture.

</dd> <dt>

**TexSize**
</dt> <dd>

Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**

</dd> <dd>

Vecteur contenant la largeur et la hauteur du sprite dans les coordonnées de texture.

</dd> <dt>

**ColorModulate**
</dt> <dd>

Type : **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

</dd> <dd>

Couleur qui sera multipliée par la couleur de pixel avant le rendu.

</dd> <dt>

**pTexture**
</dt> <dd>

Type : **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\***

</dd> <dd>

Pointeur vers une vue de la ressource Shader qui représente la texture du sprite. Voir [**interface ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).

</dd> <dt>

**TextureIndex**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Index de la texture. Si pTexture ne représente pas un tableau de texture, la valeur doit être 0.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
