---
description: Détermine si un rayon entre en intersection avec un sous-ensemble de ce maillage.
ms.assetid: 31f90141-60be-4c7f-8d6a-a1a97ff26d9d
title: ID3DX10Mesh::IntersectSubset, méthode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.IntersectSubset
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f1975c6704faa0fdbf9647b92edff805e7930c0a612fc8e5fb845b8bb26fd4ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069973"
---
# <a name="id3dx10meshintersectsubset-method"></a>ID3DX10Mesh :: IntersectSubset, méthode

Détermine si un rayon entre en intersection avec un sous-ensemble de ce maillage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IntersectSubset(
  [in]  UINT        AttribId,
  [in]  D3DXVECTOR3 *pRayPos,
  [in]  D3DXVECTOR3 *pRayDir,
  [in]  UINT        *pHitCount,
  [in]  UINT        *pFaceIndex,
  [in]  float       *pU,
  [in]  float       *pV,
  [in]  float       *pDist,
  [out] ID3D10Blob  **ppAllHits
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*AttribId* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

ID d’attribut identifiant le sous-ensemble du maillage.

</dd> <dt>

*pRayPos* \[ dans\]
</dt> <dd>

Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Pointeur vers une structure [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , en spécifiant le point de départ du rayon.

</dd> <dt>

*pRayDir* \[ dans\]
</dt> <dd>

Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Pointeur vers une structure [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , en spécifiant la direction du rayon.

</dd> <dt>

*pHitCount* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Nombre de fois que le rayon est croisé avec la maille.

</dd> <dt>

*pFaceIndex* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Pointeur vers une valeur d’index du visage le plus proche de l’origine du rayon, si pHit a la valeur **true**.

</dd> <dt>

*pu* \[ dans\]
</dt> <dd>

Type : **float \***

Pointeur vers une coordonnée d’accès Barycentric, U.

</dd> <dt>

*PV* \[ dans\]
</dt> <dd>

Type : **float \***

Pointeur vers une coordonnée d’accès Barycentric, V.

</dd> <dt>

*pDist* \[ dans\]
</dt> <dd>

Type : **float \***

Pointeur désignant une distance de paramètres d’intersection de rayon.

</dd> <dt>

*ppAllHits* \[ à\]
</dt> <dd>

Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Pointeur vers une [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob), contenant un tableau de structures d' [**\_ \_ informations d’intersection d3dx10**](d3dx10-intersect-info.md) . Il s’agit d’une liste de tous les accès qui se sont produits dans le test d’intersection.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarques

Cette API fournit un moyen de comprendre les points dans et autour d’un triangle, indépendamment de l’endroit où le triangle est réellement situé. Cette fonction retourne le point résultant à l’aide de l’équation suivante : v1 + U (V2-V1) + V (v3-v1).

Tout point dans le plan V1V2V3 peut être représenté par la coordonnée Barycentric (U, V). Le paramètre U contrôle combien v2 est pondéré dans le résultat, et le paramètre V contrôle combien v3 est pondéré dans le résultat. Enfin, la valeur de \[ 1-(U + V) \] contrôle la quantité de valeurs v1 pondérée dans le résultat.

Les coordonnées Barycentric sont une forme de coordonnées générales. Dans ce contexte, l’utilisation de coordonnées Barycentric représente une modification des systèmes de coordonnées. Ce qui est vrai pour les coordonnées cartésiennes contient la valeur true pour les coordonnées Barycentric.

Les coordonnées Barycentric définissent un point à l’intérieur d’un triangle en termes de sommets du triangle. Pour une description plus détaillée des coordonnées Barycentric, consultez [la description des coordonnées Barycentric de MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
