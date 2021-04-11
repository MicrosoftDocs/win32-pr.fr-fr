---
description: Utilise l’efficacité du traçage de rayon dans les simulations de transfert luminance (PRT) précalculées pour déterminer si un rayon croise une maille.
ms.assetid: e506aed3-bf14-4f29-845b-2091f5b00950
title: 'ID3DXPRTEngine :: ClosestRayIntersects, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ClosestRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4fd802f636077c9ec2a9f0f1060ffd43493aabf1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211921"
---
# <a name="id3dxprtengineclosestrayintersects-method"></a>ID3DXPRTEngine :: ClosestRayIntersects, méthode

Utilise l’efficacité du traçage de rayon dans les simulations de transfert luminance (PRT) précalculées pour déterminer si un rayon croise une maille. Si une intersection est trouvée, la méthode retourne l’index du trait de filet le plus proche atteint par le rayon et les coordonnées Barycentric du point d’intersection.

## <a name="syntax"></a>Syntaxe


```C++
BOOL ClosestRayIntersects(
  [in]  const D3DXVECTOR3 *pRayPos,
  [in]  const D3DXVECTOR3 *pRayDir,
  [in]        DWORD       *pFaceIndex,
  [out]       FLOAT       *pU,
  [out]       FLOAT       *pV,
  [out]       FLOAT       *pDist
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pRayPos* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , en spécifiant le point de départ du rayon.

</dd> <dt>

*pRayDir* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , en spécifiant la direction normalisée du rayon.

</dd> <dt>

*pFaceIndex* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur vers l’index du visage de maillage actuel qui est atteint pour la première fois par le rayon donné, en se basant sur l’empilement de tous les visages de maillage de blocage devant le maillage actuel.

</dd> <dt>

*pu* \[ à\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers une coordonnée d’accès Barycentric, U, pour le vertex 0 du triangle.

</dd> <dt>

*PV* \[ à\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers une coordonnée d’accès Barycentric, V, pour le vertex 1 du triangle.

</dd> <dt>

*pDist* \[ à\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur désignant la distance entre le point d’intersection et le rayon.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **bool**](../winprog/windows-data-types.md)**

Retourne la **valeur true** si le rayon croise le maillage actuel ; Sinon, retourne **false**.

## <a name="remarks"></a>Notes

Utilisez [**ID3DXPRTEngine :: SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) pour définir les distances minimale et maximale de l’intersection avec le rayon.

La coordonnée Barycentric du troisième vertex (Vertex 2) du triangle est 1-(U + V).

Cette méthode s’exécute plus lentement que [**ID3DXPRTEngine :: ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md). Utilisez **ID3DXPRTEngine :: ShadowRayIntersects** si l’emplacement du point d’intersection n’est pas nécessaire.

Les coordonnées Barycentric définissent un point à l’intérieur d’un triangle en termes de sommets du triangle. Pour une description plus détaillée des coordonnées Barycentric, consultez [la description des coordonnées Barycentric de MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md)
</dt> <dt>

[**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
