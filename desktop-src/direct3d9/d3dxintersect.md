---
description: Détermine si un rayon croise une maille.
ms.assetid: 325f5b40-80ba-4400-a143-bae41146ab07
title: D3DXIntersect, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc877fb1301e01b05184625ba2e92a2c680cfa9f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921439"
---
# <a name="d3dxintersect-function"></a>D3DXIntersect fonction)

Détermine si un rayon croise une maille.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXIntersect(
  _In_        LPD3DXBASEMESH pMesh,
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

Pointeur vers une interface [**ID3DXBaseMesh**](id3dxbasemesh.md) représentant le maillage à tester.

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

Pointeur vers un objet [**ID3DXBuffer**](id3dxbuffer.md) , contenant un tableau de structures [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) .

</dd> <dt>

*pCountOfHits* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur vers une valeur DWORD qui contient le nombre d’entrées dans le tableau ppAllHits.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être : E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

La fonction **D3DXIntersect** fournit un moyen de comprendre les points dans et autour d’un triangle, indépendamment de l’endroit où le triangle est réellement situé. Cette fonction retourne le point résultant à l’aide de l’équation suivante : v1 + U (V2-V1) + V (v3-v1).

Tout point dans le plan V1V2V3 peut être représenté par la coordonnée Barycentric (U, V). Le paramètre U contrôle combien v2 est pondéré dans le résultat, et le paramètre V contrôle combien v3 est pondéré dans le résultat. Enfin, la valeur de \[ 1-(U + V) \] contrôle la quantité de valeurs v1 pondérée dans le résultat.

Les coordonnées Barycentric sont une forme de coordonnées générales. Dans ce contexte, l’utilisation de coordonnées Barycentric représente une modification des systèmes de coordonnées. Ce qui est vrai pour les coordonnées cartésiennes contient la valeur true pour les coordonnées Barycentric.

Les coordonnées Barycentric définissent un point à l’intérieur d’un triangle en termes de sommets du triangle. Pour une description plus détaillée des coordonnées Barycentric, consultez [la description des coordonnées Barycentric de MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
