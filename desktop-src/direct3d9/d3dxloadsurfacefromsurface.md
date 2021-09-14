---
description: Charge une surface à partir d’une autre surface avec la conversion de couleurs.
ms.assetid: eddb420d-fd32-4c09-afec-435887c4e905
title: D3DXLoadSurfaceFromSurface, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromSurface
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b5138ddf540c3e4a87fe65f29938cb3557b2360
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921395"
---
# <a name="d3dxloadsurfacefromsurface-function"></a>D3DXLoadSurfaceFromSurface fonction)

Charge une surface à partir d’une autre surface avec la conversion de couleurs.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXLoadSurfaceFromSurface(
  _In_       LPDIRECT3DSURFACE9 pDestSurface,
  _In_ const PALETTEENTRY       *pDestPalette,
  _In_ const RECT               *pDestRect,
  _In_       LPDIRECT3DSURFACE9 pSrcSurface,
  _In_ const PALETTEENTRY       *pSrcPalette,
  _In_ const RECT               *pSrcRect,
  _In_       DWORD              Filter,
  _In_       D3DCOLOR           ColorKey
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDestSurface* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**

Pointeur vers une interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) . Spécifie la surface de destination, qui reçoit l’image.

</dd> <dt>

*pDestPalette* \[ dans\]
</dt> <dd>

Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la palette de destination de 256 couleurs ou **null**.

</dd> <dt>

*pDestRect* \[ dans\]
</dt> <dd>

Type : **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) . Spécifie le rectangle de destination. Affectez la valeur **null** à ce paramètre pour spécifier la surface entière.

</dd> <dt>

*pSrcSurface* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**

Pointeur vers une interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) représentant la surface source.

</dd> <dt>

*pSrcPalette* \[ dans\]
</dt> <dd>

Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la palette source de 256 couleurs ou **null**.

</dd> <dt>

*pSrcRect* \[ dans\]
</dt> <dd>

Type : **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) . Spécifie le rectangle source. Affectez la valeur **null** à ce paramètre pour spécifier la surface entière.

</dd> <dt>

*Filtre* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison d’un ou de plusieurs [ \_ filtres D3DX](d3dx-filter.md), qui contrôle la façon dont l’image est filtrée. La spécification \_ de la valeur D3DX par défaut pour ce paramètre revient à spécifier la valeur de filtre du \_ triangle de filtre D3DX \_ \| \_ \_ .

</dd> <dt>

*ColorKey* \[ dans\]
</dt> <dd>

Type : **[ **D3DCOLOR**](d3dcolor.md)**

Valeur [**D3DCOLOR**](d3dcolor.md) à remplacer par le noir transparent, ou 0 pour désactiver le ColorKey. Il s’agit toujours d’une couleur ARVB de 32 bits, indépendante du format d’image source. Alpha est significatif et doit généralement être défini sur FF pour les clés de couleur opaques. Ainsi, pour le noir opaque, la valeur est égale à 0xFF000000.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="remarks"></a>Notes

Cette fonction gère la conversion vers et à partir des formats de texture compressés.

L’écriture sur une surface non-niveau zéro n’entraîne pas la mise à jour du rectangle de modification. Si **D3DXLoadSurfaceFromSurface** est appelé et que la surface n’était pas encore modifiée (ce qui est peu probable dans les scénarios d’utilisation normale), l’application doit appeler explicitement [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) sur l’aire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de texture dans D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
