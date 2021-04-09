---
description: Crée une texture à partir d’une ressource.
ms.assetid: 7c841f21-5565-4923-a2fe-bbd618616f87
title: D3DXCreateTextureFromResource, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4ce9101caed2a60dc3be7fe0039a1e391423f1fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870102"
---
# <a name="d3dxcreatetexturefromresource-function"></a>D3DXCreateTextureFromResource fonction)

Crée une texture à partir d’une ressource.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreateTextureFromResource(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  HMODULE            hSrcModule,
  _In_  LPCTSTR            pSrcResource,
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

*hSrcModule* \[ dans\]
</dt> <dd>

Type : **[ **HMODULE**](../winprog/windows-data-types.md)**

Handle vers le module dans lequel se trouve la ressource, ou **null** pour le module associé à l’image que le système d’exploitation a utilisé pour créer le processus actuel.

</dd> <dt>

*pSrcResource* \[ dans\]
</dt> <dd>

Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Pointeur vers une chaîne qui spécifie le nom de la ressource. Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR. Dans le cas contraire, le type de données String est résolu en LPCSTR. Consultez la section Notes.

</dd> <dt>

*ppTexture* \[ à\]
</dt> <dd>

Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Adresse d’un pointeur vers une interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) représentant l’objet de texture créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Le paramètre du compilateur détermine également la version de la fonction. Si Unicode est défini, l’appel de fonction est résolu en D3DXCreateTextureFromResourceW. Dans le cas contraire, l’appel de fonction est résolu en D3DXCreateTextureFromResourceA, car les chaînes ANSI sont utilisées.

La fonction est équivalente à D3DXCreateTextureFromResourceEx (pDevice, hSrcModule, pSrcResource, D3DX \_ default, D3DX par défaut \_ , D3DX \_ default, 0, D3DFMT \_ UNknown, D3DPOOL \_ Managed, D3DX \_ default, D3DX \_ default, 0, **null**, **null**, ppTexture).

La ressource en cours de chargement doit être de type RT \_ bitmap ou RT \_ RCDATA. Le type de ressource « RT \_ RCDATA » est utilisé pour charger des formats autres que des bitmaps (tels que. TGA,. jpg et. DDS).

Cette fonction prend en charge les formats de fichier suivants :. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm et. tga. Consultez [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Notez qu’une ressource créée avec cette fonction quand elle est appelée à partir d’un objet IDirect3DDevice9 est placée dans la classe de mémoire indiquée par D3DPOOL \_ gérée. Lorsque cette méthode est appelée à partir d’un objet IDirect3DDevice9Ex, la ressource est placée dans la classe de mémoire indiquée par la \_ valeur par défaut de D3DPOOL.

Le filtrage est appliqué automatiquement à une texture créée à l’aide de cette méthode. Le filtrage est équivalent au filtre \_ \_ triangulaire \| de filtre D3DX \_ \_ , filtre en fondu dans le [ \_ filtre D3DX](d3dx-filter.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**D3DXCreateTextureFromResourceEx**](d3dxcreatetexturefromresourceex.md)
</dt> <dt>

[Fonctions de texture dans D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
