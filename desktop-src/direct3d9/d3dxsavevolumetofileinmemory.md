---
description: Enregistre un volume dans une mémoire tampon. La méthode crée une mémoire tampon ID3DXBuffer pour stocker les données et retourne cet objet.
ms.assetid: 4887ff1f-7904-4764-b284-b2c8e037f806
title: D3DXSaveVolumeToFileInMemory, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7daaa41e0cc87ea03a0aedc5fc2f7ca96653329f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211745"
---
# <a name="d3dxsavevolumetofileinmemory-function"></a>D3DXSaveVolumeToFileInMemory fonction)

Enregistre un volume dans une mémoire tampon. La méthode crée une mémoire tampon [**ID3DXBuffer**](id3dxbuffer.md) pour stocker les données et retourne cet objet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXSaveVolumeToFileInMemory(
  _Out_       LPD3DXBUFFER         *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT DestFormat,
  _In_        LPDIRECT3DVOLUME9    pSrcVolume,
  _In_  const PALETTEENTRY         *pSrcPalette,
  _In_  const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppDestBuf* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse d’un pointeur vers une mémoire tampon [**ID3DXBuffer**](id3dxbuffer.md) qui stocke l’image.

</dd> <dt>

*DestFormat* \[ dans\]
</dt> <dd>

Type : **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**

[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) spécifiant le format de fichier à utiliser lors de l’enregistrement. Cette fonction prend en charge l’enregistrement dans tous les formats **D3DXIMAGE \_ FILEFORMAT** , sauf portable pixmap (. ppm) et Targa/Truevision Graphics Adapter (. TGA).

</dd> <dt>

*pSrcVolume* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**

Pointeur vers l’interface [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) contenant l’image à enregistrer.

</dd> <dt>

*pSrcPalette* \[ dans\]
</dt> <dd>

Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) contenant une palette de 256 couleurs. Ce paramètre peut être **NULL**.

</dd> <dt>

*pSrcBox* \[ dans\]
</dt> <dd>

Type : **const [**D3DBOX**](d3dbox.md) \***

Pointeur vers une structure [**D3DBOX**](d3dbox.md) . Spécifie la zone source. Affectez la valeur **null** à ce paramètre pour spécifier la totalité du volume.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être la suivante : D3DERR \_ INVALIDCALL

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de texture dans D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXSaveVolumeToFile**](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
