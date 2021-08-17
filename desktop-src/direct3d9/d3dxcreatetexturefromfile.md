---
description: Crée une texture à partir d’un fichier.
ms.assetid: 247b0ee2-ee31-4090-b94c-41951b46675f
title: D3DXCreateTextureFromFile, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b3ffce68a8044267e67d874412264d5a915c65b88ea5cc13b0cd8d2cd1400828
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732158"
---
# <a name="d3dxcreatetexturefromfile-function"></a>D3DXCreateTextureFromFile fonction)

Crée une texture à partir d’un fichier.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreateTextureFromFile(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  LPCTSTR            pSrcFile,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
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

*ppTexture* \[ à\]
</dt> <dd>

Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Adresse d’un pointeur vers une interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) représentant l’objet de texture créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Le paramètre du compilateur détermine également la version de la fonction. Si Unicode est défini, l’appel de fonction est résolu en D3DXCreateTextureFromFileW. Dans le cas contraire, l’appel de fonction est résolu en D3DXCreateTextureFromFileA, car les chaînes ANSI sont utilisées.

Cette fonction prend en charge les formats de fichier suivants : .bmp,. DDS,. dib,. HDR, .jpg,. PFM, .png,. ppm et. tga. Consultez [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

La fonction est équivalente à D3DXCreateTextureFromFileEx (pDevice, pSrcFile, D3DX \_ default, D3DX \_ par défaut, D3DX default, \_ 0, D3DFMT \_ UNknown, D3DPOOL \_ Managed, D3DX \_ default, D3DX \_ default, 0, **null**, **null,** ppTexture).

Les textures Mipmapped ont automatiquement chaque niveau rempli avec la texture chargée.

Lors du chargement d’images dans des textures mipmapped, certains appareils ne peuvent pas accéder à une image 1x1 et cette fonction échoue. Dans ce cas, les images doivent être chargées manuellement.

Notez qu’une ressource créée avec cette fonction sera placée dans la classe de mémoire indiquée par D3DPOOL \_ Managed.

Le filtrage est appliqué automatiquement à une texture créée à l’aide de cette méthode. Le filtrage est équivalent au filtre \_ \_ triangulaire \| de filtre D3DX \_ \_ , filtre en fondu dans le [ \_ filtre D3DX](d3dx-filter.md).

Pour des performances optimales lors de l’utilisation de **D3DXCreateTextureFromFile**:

1.  La mise à l’échelle des images et la conversion du format au moment du chargement peuvent être lentes. Stockez les images au format et à la résolution qu’elles seront utilisées. Si le matériel cible requiert une puissance de deux dimensions, créez et stockez des images à l’aide de la puissance de deux dimensions.
2.  Envisagez d’utiliser des fichiers de surface DirectDraw (DDS). Étant donné que les fichiers DDS peuvent être utilisés pour représenter n’importe quel format de texture Direct3D 9, ils sont très faciles à lire pour D3DX. En outre, ils peuvent stocker des des mipmaps, de sorte que tous les algorithmes de génération de mipmap peuvent être utilisés pour créer les images.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)
</dt> <dt>

[Fonctions de texture dans D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
