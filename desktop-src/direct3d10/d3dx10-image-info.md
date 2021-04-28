---
description: D3DX10_IMAGE_INFO structure-retourne une description du contenu d’origine d’un fichier image.
ms.assetid: 40d89166-cc11-490d-867c-ae5db23a0784
title: Structure D3DX10_IMAGE_INFO (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_INFO
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 228ddf777217e9e61369b0a7fc3b3eb1ca012b1d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105477"
---
# <a name="d3dx10_image_info-structure"></a>Structure d’informations d' \_ image d3dx10 \_

Retourne une description du contenu d’origine d’un fichier image.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DX10_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D10_RESOURCE_DIMENSION ResourceDimension;
  D3DX10_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX10_IMAGE_INFO, *LPD3DX10_IMAGE_INFO;
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

**ArraySize**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Taille du tableau de texture. *ArraySize* sera 1 pour une seule image.

</dd> <dt>

**Miplevels a**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de niveaux de mipmap dans l’image d’origine.

</dd> <dt>

**MiscFlags**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Diverses propriétés de ressource ( [**consultez \_ \_ \_ indicateur divers des ressources D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).

</dd> <dt>

**Format**
</dt> <dd>

Type : **[ **dxgi \_ format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Valeur du type énuméré [**de \_ format dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) qui décrit le plus précisément les données de l’image d’origine.

</dd> <dt>

**ResourceDimension**
</dt> <dd>

Type : **[ **\_ \_ dimension de ressource D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**

</dd> <dd>

Représente le type de la texture stockée dans le fichier. Consultez [**\_ \_ dimension de ressource D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).

</dd> <dt>

**ImageFileFormat**
</dt> <dd>

Type : **[ **d3dx10 \_ image \_ file \_ format**](d3dx10-image-file-format.md)**

</dd> <dd>

Représente le format du fichier image. Consultez [**\_ format de \_ fichier \_ image d3dx10**](d3dx10-image-file-format.md).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
