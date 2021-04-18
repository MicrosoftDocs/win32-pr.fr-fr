---
description: Charge un volume à partir d’une ressource.
ms.assetid: 3fa1243b-5e31-4737-8d3c-08852d6528d9
title: D3DXLoadVolumeFromResource, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d57ce492db24ac9920662d4de5baed4650dd801
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522566"
---
# <a name="d3dxloadvolumefromresource-function"></a>D3DXLoadVolumeFromResource fonction)

Charge un volume à partir d’une ressource.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXLoadVolumeFromResource(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       HMODULE           hSrcModule,
  _In_       LPCSTR            pSrcResource,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDestVolume* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**

Pointeur vers une interface [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) . Spécifie le volume de destination.

</dd> <dt>

*pDestPalette* \[ dans\]
</dt> <dd>

Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la palette de destination de 256 couleurs ou **null**.

</dd> <dt>

*pDestBox* \[ dans\]
</dt> <dd>

Type : **const [**D3DBOX**](d3dbox.md) \***

Pointeur vers une structure [**D3DBOX**](d3dbox.md) . Spécifie la zone de destination. Affectez la valeur **null** à ce paramètre pour spécifier la totalité du volume.

</dd> <dt>

*hSrcModule* \[ dans\]
</dt> <dd>

Type : **[ **HMODULE**](../winprog/windows-data-types.md)**

Handle vers le module dans lequel se trouve la ressource, ou **null** pour le module associé à l’image que le système d’exploitation a utilisé pour créer le processus actuel.

</dd> <dt>

*pSrcResource* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Pointeur vers une chaîne qui spécifie le nom de fichier de l’image source. Si UNICODE ou \_ Unicode sont définis, ce type de paramètre est LPCWSTR, sinon, le type est LPCSTR.

</dd> <dt>

*pSrcBox* \[ dans\]
</dt> <dd>

Type : **const [**D3DBOX**](d3dbox.md) \***

Pointeur vers une structure [**D3DBOX**](d3dbox.md) . Spécifie la zone source. Affectez la valeur **null** à ce paramètre pour spécifier la totalité du volume.

</dd> <dt>

*Filtre* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison d’un ou de [plusieurs \_ filtres D3DX](d3dx-filter.md), contrôlant la façon dont l’image est filtrée. La spécification \_ de la valeur D3DX par défaut pour ce paramètre revient à spécifier la valeur de filtre du \_ triangle de filtre D3DX \_ \| \_ \_ .

</dd> <dt>

*ColorKey* \[ dans\]
</dt> <dd>

Type : **[ **D3DCOLOR**](d3dcolor.md)**

Valeur [**D3DCOLOR**](d3dcolor.md) à remplacer par le noir transparent, ou 0 pour désactiver le ColorKey. Il s’agit toujours d’une couleur ARVB de 32 bits, indépendante du format d’image source. Alpha est significatif et doit généralement être défini sur FF pour les clés de couleur opaques. Ainsi, pour le noir opaque, la valeur est égale à 0xFF000000.

</dd> <dt>

*pSrcInfo* \[ dans\]
</dt> <dd>

Type : **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***

Pointeur vers une structure d' [**\_ informations D3DXIMAGE**](d3dximage-info.md) à remplir avec une description des données dans le fichier image source, ou **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="remarks"></a>Notes

La ressource en cours de chargement doit être une ressource bitmap (RT \_ bitmap).

Cette fonction gère la conversion vers et à partir des formats de texture compressés.

L’écriture sur une surface non-niveau zéro de la texture du volume n’entraîne pas la mise à jour du rectangle de modification. Si [**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md) est appelé et que la texture n’a pas déjà été modifiée (ce qui est peu probable dans les scénarios d’utilisation normale), l’application doit appeler explicitement [**IDirect3DVolumeTexture9 :: AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) sur la texture du volume.

Cette fonction prend en charge les chaînes Unicode et ANSI.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md)
</dt> <dt>

[**D3DXLoadVolumeFromFileInMemory**](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[**D3DXLoadVolumeFromMemory**](d3dxloadvolumefrommemory.md)
</dt> <dt>

[**D3DXLoadVolumeFromVolume**](d3dxloadvolumefromvolume.md)
</dt> <dt>

[Fonctions de texture dans D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
