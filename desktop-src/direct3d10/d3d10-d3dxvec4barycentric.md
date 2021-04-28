---
description: 'D3DXVec4BaryCentric, fonction (D3DX10Math. h) : retourne un point dans les coordonnées Barycentric, à l’aide des vecteurs 4D spécifiés.'
ms.assetid: 44406135-3270-4f2e-bb53-29affb2510f2
title: D3DXVec4BaryCentric, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4BaryCentric
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 935432d1634a7fd35401d92471b1f366075ac8b7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102987"
---
# <a name="d3dxvec4barycentric-function-d3dx10mathh"></a>D3DXVec4BaryCentric, fonction (D3DX10Math. h)

Retourne un point dans les coordonnées Barycentric, à l’aide des vecteurs 4D spécifiés.

## <a name="syntax"></a>Syntaxe


```C++
D3DXVECTOR4* D3DXVec4BaryCentric(
  _In_       D3DXVECTOR4 *pOut,
  _In_ const D3DXVECTOR4 *pV1,
  _In_ const D3DXVECTOR4 *pV2,
  _In_ const D3DXVECTOR4 *pV3,
  _In_       FLOAT       f,
  _In_       FLOAT       g
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ dans\]
</dt> <dd>

Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Pointeur vers le [**D3DXVECTOR4**](d3d10-d3dxvector4.md) qui est le résultat de l’opération.

</dd> <dt>

*pV1* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Pointeur vers une structure D3DXVECTOR4 source.

</dd> <dt>

*pV2* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Pointeur vers une structure D3DXVECTOR4 source.

</dd> <dt>

*pV3* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Pointeur vers une structure D3DXVECTOR4 source.

</dd> <dt>

*f* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Facteur de pondération. Consultez la section Notes.

</dd> <dt>

*g* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Facteur de pondération. Consultez la section Notes.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Pointeur vers une structure D3DXVECTOR4 dans les coordonnées Barycentric.

## <a name="remarks"></a>Notes 

La fonction D3DXVec4BaryCentric fournit un moyen de comprendre les points dans et autour d’un triangle, indépendamment de l’endroit où le triangle est réellement situé. Cette fonction retourne le point résultant à l’aide de l’équation suivante : v1 + f (V2-V1) + g (v3-v1).

Tout point dans le plan V1V2V3 peut être représenté par la coordonnée Barycentric (f, g). Le paramètre f contrôle combien v2 est pondéré dans le résultat et le paramètre g contrôle combien v3 est pondéré dans le résultat. Enfin, 1-f-g contrôle la quantité de v1 qui est pondérée dans le résultat.

Notez les relations suivantes.

-   Si (f>= 0 &, & g>= 0 &, & 1-f-g>= 0), le point se trouve à l’intérieur du triangle V1V2V3.
-   Si (f = = 0 &, & g>= 0 &, & 1-f-g>= 0), le point se trouve sur la ligne V1V3.
-   Si (f>= 0 &, & g = = 0 &, & 1-f-g>= 0), le point se trouve sur la ligne V1V2.
-   Si (f>= 0 &, & g>= 0 &, & 1-f-g = = 0), le point se trouve sur la ligne V2V3.

Les coordonnées Barycentric sont une forme de coordonnées générales. Dans ce contexte, l’utilisation de coordonnées Barycentric représente une modification des systèmes de coordonnées. Ce qui est vrai pour les coordonnées cartésiennes contient la valeur true pour les coordonnées Barycentric.

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, la fonction D3DXVec4BaryCentric peut être utilisée comme paramètre pour une autre fonction.

Les coordonnées Barycentric définissent un point à l’intérieur d’un triangle en termes de sommets du triangle. Pour une description plus détaillée des coordonnées Barycentric, consultez [la description des coordonnées Barycentric de MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
