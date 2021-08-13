---
title: Structure D3DX11_IMAGE_LOAD_INFO (D3DX11tex. h)
description: 'remarque : la bibliothèque de l’utilitaire d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Fournissez éventuellement des informations sur les API de chargeur de texture pour contrôler la façon dont les textures sont chargées. | Structure D3DX11_IMAGE_LOAD_INFO (D3DX11tex. h)'
ms.assetid: 6cd2f590-4e15-41e6-9f04-cd91eeb082db
keywords:
- Structure D3DX11_IMAGE_LOAD_INFO Direct3D 11
- Pointeur de structure LPD3DX11_IMAGE_LOAD_INFO Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c45bc3b9ec948c869b121190f52435a257141f1e5a6e9f36c347ab29bafb5522
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536856"
---
# <a name="d3dx11_image_load_info-structure"></a>\_Structure des \_ informations de chargement d’image D3DX11 \_

> [!Note]  
> la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.

 

Fournissez éventuellement des informations sur les API de chargeur de texture pour contrôler la façon dont les textures sont chargées. \_La valeur par défaut D3DX11 pour l’un de ces paramètres permettra à D3DX d’utiliser automatiquement la valeur du fichier source.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DX11_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D11_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX11_IMAGE_INFO *pSrcInfo;
} D3DX11_IMAGE_LOAD_INFO, *LPD3DX11_IMAGE_LOAD_INFO;
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

**FirstMipLevel**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Niveau de mipmap de résolution le plus élevé de la texture. Si la valeur est supérieure à 0, après le chargement de la texture, FirstMipLevel est mappé au niveau mipmap 0.

</dd> <dt>

**Miplevels a**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre maximal de niveaux de mipmap dans la texture. Consultez les notes dans [**d3d11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv). L’utilisation de \_ la valeur par défaut 0 ou D3DX11 entraîne la création d’une chaîne mipmap complète.

</dd> <dt>

**Utilisation**
</dt> <dd>

Type : **[ **\_ utilisation de d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)**

</dd> <dd>

La façon dont la ressource de texture est destinée à être utilisée. Consultez [**\_ utilisation de d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).

</dd> <dt>

**BindFlags**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Étapes de pipeline que la texture sera autorisée à lier. Consultez [**l' \_ \_ indicateur de liaison d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag).

</dd> <dt>

**Cpuaccessflags a**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Autorisations d’accès dont dispose l’UC pour la ressource de texture. Consultez [**\_ indicateur d' \_ accès \_ au processeur d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).

</dd> <dt>

**MiscFlags**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Diverses propriétés de ressource ( [**consultez \_ \_ \_ indicateur divers des ressources d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)).

</dd> <dt>

**Format**
</dt> <dd>

Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Énumération de [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) indiquant le format de la texture après son chargement.

</dd> <dt>

**Filter**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Filtre la texture à l’aide du filtre spécifié (uniquement lors du rééchantillonnage). Consultez [**\_ \_ indicateur de filtre D3DX11**](d3dx11-filter-flag.md).

</dd> <dt>

**MipFilter**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Filtrez les niveaux MIP de texture à l’aide du filtre spécifié (uniquement si vous générez des mipmaps). Les valeurs valides sont le \_ filtre D3DX11 \_ aucun, le \_ point de filtre D3DX11, le filtre D3DX11 de filtre \_ \_ \_ linéaire ou le \_ triangle de filtre D3DX11 \_ . Consultez [**\_ \_ indicateur de filtre D3DX11**](d3dx11-filter-flag.md).

</dd> <dt>

**pSrcInfo**
</dt> <dd>

Type : **[ **\_ \_ informations sur l’image D3DX11**](d3dx11-image-info.md)\***

</dd> <dd>

Informations sur l’image d’origine. Consultez [**D3DX11 \_ image \_ info**](d3dx11-image-info.md). Peut être obtenu avec [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)ou [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

Lors de l’initialisation de la structure, vous pouvez définir n’importe quel membre sur D3DX11 \_ par défaut et D3DX l’initialise avec une valeur par défaut à partir de la texture source lorsque la texture est chargée.

Cette structure peut être utilisée par les API qui :

-   Créer des ressources, telles que [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) et [**D3DX11CreateShaderResourceViewFromFile**](d3dx11createshaderresourceviewfromfile.md).
-   Créer des processeurs de données, tels que [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) ou [**D3DX11CreateAsyncShaderResourceViewProcessor**](d3dx11createasyncshaderresourceviewprocessor.md).

Les valeurs par défaut sont :


```
    Width = D3DX11_DEFAULT;
    Height = D3DX11_DEFAULT;
    Depth = D3DX11_DEFAULT;
    FirstMipLevel = D3DX11_DEFAULT;
    MipLevels = D3DX11_DEFAULT;
    Usage = (D3D11_USAGE) D3DX11_DEFAULT;
    BindFlags = D3DX11_DEFAULT;
    CpuAccessFlags = D3DX11_DEFAULT;
    MiscFlags = D3DX11_DEFAULT;
    Format = DXGI_FORMAT_FROM_FILE;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
    pSrcInfo = NULL;
```



Voici un bref exemple qui utilise cette structure pour fournir le format de pixel lors du chargement d’une texture. Pour obtenir le code complet, consultez HDRFormats10. cpp dans l' [exemple HDRToneMappingCS11](https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx).


```
ID3D11ShaderResourceView* pCubeRV = NULL;
WCHAR strPath[MAX_PATH];
D3DX11_IMAGE_LOAD_INFO LoadInfo;

    DXUTFindDXSDKMediaFileCch( strPath, MAX_PATH, 
        L"Light Probes\\uffizi_cross.dds" );

    LoadInfo.Format = DXGI_FORMAT_R16G16B16A16_FLOAT;

    hr = D3DX11CreateShaderResourceViewFromFile( pd3dDevice, strPath, 
        &LoadInfo, NULL, &pCubeRV, NULL );
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

