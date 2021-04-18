---
description: Crée un objet ID3DXTextureGutterHelper à partir d’une maille d’entrée et de données de texture.
ms.assetid: 1696fc3d-5b35-48cc-a79b-c0d4ed44e420
title: D3DXCreateTextureGutterHelper, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureGutterHelper
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8957649f3cef6ea67932579918163613160ee993
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527107"
---
# <a name="d3dxcreatetexturegutterhelper-function"></a>D3DXCreateTextureGutterHelper fonction)

Crée un objet [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) à partir d’une maille d’entrée et de données de texture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreateTextureGutterHelper(
  _In_    UINT                      Width,
  _In_    UINT                      Height,
  _In_    LPD3DXMESH                pMesh,
  _In_    FLOAT                     GutterSize,
  _Inout_ LPD3DXTEXTUREGUTTERHELPER *ppBuffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Largeur* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Largeur de la texture, en pixels.

</dd> <dt>

*Hauteur* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Hauteur de la texture, en pixels.

</dd> <dt>

*pMesh* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

Pointeur vers un objet de maillage [**ID3DXMesh**](id3dxmesh.md) d’entrée.

</dd> <dt>

*GutterSize* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Nombre de texels permettant de suréchantillonner la texture et de créer la région de la reliure. Doit être au moins égal à 1.

</dd> <dt>

*ppBuffer* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)\***

Pointeur vers un objet [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) à créer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est S \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Utilisez [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) pour transformer une scène en nouvelles coordonnées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de transfert luminance précalculées](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
