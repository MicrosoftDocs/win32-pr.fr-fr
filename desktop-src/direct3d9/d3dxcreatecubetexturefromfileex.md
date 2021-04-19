---
description: Crée une texture de cube à partir d’un fichier. Il s’agit d’une fonction plus avancée que D3DXCreateCubeTextureFromFile.
ms.assetid: 77e64b33-9282-42fa-978c-a93fa9ba11fc
title: D3DXCreateCubeTextureFromFileEx, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b4f56ad3f8e314f7ceb5f4efb07562257efab5fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527131"
---
# <a name="d3dxcreatecubetexturefromfileex-function"></a>D3DXCreateCubeTextureFromFileEx fonction)

Crée une texture de cube à partir d’un fichier. Il s’agit d’une fonction plus avancée que [**D3DXCreateCubeTextureFromFile**](d3dxcreatecubetexturefromfile.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreateCubeTextureFromFileEx(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCTSTR                pSrcFile,
  _In_  UINT                   Size,
  _In_  UINT                   MipLevels,
  _In_  DWORD                  Usage,
  _In_  D3DFORMAT              Format,
  _In_  D3DPOOL                Pool,
  _In_  DWORD                  Filter,
  _In_  DWORD                  MipFilter,
  _In_  D3DCOLOR               ColorKey,
  _Out_ D3DXIMAGE_INFO         *pSrcInfo,
  _Out_ PALETTEENTRY           *pPalette,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture du cube.

</dd> <dt>

*pSrcFile* \[ dans\]
</dt> <dd>

Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Pointeur vers une chaîne qui spécifie le nom de fichier. Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR. Dans le cas contraire, le type de données String est résolu en LPCSTR. Consultez la section Notes.

</dd> <dt>

*Taille* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Largeur et hauteur de la texture du cube, en pixels. Par exemple, si la texture du cube est un cube de 8 pixels par 8 pixels, la valeur de ce paramètre doit être 8. Si cette valeur est 0 ou D3DX \_ default, les dimensions sont extraites du fichier.

</dd> <dt>

*Miplevels a* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de niveaux MIP demandés. Si cette valeur est égale à zéro ou à D3DX \_ default, une chaîne mipmap complète est créée.

</dd> <dt>

*Utilisation* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

0 ou D3DUSAGE \_ RENDERTARGET, ou D3DUSAGE \_ dynamique. L’affectation de la valeur D3DUSAGE RENDERTARGET à cet indicateur \_ indique que la surface doit être utilisée comme cible de rendu. La ressource peut ensuite être transmise au paramètre *pNewRenderTarget* de la méthode [**SetRenderTarget**](/windows/desktop/api) . Si D3DUSAGE \_ RENDERTARGET est spécifié, l’application doit vérifier que l’appareil prend en charge cette opération en appelant [**CheckDeviceFormat**](/windows/desktop/api). D3DUSAGE \_ Dynamic indique que la surface doit être gérée dynamiquement. Pour plus d’informations sur l’utilisation des textures dynamiques, consultez [utilisation de textures dynamiques](performance-optimizations.md).

</dd> <dt>

*Format* \[ dans\]
</dt> <dd>

Type : **[D3DFORMAT](d3dformat.md)**

Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de pixel demandé pour la texture du cube. La texture de cube retournée peut avoir un format différent de celui spécifié par le *format*. Les applications doivent vérifier le format de la texture de cube retournée. Si [D3DFMT est \_ inconnu](other-d3dx-constants.md), le format est extrait du fichier. Si D3DFMT \_ à partir d' \_ un fichier, le format est pris exactement comme dans le fichier, et l’appel échoue si cela ne respecte pas les fonctionnalités de l’appareil.

</dd> <dt>

*Pool* \[ dans\]
</dt> <dd>

Type : **[ **D3DPOOL**](./d3dpool.md)**

Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , décrivant la classe de mémoire dans laquelle la texture de cube doit être placée.

</dd> <dt>

*Filtre* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison d’une ou de plusieurs constantes de [ \_ filtre D3DX](d3dx-filter.md) , contrôlant la façon dont l’image est filtrée. La spécification \_ de la valeur D3DX par défaut pour ce paramètre revient à spécifier la valeur de filtre du \_ triangle de filtre D3DX \_ \| \_ \_ .

</dd> <dt>

*MipFilter* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison d’une ou de plusieurs constantes de [ \_ filtre D3DX](d3dx-filter.md) contrôlant la façon dont l’image est filtrée. La spécification \_ de D3DX par défaut pour ce paramètre est l’équivalent de la spécification de la \_ zone de filtre D3DX \_ . En outre, utilisez bits 27-31 pour spécifier le nombre de niveaux MIP à ignorer (à partir du haut de la chaîne mipmap) lorsqu’une texture. DDS est chargée en mémoire ; Cela vous permet d’ignorer jusqu’à 32 niveaux.

</dd> <dt>

*ColorKey* \[ dans\]
</dt> <dd>

Type : **[ **D3DCOLOR**](d3dcolor.md)**

Valeur [**D3DCOLOR**](d3dcolor.md) à remplacer par le noir transparent, ou 0 pour désactiver le ColorKey. Il s’agit toujours d’une couleur ARVB de 32 bits, indépendante du format d’image source. Alpha est significatif et doit généralement être défini sur FF pour les clés de couleur opaques. Ainsi, pour le noir opaque, la valeur est égale à 0xFF000000.

</dd> <dt>

*pSrcInfo* \[ à\]
</dt> <dd>

Type : **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***

Pointeur vers une structure d' [**\_ informations D3DXIMAGE**](d3dximage-info.md) à remplir avec une description des données dans le fichier image source, ou **null**.

</dd> <dt>

*pPalette* \[ à\]
</dt> <dd>

Type : **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***

Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) qui représente une palette de couleurs 256 à remplir, ou **null**.

</dd> <dt>

*ppCubeTexture* \[ à\]
</dt> <dd>

Type : **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***

Adresse d’un pointeur vers une interface [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , représentant l’objet de texture de cube créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Le paramètre du compilateur détermine également la version de la fonction. Si Unicode est défini, l’appel de fonction est résolu en **D3DXCreateCubeTextureFromFileExW**. Dans le cas contraire, l’appel de fonction est résolu en **D3DXCreateCubeTextureFromFileExA** , car les chaînes ANSI sont utilisées.

Cette fonction prend en charge les formats de fichier suivants :. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm et. tga. Consultez [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Les textures de cube diffèrent des autres surfaces dans le fait qu’il s’agit de collections de surfaces. Pour appeler [**SetRenderTarget**](/windows/desktop/api) avec une texture de cube, vous devez sélectionner un visage individuel à l’aide de [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) et passer la surface résultante à **SetRenderTarget**.

**D3DXCreateCubeTextureFromFileEx** utilise le format de fichier de la surface DIRECTDRAW (DDS). L’éditeur de texture DirectX (Dxtex.exe) vous permet de générer un mappage de cube à partir d’autres formats de fichier et de l’enregistrer au format de fichier DDS. Vous pouvez obtenir Dxtex.exe et en savoir plus à ce sujet à partir du kit de développement logiciel (SDK) DirectX. Pour plus d’informations sur DirectX SDK, consultez [où se trouve le kit de développement logiciel (SDK) DirectX ?](../directx-sdk--august-2009-.md).

En cas d’omission des niveaux de mipmap lors du chargement d’un fichier. DDS, utilisez la \_ macro D3DX Skip \_ DDS \_ MIP \_ levels pour générer la valeur MipFilter. Cette macro prend le nombre de niveaux à ignorer et le type de filtre et retourne la valeur de filtre, qui serait ensuite transmise dans le paramètre MipFilter.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**D3DXCreateCubeTextureFromFile**](d3dxcreatecubetexturefromfile.md)
</dt> <dt>

[Fonctions de texture dans D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
