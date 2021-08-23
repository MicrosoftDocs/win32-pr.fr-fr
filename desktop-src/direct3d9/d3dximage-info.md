---
description: D3DXIMAGE_INFO structure-retourne une description du contenu d’origine d’un fichier image.
ms.assetid: d6cbd5b7-642e-43ce-a2ed-11a400c5bdc1
title: Structure D3DXIMAGE_INFO (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMAGE_INFO
api_type:
- HeaderDef
api_location:
- d3dx9tex.h
ms.openlocfilehash: ede879b288569b503257abeb189d93316ed2bd96dd4db99f6e22f32bbb4f98b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607819"
---
# <a name="d3dximage_info-structure"></a>\_Structure d’informations D3DXIMAGE

Retourne une description du contenu d’origine d’un fichier image.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXIMAGE_INFO {
  UINT                 Width;
  UINT                 Height;
  UINT                 Depth;
  UINT                 MipLevels;
  D3DFORMAT            Format;
  D3DRESOURCETYPE      ResourceType;
  D3DXIMAGE_FILEFORMAT ImageFileFormat;
} D3DXIMAGE_INFO, *LPD3DXIMAGE_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**Width**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Largeur de l’image d’origine, en pixels.

</dd> <dt>

**Height**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Hauteur de l’image d’origine en pixels.

</dd> <dt>

**Profondeur**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Profondeur de l’image d’origine, en pixels.

</dd> <dt>

**Miplevels a**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de niveaux MIP dans l’image d’origine.

</dd> <dt>

**Format**
</dt> <dd>

Type : **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Valeur du type énuméré [D3DFORMAT](d3dformat.md) qui décrit le plus précisément les données de l’image d’origine.

</dd> <dt>

**ResourceType**
</dt> <dd>

Type : **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Représente le type de la texture stockée dans le fichier. Il s’agit de D3DRTYPE \_ texture, D3DRTYPE \_ VOLUMETEXTURE ou D3DRTYPE \_ CubeTexture.

</dd> <dt>

**ImageFileFormat**
</dt> <dd>

Type : **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**

</dd> <dd>

Représente le format du fichier image.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9tex. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
