---
description: Applique des reliures à une mémoire tampon de texture FLOTTante.
ms.assetid: 822483d7-ae62-498a-bce7-3a925ab21c04
title: 'ID3DXTextureGutterHelper :: ApplyGuttersFloat, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ApplyGuttersFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 00ee6eac7328ee5f6adceb5b3966c222509237b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106540927"
---
# <a name="id3dxtexturegutterhelperapplyguttersfloat-method"></a>ID3DXTextureGutterHelper :: ApplyGuttersFloat, méthode

Applique des reliures à une mémoire tampon de texture FLOTTante.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ApplyGuttersFloat(
  [in] FLOAT *pDataIn,
  [in] UINT  *NumCoeffs,
  [in] UINT  *Width,
  [in] UINT  *Height
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDataIn* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers une mémoire tampon de données de texture de type FLOAT.

</dd> <dt>

*NumCoeffs* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Nombre de scalaires par canal de couleurs utilisé en mémoire pour stocker des exemples. Chaque Texel contient des valeurs FLOAT NumCoeffs.

</dd> <dt>

*Largeur* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Largeur de la texture, en pixels, obtenue à partir de [**ID3DXTextureGutterHelper :: GetWidth**](id3dxtexturegutterhelper--getwidth.md).

</dd> <dt>

*Hauteur* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Hauteur de la texture, en pixels, obtenue à partir de [**ID3DXTextureGutterHelper :: GetHeight**](id3dxtexturegutterhelper--getheight.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Notes

Les [**texels de classe 2**](id3dxtexturegutterhelper.md) sont générés par le rééchantillonnage des texels de classe 1 et 4.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
