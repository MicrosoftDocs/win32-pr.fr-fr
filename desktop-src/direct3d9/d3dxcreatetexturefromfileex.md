---
description: Crée une texture à partir d’un fichier. Il s’agit d’une fonction plus avancée que D3DXCreateTextureFromFile.
ms.assetid: 820bbd77-98af-4051-a22e-825fa4dd87d8
title: D3DXCreateTextureFromFileEx, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4dba1424f98389a9282fdebf9dae55c7e1601f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870105"
---
# <a name="d3dxcreatetexturefromfileex-function"></a>D3DXCreateTextureFromFileEx fonction)

Crée une texture à partir d’un fichier. Il s’agit d’une fonction plus avancée que [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreateTextureFromFileEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    LPCTSTR            pSrcFile,
  _In_    UINT               Width,
  _In_    UINT               Height,
  _In_    UINT               MipLevels,
  _In_    DWORD              Usage,
  _In_    D3DFORMAT          Format,
  _In_    D3DPOOL            Pool,
  _In_    DWORD              Filter,
  _In_    DWORD              MipFilter,
  _In_    D3DCOLOR           ColorKey,
  _Inout_ D3DXIMAGE_INFO     *pSrcInfo,
  _Out_   PALETTEENTRY       *pPalette,
  _Out_   LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture.

</dd> <dt>

*pSrcFile* \[ dans\]
</dt> <dd>

Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Pointeur vers une chaîne qui spécifie le nom de fichier. Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR. Dans le cas contraire, le type de données String est résolu en LPCSTR. Consultez la section Notes.

</dd> <dt>

*Largeur* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Largeur en pixels. Si cette valeur est égale à zéro ou D3DX \_ par défaut, les dimensions sont extraites du fichier et arrondies à une puissance de deux. Si l’appareil prend en charge les textures non-puissance de 2 et que la [ \_ valeur par défaut de D3DX \_ NONPOW2](other-d3dx-constants.md) est spécifiée, la taille n’est pas arrondie.

</dd> <dt>

*Hauteur* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Hauteur, en pixels. Si cette valeur est égale à zéro ou D3DX \_ par défaut, les dimensions sont extraites du fichier et arrondies à une puissance de deux. Si l’appareil prend en charge les textures non-puissance de 2 et que la [ \_ valeur par défaut de D3DX \_ NONPOW2](other-d3dx-constants.md) est sepcified, la taille n’est pas arrondie.

</dd> <dt>

*Miplevels a* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de niveaux MIP demandés. Si cette valeur est égale à zéro ou à D3DX \_ default, une chaîne mipmap complète est créée. Si D3DX \_ à partir d' \_ un fichier, la taille est prise exactement telle qu’elle figure dans le fichier, et l’appel échoue si cela ne respecte pas les fonctionnalités de l’appareil.

</dd> <dt>

*Utilisation* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

0, [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)ou **D3DUSAGE \_ dynamique**. L’affectation de la valeur **D3DUSAGE \_ RENDERTARGET** à cet indicateur indique que la surface doit être utilisée comme cible de rendu. La ressource peut ensuite être transmise au paramètre *pNewRenderTarget* de la méthode [**SetRenderTarget**](/windows/desktop/api) . Si **D3DUSAGE \_ RENDERTARGET** ou **D3DUSAGE \_ Dynamic** est spécifié, *pool* doit avoir la valeur D3DPOOL \_ Default et l’application doit vérifier que l’appareil prend en charge cette opération en appelant [**CheckDeviceFormat**](/windows/desktop/api). **D3DUSAGE \_ DYNAMIQUE** indique que l’aire de conception doit être gérée dynamiquement. Consultez [utilisation de textures dynamiques](performance-optimizations.md).

</dd> <dt>

*Format* \[ dans\]
</dt> <dd>

Type : **[D3DFORMAT](d3dformat.md)**

Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de pixel demandé pour la texture. La texture retournée peut avoir un format différent de celui spécifié par le *format*. Les applications doivent vérifier le format de la texture retournée. Si D3DFMT \_ est inconnu, le format est extrait du fichier. Si D3DFMT \_ à partir d' \_ un fichier, le format est pris exactement comme dans le fichier, et l’appel échoue si cela ne respecte pas les fonctionnalités de l’appareil.

</dd> <dt>

*Pool* \[ dans\]
</dt> <dd>

Type : **[ **D3DPOOL**](./d3dpool.md)**

Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , décrivant la classe de mémoire dans laquelle la texture doit être placée.

</dd> <dt>

*Filtre* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison d’une ou de plusieurs constantes de [ \_ filtre D3DX](d3dx-filter.md) contrôlant la façon dont l’image est filtrée. La spécification de la [ \_ valeur D3DX par défaut](other-d3dx-constants.md) pour ce paramètre revient à spécifier la valeur de filtre du \_ triangle de filtre D3DX \_ \| \_ \_ .

</dd> <dt>

*MipFilter* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison d’une ou de plusieurs constantes de [ \_ filtre D3DX](d3dx-filter.md) contrôlant la façon dont l’image est filtrée. La spécification \_ de D3DX par défaut pour ce paramètre est l’équivalent de la spécification de la \_ zone de filtre D3DX \_ . En outre, utilisez bits 27-31 pour spécifier le nombre de niveaux MIP à ignorer (à partir du haut de la chaîne mipmap) lorsqu’une texture. DDS est chargée en mémoire ; Cela vous permet d’ignorer jusqu’à 32 niveaux.

</dd> <dt>

*ColorKey* \[ dans\]
</dt> <dd>

Type : **[ **D3DCOLOR**](d3dcolor.md)**

Valeur [**D3DCOLOR**](d3dcolor.md) à remplacer par le noir transparent, ou 0 pour désactiver la clé de couleur. Il s’agit toujours d’une couleur ARVB de 32 bits, indépendante du format d’image source. Alpha est significatif et doit généralement être défini sur FF pour les clés de couleur opaques. Ainsi, pour le noir opaque, la valeur est égale à 0xFF000000.

</dd> <dt>

*pSrcInfo* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***

Pointeur vers une structure d' [**\_ informations D3DXIMAGE**](d3dximage-info.md) à remplir avec une description des données dans le fichier image source, ou **null**.

</dd> <dt>

*pPalette* \[ à\]
</dt> <dd>

Type : **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***

Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) qui représente une palette de couleurs 256 à remplir, ou **null**.

