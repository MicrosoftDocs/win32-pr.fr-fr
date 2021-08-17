---
description: Récupère les coordonnées Barycentric texels.
ms.assetid: f380a37f-b9c1-4433-b1d6-e9feeca79b30
title: 'ID3DXTextureGutterHelper :: GetBaryMap, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4183bf9bfa5065595073b8534e978367c3ec16bf76245d639da81292641afa81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729198"
---
# <a name="id3dxtexturegutterhelpergetbarymap-method"></a>ID3DXTextureGutterHelper :: GetBaryMap, méthode

Récupère les coordonnées Barycentric texels.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetBaryMap(
  [in, out] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pBaryData* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) qui contient les deux premières coordonnées Barycentric de chaque Texel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Remarques

La troisième coordonnée Barycentric est donnée par :


```
    1 - ( pBaryData.x + pBaryData.y )
```



Les coordonnées Barycentric sont toujours spécifiées en ce qui concerne le triangle retourné par [**ID3DXTextureGutterHelper :: GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md).

Les coordonnées Barycentric retournées par cette méthode sont valides uniquement pour les texels valides (non de classe 0). [**ID3DXTextureGutterHelper :: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) retourne des valeurs non nulles pour les texels valides.

Les [**texels de classe 2**](id3dxtexturegutterhelper.md) sont mappés au point le plus proche sur le triangle dans l’espace Texel.

L’application doit allouer et gérer pBaryData.

Les coordonnées Barycentric définissent un point à l’intérieur d’un triangle en termes de sommets du triangle. Pour une description plus détaillée des coordonnées Barycentric, consultez [la description des coordonnées Barycentric de MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




