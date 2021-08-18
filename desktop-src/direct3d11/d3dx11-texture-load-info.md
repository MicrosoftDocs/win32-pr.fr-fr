---
title: Structure D3DX11_TEXTURE_LOAD_INFO (D3DX11tex. h)
description: 'remarque : la bibliothèque de l’utilitaire d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Décrit les paramètres utilisés pour charger une texture à partir d’une autre texture.'
ms.assetid: 2fe24752-d1bc-4666-bf0f-cc397394da56
keywords:
- Structure D3DX11_TEXTURE_LOAD_INFO Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TEXTURE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b441ed81e7054cb84731f204ddbf2a863b7a98a75e5e01ed54cf49b28dba7957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989899"
---
# <a name="d3dx11_texture_load_info-structure"></a>\_Structure d' \_ \_ informations sur le chargement de la texture D3DX11

> [!Note]  
> la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.

 

Décrit les paramètres utilisés pour charger une texture à partir d’une autre texture.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DX11_TEXTURE_LOAD_INFO {
  D3D11_BOX *pSrcBox;
  D3D11_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX11_TEXTURE_LOAD_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**pSrcBox**
</dt> <dd>

Type : **[ **d3d11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***

</dd> <dd>

Zone texture source (consultez [**d3d11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).

</dd> <dt>

**pDstBox**
</dt> <dd>

Type : **[ **d3d11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***

</dd> <dd>

Zone texture de destination (voir [**d3d11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).

</dd> <dt>

**SrcFirstMip**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Niveau de mipmap de la texture source, consultez [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) pour plus de détails.

</dd> <dt>

**DstFirstMip**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Niveau de mipmap de texture de destination, consultez [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) pour plus de détails.

</dd> <dt>

**NumMips**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre de niveaux de mipmap dans la texture source.

</dd> <dt>

**SrcFirstElement**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Premier élément de la texture source.

</dd> <dt>

**DstFirstElement**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Premier élément de la texture de destination.

</dd> <dt>

**NumElements**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre d’éléments à charger.

</dd> <dt>

**Filter**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Options de filtrage pendant le rééchantillonnage (voir [**\_ \_ indicateur de filtre D3DX11**](d3dx11-filter-flag.md)).

</dd> <dt>

**MipFilter**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Options de filtrage lors de la génération de niveaux MIP (voir [**\_ \_ indicateur de filtre D3DX11**](d3dx11-filter-flag.md)).

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure est utilisée dans un appel à [**D3DX11LoadTextureFromTexture**](d3dx11loadtexturefromtexture.md).

Les valeurs par défaut sont :


```
    pSrcBox = NULL;
    pDstBox = NULL;
    SrcFirstMip = 0;
    DstFirstMip = 0;
    NumMips = D3DX11_DEFAULT;
    SrcFirstElement = 0;
    DstFirstElement = 0;
    NumElements = D3DX11_DEFAULT;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

