---
description: Charge un volume à partir de la mémoire.
ms.assetid: 9f74fcc0-f935-4466-865b-e798711a1f2f
title: D3DXLoadVolumeFromMemory, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d6c3f1bdfe40f19eeb57b4f0d8a38c40a239404
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921384"
---
# <a name="d3dxloadvolumefrommemory-function"></a>D3DXLoadVolumeFromMemory fonction)

Charge un volume à partir de la mémoire.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXLoadVolumeFromMemory(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCVOID           pSrcMemory,
  _In_       D3DFORMAT         SrcFormat,
  _In_       UINT              SrcRowPitch,
  _In_       UINT              SrcSlicePitch,
  _In_ const PALETTEENTRY      *pSrcPalette,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDestVolume* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**

Pointeur vers une interface [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) . Spécifie le volume de destination, qui reçoit l’image.

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

*pSrcMemory* \[ dans\]
</dt> <dd>

Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**

Pointeur vers l’angle supérieur gauche du volume source en mémoire.

</dd> <dt>

*SrcFormat* \[ dans\]
</dt> <dd>

Type : **[D3DFORMAT](d3dformat.md)**

Membre du type énuméré [D3DFORMAT](d3dformat.md) , format de pixel du volume source.

</dd> <dt>

*SrcRowPitch* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Hauteur de l’image source, en octets. Pour les formats DXT (formats de texture compressés), ce nombre doit représenter la taille d’une ligne de cellules, en octets.

</dd> <dt>

*SrcSlicePitch* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Hauteur de l’image source, en octets. Pour les formats DXT (formats de texture compressés), ce nombre doit représenter la taille d’une tranche de cellules, en octets.

</dd> <dt>

*pSrcPalette* \[ dans\]
</dt> <dd>

Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la palette source de 256 couleurs ou **null**.

</dd> <dt>

*pSrcBox* \[ dans\]
</dt> <dd>

Type : **const [**D3DBOX**](d3dbox.md) \***

Pointeur vers une structure [**D3DBOX**](d3dbox.md) . Spécifie la zone source. **Null** n’est pas une valeur valide pour ce paramètre.

</dd> <dt>

*Filtre* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison d’un ou de plusieurs [ \_ filtres D3DX](d3dx-filter.md) contrôlant la façon dont l’image est filtrée. La spécification \_ de la valeur D3DX par défaut pour ce paramètre revient à spécifier la valeur de filtre du \_ triangle de filtre D3DX \_ \| \_ \_ .

</dd> <dt>

*ColorKey* \[ dans\]
</dt> <dd>

Type : **[ **D3DCOLOR**](d3dcolor.md)**

Valeur [**D3DCOLOR**](d3dcolor.md) à remplacer par le noir transparent, ou 0 pour désactiver le ColorKey. Il s’agit toujours d’une couleur ARVB de 32 bits, indépendante du format d’image source. Alpha est significatif et doit généralement être défini sur FF pour les clés de couleur opaques. Ainsi, pour le noir opaque, la valeur est égale à 0xFF000000.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="remarks"></a>Notes

L’écriture sur une surface non-niveau zéro de la texture du volume n’entraîne pas la mise à jour du rectangle de modification. Si **D3DXLoadVolumeFromMemory** est appelé et que la texture n’a pas déjà été modifiée (ce qui est peu probable dans les scénarios d’utilisation normale), l’application doit appeler explicitement [**IDirect3DVolumeTexture9 :: AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) sur la texture du volume.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md)
</dt> <dt>

[**D3DXLoadVolumeFromResource**](d3dxloadvolumefromresource.md)
</dt> <dt>

[**D3DXLoadVolumeFromVolume**](d3dxloadvolumefromvolume.md)
</dt> <dt>

[Fonctions de texture dans D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
