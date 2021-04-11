---
description: Définit les coordonnées Barycentric texels.
ms.assetid: 6c7c74aa-71a3-45aa-9b18-6409fbd63bda
title: 'ID3DXTextureGutterHelper :: SetBaryMap, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5e3de61913041a4e59e075ea42dacc308c1ce5f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211906"
---
# <a name="id3dxtexturegutterhelpersetbarymap-method"></a>ID3DXTextureGutterHelper :: SetBaryMap, méthode

Définit les coordonnées Barycentric texels.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetBaryMap(
  [in] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pBaryData* \[ dans\]
</dt> <dd>

Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) qui contient les deux premières coordonnées Barycentric de chaque Texel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Notes

La troisième coordonnée Barycentric est donnée par :


```
1 - ( pBaryData.x + pBaryData.y )
```



L’entrée de coordonnées Barycentric pour cette méthode est valide uniquement pour les texels valides (non de classe 0). [**ID3DXTextureGutterHelper :: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) retourne des valeurs non nulles pour les texels valides.

Les coordonnées Barycentric définissent un point à l’intérieur d’un triangle en termes de sommets du triangle. Pour une description plus détaillée des coordonnées Barycentric, consultez [la description des coordonnées Barycentric de MathWorld](http://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




