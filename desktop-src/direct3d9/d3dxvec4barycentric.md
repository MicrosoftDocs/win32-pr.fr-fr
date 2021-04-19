---
description: Retourne un point dans les coordonnées Barycentric, à l’aide des vecteurs 4D spécifiés.
ms.assetid: 80d73232-76bf-4f40-add2-dd1bdcc5cd98
title: D3DXVec4BaryCentric, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4BaryCentric
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 75f0d068d1545f1b8b55dc3b976d3585e6f9bc88
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545291"
---
# <a name="d3dxvec4barycentric-function-d3dx9mathh"></a>D3DXVec4BaryCentric, fonction (D3dx9math. h)

Retourne un point dans les coordonnées Barycentric, à l’aide des vecteurs 4D spécifiés.

## <a name="syntax"></a>Syntaxe


```C++
D3DXVECTOR4* D3DXVec4BaryCentric(
  _Out_       D3DXVECTOR4 *pOut,
  _In_  const D3DXVECTOR4 *pV1,
  _In_  const D3DXVECTOR4 *pV2,
  _In_  const D3DXVECTOR4 *pV3,
  _In_        FLOAT       f,
  _In_        FLOAT       g
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ à\]
</dt> <dd>

Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Pointeur vers la structure [**D3DXVECTOR4**](d3dxvector4.md) qui est le résultat de l’opération.

</dd> <dt>

*pV1* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) source.

</dd> <dt>

*pV2* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) source.

</dd> <dt>

*pV3* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) source.

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

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) dans les coordonnées Barycentric.

## <a name="remarks"></a>Notes

La fonction **D3DXVec4BaryCentric** fournit un moyen de comprendre les points dans et autour d’un triangle, indépendamment de l’endroit où le triangle est réellement situé. Cette fonction retourne le point résultant à l’aide de l’équation suivante : v1 + f (V2-V1) + g (v3-v1).

Tout point dans le plan V1V2V3 peut être représenté par la coordonnée Barycentric (f, g). Le paramètre *f* contrôle combien v2 est pondéré dans le résultat et le paramètre *g* contrôle combien v3 est pondéré dans le résultat. Enfin, 1-f-g contrôle la quantité de v1 qui est pondérée dans le résultat.

Notez les relations suivantes.

-   Si (f>= 0 &, & g>= 0 &, & 1-f-g>= 0), le point se trouve à l’intérieur du triangle V1V2V3.
-   Si (f = = 0 &, & g>= 0 &, & 1-f-g>= 0), le point se trouve sur la ligne V1V3.
-   Si (f>= 0 &, & g = = 0 &, & 1-f-g>= 0), le point se trouve sur la ligne V1V2.
-   Si (f>= 0 &, & g>= 0 &, & 1-f-g = = 0), le point se trouve sur la ligne V2V3.

Les coordonnées Barycentric sont une forme de coordonnées générales. Dans ce contexte, l’utilisation de coordonnées Barycentric représente une modification des systèmes de coordonnées. Ce qui est vrai pour les coordonnées cartésiennes contient la valeur true pour les coordonnées Barycentric.

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* . De cette façon, la fonction **D3DXVec4BaryCentric** peut être utilisée comme paramètre pour une autre fonction.

Les coordonnées Barycentric définissent un point à l’intérieur d’un triangle en termes de sommets du triangle. Pour une description plus détaillée des coordonnées Barycentric, consultez [la description des coordonnées Barycentric de MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
