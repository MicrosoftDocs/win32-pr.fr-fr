---
description: Fournissez éventuellement des informations sur les API de chargeur de texture pour contrôler la façon dont les textures sont chargées. \_La valeur par défaut d3dx10 pour l’un de ces paramètres permettra à D3DX d’utiliser automatiquement la valeur du fichier source.
ms.assetid: 8325d50e-a8a9-4ee2-87e2-e60fb3699af6
title: Structure D3DX10_IMAGE_LOAD_INFO (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 89e819e81c11842feaa6996e047f3cac3587792c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517577"
---
# <a name="d3dx10_image_load_info-structure"></a>\_Structure des \_ informations de chargement d’image d3dx10 \_

Fournissez éventuellement des informations sur les API de chargeur de texture pour contrôler la façon dont les textures sont chargées. \_La valeur par défaut d3dx10 pour l’un de ces paramètres permettra à D3DX d’utiliser automatiquement la valeur du fichier source.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DX10_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D10_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX10_IMAGE_INFO *pSrcInfo;
} D3DX10_IMAGE_LOAD_INFO, *LPD3DX10_IMAGE_LOAD_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**Width**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Largeur cible de la texture. Si la largeur réelle de la texture est supérieure ou inférieure à cette valeur, la texture est mise à l’échelle vers le haut ou vers le haut pour s’ajuster à cette largeur cible.

</dd> <dt>

**Height**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Hauteur cible de la texture. Si la hauteur réelle de la texture est supérieure ou inférieure à cette valeur, la texture est mise à l’échelle vers le haut ou vers le haut pour s’ajuster à cette hauteur cible.

</dd> <dt>

**Profondeur**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Profondeur de la texture. Cela s’applique uniquement aux textures de volume.

</dd> <dt>

**FirstMipLevel**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Niveau de mipmap de résolution le plus élevé de la texture. Si la valeur est supérieure à 0, après le chargement de la texture, FirstMipLevel est mappé au niveau mipmap 0.

</dd> <dt>

**Miplevels a**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre maximal de niveaux de mipmap que la texture aura. L’utilisation de \_ la valeur par défaut 0 ou d3dx10 entraîne la création d’une chaîne mipmap complète.

</dd> <dt>

**Utilisation**
</dt> <dd>

Type : **[ **\_ utilisation de D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)**

</dd> <dd>

La façon dont la ressource de texture est destinée à être utilisée. Consultez [**\_ utilisation de D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).

</dd> <dt>

**BindFlags**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Étapes de pipeline que la texture sera autorisée à lier. Consultez [**l' \_ \_ indicateur de liaison D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag).

</dd> <dt>

**Cpuaccessflags a**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Autorisations d’accès dont dispose l’UC pour la ressource de texture. Consultez [**\_ indicateur d' \_ accès \_ au processeur D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag).

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

Format de la texture après son chargement. Consultez [**\_ format dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).

</dd> <dt>

**Filter**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Filtre la texture à l’aide du filtre spécifié (uniquement lors du rééchantillonnage). Consultez [**\_ \_ indicateur de filtre d3dx10**](d3dx10-filter-flag.md).

</dd> <dt>

**MipFilter**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Filtrez les niveaux MIP de texture à l’aide du filtre spécifié (uniquement si vous générez des mipmaps). Les valeurs valides sont le \_ filtre d3dx10 \_ aucun, le \_ point de filtre d3dx10, le filtre d3dx10 de filtre \_ \_ \_ linéaire ou le \_ triangle de filtre d3dx10 \_ . Consultez [**\_ \_ indicateur de filtre d3dx10**](d3dx10-filter-flag.md).

</dd> <dt>

**pSrcInfo**
</dt> <dd>

Type : **[ **\_ \_ informations sur l’image d3dx10**](d3dx10-image-info.md)\***

</dd> <dd>

Informations sur l’image d’origine. Consultez [**d3dx10 \_ image \_ info**](d3dx10-image-info.md). Peut être obtenu avec [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md), [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md)ou [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md).

</dd> </dl>

## <a name="remarks"></a>Notes

Lors de l’initialisation de la structure, vous pouvez définir n’importe quel membre sur D3DX10 \_ par défaut et D3DX l’initialise avec une valeur par défaut à partir de la texture source lorsque la texture est chargée.

Cette structure peut être utilisée par les API qui :

-   Créer des ressources, telles que [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) et [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md).
-   Créer des processeurs de données, tels que [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) ou [**D3DX10CreateAsyncShaderResourceViewProcessor**](d3dx10createasyncshaderresourceviewprocessor.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
