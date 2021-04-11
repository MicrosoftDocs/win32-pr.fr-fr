---
description: Croise le rayon spécifié avec le sous-ensemble de maillage donné. Cela offre des fonctionnalités similaires à D3DXIntersect.
ms.assetid: 4a757b9e-18eb-424e-9f3e-cdf917c23787
title: D3DXIntersectSubset, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersectSubset
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 621f45d7c2a6d8ff162f539ef62153d3ae70f6e9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211757"
---
# <a name="d3dxintersectsubset-function"></a>D3DXIntersectSubset fonction)

Croise le rayon spécifié avec le sous-ensemble de maillage donné. Cela offre des fonctionnalités similaires à [**D3DXIntersect**](d3dxintersect.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXIntersectSubset(
  _In_        LPD3DXBASEMESH pMesh,
  _In_        DWORD          AttribId,
  _In_  const D3DXVECTOR3    *pRayPos,
  _In_  const D3DXVECTOR3    *pRayDir,
  _Out_       BOOL           *pHit,
  _Out_       DWORD          *pFaceIndex,
  _Out_       FLOAT          *pU,
  _Out_       FLOAT          *pV,
  _Out_       FLOAT          *pDist,
  _Out_       LPD3DXBUFFER   *ppAllHits,
  _Out_       DWORD          *pCountOfHits
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMesh* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Pointeur vers une interface [**ID3DXBaseMesh**](id3dxbasemesh.md) représentant le maillage à tester. La maille doit être triée par attribut.

</dd> <dt>

*AttribId* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Identificateur d’attribut du sous-ensemble avec lequel effectuer l’intersection.

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

*pHit* \[ à\]
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)\***

Pointeur vers un booléen. Si le rayon croise une face triangulaire sur le maillage, cette valeur est définie sur **true**. Sinon, cette valeur est définie sur **false**.

</dd> <dt>

*pFaceIndex* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur vers une valeur d’index du visage le plus proche de l’origine du rayon, si pHit a la valeur **true**.

</dd> <dt>

*pu* \[ à\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers une coordonnée d’accès Barycentric, U.

</dd> <dt>

*PV* \[ à\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers une coordonnée d’accès Barycentric, V.

</dd> <dt>

*pDist* \[ à\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur désignant une distance de paramètres d’intersection de rayon.

</dd> <dt>

*ppAllHits* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Tableau de structures [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) , représentant tous les accès, pas seulement les correspondances les plus proches.

</dd> <dt>

*pCountOfHits* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Nombre d’éléments dans le tableau retourné par ppAllHits.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être la valeur suivante : E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

La fonction **D3DXIntersectSubset** fournit un moyen de comprendre les points dans et autour d’un triangle, indépendamment de l’endroit où le triangle est réellement situé. Cette fonction retourne le point résultant à l’aide de l’équation suivante : v1 + U (V2-V1) + V (v3-v1).

Tout point dans le plan V1V2V3 peut être représenté par la coordonnée Barycentric (U, V). Le paramètre U contrôle combien v2 est pondéré dans le résultat et le paramètre V contrôle combien v3 est pondéré dans le résultat. Enfin, la valeur de \[ 1-(U + V) \] contrôle la quantité de valeurs v1 pondérée dans le résultat.

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

 

 
