---
description: Décrit les paramètres utilisés pour charger une texture à partir d’une autre texture.
ms.assetid: dee693ce-afa7-479b-a76a-00816e30d5cf
title: Structure D3DX10_TEXTURE_LOAD_INFO (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_TEXTURE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 144475b4b4967ff0a1fd130a658b8276af5d8897cc043000d150417aa01b227e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753469"
---
# <a name="d3dx10_texture_load_info-structure"></a>\_Structure d' \_ \_ informations sur le chargement de la texture d3dx10

Décrit les paramètres utilisés pour charger une texture à partir d’une autre texture.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DX10_TEXTURE_LOAD_INFO {
  D3D10_BOX *pSrcBox;
  D3D10_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX10_TEXTURE_LOAD_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**pSrcBox**
</dt> <dd>

Type : **[ **D3D10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***

</dd> <dd>

Zone texture source (consultez [**D3D10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).

</dd> <dt>

**pDstBox**
</dt> <dd>

Type : **[ **D3D10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***

</dd> <dd>

Zone texture de destination (voir [**D3D10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).

</dd> <dt>

**SrcFirstMip**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Niveau de mipmap de la texture source, consultez [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) pour plus de détails.

</dd> <dt>

**DstFirstMip**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Niveau de mipmap de texture de destination, consultez [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) pour plus de détails.

</dd> <dt>

**NumMips**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de niveaux de mipmap dans la texture source.

</dd> <dt>

**SrcFirstElement**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Premier élément de la texture source.

</dd> <dt>

**DstFirstElement**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Premier élément de la texture de destination.

</dd> <dt>

**NumElements**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre d’éléments à charger.

</dd> <dt>

**Filter**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Options de filtrage pendant le rééchantillonnage (voir [**\_ \_ indicateur de filtre d3dx10**](d3dx10-filter-flag.md)).

</dd> <dt>

**MipFilter**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Options de filtrage lors de la génération de niveaux MIP (voir [**\_ \_ indicateur de filtre d3dx10**](d3dx10-filter-flag.md)).

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure est utilisée dans un appel à [**D3DX10LoadTextureFromTexture**](d3dx10loadtexturefromtexture.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