</dd> <dt>

*ppTexture* \[ à\]
</dt> <dd>

Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Adresse d’un pointeur vers une interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) représentant l’objet de texture créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Le paramètre du compilateur détermine également la version de la fonction. Si Unicode est défini, l’appel de fonction est résolu en D3DXCreateTextureFromFileExW. Dans le cas contraire, l’appel de fonction est résolu en D3DXCreateTextureFromFileExA, car les chaînes ANSI sont utilisées.

Utilisez [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) pour déterminer si votre appareil peut prendre en charge la texture en fonction de l’état actuel.

Cette fonction prend en charge les formats de fichier suivants :. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm et. tga. Consultez [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Les textures Mipmapped ont automatiquement chaque niveau rempli avec la texture chargée. Lors du chargement d’images dans des textures mipmapped, certains appareils ne peuvent pas accéder à une image 1x1 et cette fonction échoue. Dans ce cas, les images doivent être chargées manuellement.

Pour des performances optimales lors de l’utilisation de **D3DXCreateTextureFromFileEx**:

1.  La mise à l’échelle des images et la conversion du format au moment du chargement peuvent être lentes. Stockez les images au format et à la résolution qu’elles seront utilisées. Si le matériel cible requiert des dimensions de puissance de 2, créez et stockez des images en utilisant des dimensions de puissance de 2.
2.  Pour la création d’image mipmap au moment du chargement, filtrez à l’aide de [ \_ \_ la zone de filtre D3DX](d3dx-filter.md). Un filtre de zone est beaucoup plus rapide que les autres types de filtres tels que le \_ triangle de filtre D3DX \_ .
3.  Envisagez d’utiliser des fichiers DDS. Étant donné que les fichiers DDS peuvent être utilisés pour représenter n’importe quel format de texture Direct3D 9, ils sont très faciles à lire pour D3DX. En outre, ils peuvent stocker des des mipmaps, de sorte que tous les algorithmes de génération de mipmap peuvent être utilisés pour créer les images.

En cas d’omission des niveaux de mipmap lors du chargement d’un fichier. DDS, utilisez la \_ macro D3DX Skip \_ DDS \_ MIP \_ levels pour générer la valeur MipFilter. Cette macro prend le nombre de niveaux à ignorer et le type de filtre et retourne la valeur de filtre, qui serait ensuite transmise dans le paramètre MipFilter.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md)
</dt> <dt>

[Fonctions de texture dans D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
