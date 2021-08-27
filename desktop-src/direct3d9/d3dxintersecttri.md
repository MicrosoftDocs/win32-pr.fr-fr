---
description: D3DXIntersectTri, fonction (D3DX9Mesh. h)-calcule l’intersection d’un rayon et d’un triangle.
ms.assetid: f335a71d-7203-4ea1-a6bf-407b28c712e6
title: D3DXIntersectTri, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersectTri
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fcb542c5c7bb4edb4dafffa1254b76504aaf0f256a9d694db9d55724f2c94c2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069279"
---
# <a name="d3dxintersecttri-function-d3dx9meshh"></a>D3DXIntersectTri, fonction (D3DX9Mesh. h)

Calcule l’intersection d’un rayon et d’un triangle.

## <a name="syntax"></a>Syntaxe


```C++
BOOL D3DXIntersectTri(
  _In_  const D3DXVECTOR3 *p0,
  _In_  const D3DXVECTOR3 *p1,
  _In_  const D3DXVECTOR3 *p2,
  _In_  const D3DXVECTOR3 *pRayPos,
  _In_  const D3DXVECTOR3 *pRayDir,
  _Out_       FLOAT       *pU,
  _Out_       FLOAT       *pV,
  _Out_       FLOAT       *pDist
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*P0* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , décrivant la première position du sommet de triangle.

</dd> <dt>

*P1* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur désignant une structure [**D3DXVECTOR3**](d3dxvector3.md) , décrivant la deuxième position du sommet du triangle.

</dd> <dt>

*P2* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur désignant une structure [**D3DXVECTOR3**](d3dxvector3.md) , décrivant la troisième position du sommet de triangle.

</dd> <dt>

*pRayPos* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , en spécifiant le point de départ du rayon.

</dd> <dt>

*pRayDir* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , en spécifiant la direction du rayon.

</dd> <dt>

*pu* \[ à\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Coordonnées d’accès Barycentric, U.

</dd> <dt>

*PV* \[ à\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Coordonnées d’accès Barycentric, V.

</dd> <dt>

*pDist* \[ à\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Distance des paramètres d’intersection de rayon.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **bool**](../winprog/windows-data-types.md)**

Retourne la **valeur true** si le rayon croise la zone du triangle. Sinon, retourne **false**.

## <a name="remarks"></a>Remarques

La fonction [**D3DXIntersect**](d3dxintersect.md) fournit un moyen de comprendre les points dans et autour d’un triangle, indépendamment de l’endroit où le triangle est réellement situé. Cette fonction retourne le point résultant à l’aide de l’équation suivante : v1 + U (V2-V1) + V (v3-v1).

Tout point dans le plan V1V2V3 peut être représenté par la coordonnée Barycentric (U, V). Le paramètre U contrôle combien v2 est pondéré dans le résultat, et le paramètre V contrôle combien v3 est pondéré dans le résultat. Enfin, la valeur de \[ 1-(U + V) \] contrôle la quantité de valeurs v1 pondérée dans le résultat.

Les coordonnées Barycentric sont une forme de coordonnées générales. Dans ce contexte, l’utilisation de coordonnées Barycentric représente une modification des systèmes de coordonnées. Ce qui est vrai pour les coordonnées cartésiennes contient la valeur true pour les coordonnées Barycentric.

Les coordonnées Barycentric définissent un point à l’intérieur d’un triangle en termes de sommets du triangle. Pour une description plus détaillée des coordonnées Barycentric, consultez [la description des coordonnées Barycentric de MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
