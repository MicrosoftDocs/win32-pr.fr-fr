---
description: Reçoit une valeur de classe Texel qui indique la classe Texel en fonction de l’emplacement de chaque Texel.
ms.assetid: 450739a8-e30c-4e56-9560-8cb705a75672
title: 'ID3DXTextureGutterHelper :: GetGutterMap, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d973e716c598eaceaf7f75e6694a35691df4266
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120397"
---
# <a name="id3dxtexturegutterhelpergetguttermap-method"></a>ID3DXTextureGutterHelper :: GetGutterMap, méthode

Reçoit une valeur de classe Texel qui indique la classe Texel en fonction de l’emplacement de chaque Texel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetGutterMap(
  [in, out] BYTE *pGutterData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pGutterData* \[ in, out\]
</dt> <dd>

Type : **[ **Byte**](../winprog/windows-data-types.md)\***

Pointeur désignant la classe Texel. Les classes Texel possibles sont les suivantes. Il n’existe pas de classe Texel 3.



| Texel (classe) | Emplacement de Texel                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0           | Point non valide ; Texel ne sera pas utilisé.                                                                                                                                                                                                                                                                                                                                        |
| 1           | Triangle intérieur.                                                                                                                                                                                                                                                                                                                                                              |
| 2           | Marge intérieure.                                                                                                                                                                                                                                                                                                                                                                |
| 4           | Marge intérieure ; Texel sera évalué comme un exemple complet dans les méthodes [**ID3DXTextureGutterHelper :: ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper :: ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)ou [**ID3DXTextureGutterHelper :: ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) . |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Notes

L’application doit allouer et gérer des pGutterData, avec la taille donnée par :


```
texture width * texture height * sizeof(BYTE)
```



La largeur et la hauteur de la texture sont retournées par [**ID3DXTextureGutterHelper :: GetWidth**](id3dxtexturegutterhelper--getwidth.md) et [**ID3DXTextureGutterHelper :: GetHeight**](id3dxtexturegutterhelper--getheight.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
