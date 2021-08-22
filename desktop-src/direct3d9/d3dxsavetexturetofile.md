---
description: Enregistre une texture dans un fichier.
ms.assetid: b14dd893-e967-4be9-81e8-aeb52035d91c
title: D3DXSaveTextureToFile, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveTextureToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 954b761f8980a7397be1c79fbd8beb88ddbb29f29ce74557ca90cc77dee2ea5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988316"
---
# <a name="d3dxsavetexturetofile-function"></a>D3DXSaveTextureToFile fonction)

Enregistre une texture dans un fichier.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXSaveTextureToFile(
  _In_       LPCTSTR                pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT   DestFormat,
  _In_       LPDIRECT3DBASETEXTURE9 pSrcTexture,
  _In_ const PALETTEENTRY           *pSrcPalette
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDestFile* \[ dans\]
</dt> <dd>

Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Pointeur vers une chaîne qui spécifie le nom de fichier de l’image de destination. Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR. Dans le cas contraire, le type de données String est résolu en LPCSTR. Consultez la section Notes.

</dd> <dt>

*DestFormat* \[ dans\]
</dt> <dd>

Type : **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**

[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) spécifiant le format de fichier à utiliser lors de l’enregistrement. Cette fonction prend en charge l’enregistrement dans tous les formats **D3DXIMAGE \_ FILEFORMAT** , sauf portable pixmap (. ppm) et Targa/Truevision Graphics Adapter (. TGA).

</dd> <dt>

*pSrcTexture* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Pointeur vers l’interface [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) , contenant la texture à enregistrer.

</dd> <dt>

*pSrcPalette* \[ dans\]
</dt> <dd>

Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) contenant une palette de 256 couleurs. Ce paramètre peut être **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être la suivante : D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Remarques

Le paramètre du compilateur détermine également la version de la fonction. Si Unicode est défini, l’appel de fonction est résolu en D3DXSaveTextureToFileW. Dans le cas contraire, l’appel de fonction est résolu en D3DXSaveTextureToFileA, car les chaînes ANSI sont utilisées.

Cette fonction gère la conversion vers et à partir des formats de texture compressés.

Si le volume n’est pas dynamique (en raison d’un paramètre d’utilisation défini à 0 lors de la création) et situé dans la mémoire vidéo (le pool de mémoire défini sur D3DPOOL \_ par défaut), **D3DXSaveTextureToFile** échoue car D3DX ne peut pas verrouiller les volumes non dynamiques situés dans la mémoire vidéo.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de texture dans D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXSaveSurfaceToFile**](d3dxsavesurfacetofile.md)
</dt> <dt>

[**D3DXSaveVolumeToFile**](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
