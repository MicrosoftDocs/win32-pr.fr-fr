---
description: Définit une valeur de classe Texel qui indique la classe Texel en fonction de l’emplacement de chaque Texel.
ms.assetid: cb2e6afb-4b6a-4b01-aaa8-1fd2d1f2bfa1
title: 'ID3DXTextureGutterHelper :: SetGutterMap, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8d3c0b7c7e33664f3e078eca82a6f39b1294992a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403419"
---
# <a name="id3dxtexturegutterhelpersetguttermap-method"></a>ID3DXTextureGutterHelper :: SetGutterMap, méthode

Définit une valeur de classe Texel qui indique la classe Texel en fonction de l’emplacement de chaque Texel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetGutterMap(
  [in] BYTE *pGutterData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pGutterData* \[ dans\]
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
