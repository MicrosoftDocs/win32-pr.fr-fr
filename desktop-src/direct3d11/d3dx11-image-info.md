---
title: Structure D3DX11_IMAGE_INFO (D3DX11tex. h)
description: 'remarque : la bibliothèque de l’utilitaire d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Fournissez éventuellement des informations sur les API de chargeur de texture pour contrôler la façon dont les textures sont chargées. | Structure D3DX11_IMAGE_INFO (D3DX11tex. h)'
ms.assetid: 981f4f1d-7609-416a-8f92-c7223d8b2773
keywords:
- Structure D3DX11_IMAGE_INFO Direct3D 11
- Pointeur de structure LPD3DX11_IMAGE_INFO Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64366755e9bb9398e8107d931ee5425d2fcee78fdd9d03487b9533270cc17c19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536866"
---
# <a name="d3dx11_image_info-structure"></a>Structure d’informations d' \_ image D3DX11 \_

> [!Note]  
> la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.

 

Fournissez éventuellement des informations sur les API de chargeur de texture pour contrôler la façon dont les textures sont chargées. \_La valeur par défaut D3DX11 pour l’un de ces paramètres permettra à D3DX d’utiliser automatiquement la valeur du fichier source.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DX11_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D11_RESOURCE_DIMENSION ResourceDimension;
  D3DX11_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX11_IMAGE_INFO, *LPD3DX11_IMAGE_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**Width**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Largeur cible de la texture. Si la largeur réelle de la texture est supérieure ou inférieure à cette valeur, la texture est mise à l’échelle vers le haut ou vers le haut pour s’ajuster à cette largeur cible.

</dd> <dt>

**Height**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Hauteur cible de la texture. Si la hauteur réelle de la texture est supérieure ou inférieure à cette valeur, la texture est mise à l’échelle vers le haut ou vers le haut pour s’ajuster à cette hauteur cible.

</dd> <dt>

**Profondeur**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Profondeur de la texture. Cela s’applique uniquement aux textures de volume.

</dd> <dt>

**ArraySize**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre d’éléments dans le tableau.

</dd> <dt>

**Miplevels a**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre maximal de niveaux de mipmap dans la texture. Consultez les notes dans [**d3d11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv). L’utilisation de \_ la valeur par défaut 0 ou D3DX11 entraîne la création d’une chaîne mipmap complète.

</dd> <dt>

**MiscFlags**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Diverses propriétés de ressource spécifiées avec un indicateur d' [**\_ \_ \_ indicateur div de ressource d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) .

</dd> <dt>

**Format**
</dt> <dd>

Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Énumération de [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) spécifiant le format de la texture après son chargement.

</dd> <dt>

**ResourceDimension**
</dt> <dd>

Type : **[ **\_ \_ dimension de ressource d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)**

</dd> <dd>

Valeur [**de \_ \_ dimension de ressource d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension) , qui identifie le type de ressource.

</dd> <dt>

**ImageFileFormat**
</dt> <dd>

Type : **[ **D3DX11 \_ image \_ file \_ format**](d3dx11-image-file-format.md)**

</dd> <dd>

Valeur [**de \_ \_ \_ format de fichier image D3DX11**](d3dx11-image-file-format.md) , qui identifie le format de l’image.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure est utilisée par les méthodes telles que : [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)ou [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

