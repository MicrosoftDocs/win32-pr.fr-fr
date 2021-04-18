---
description: Crée une matrice qui aplatit la géométrie dans un plan.
ms.assetid: 83c9e7d6-fc6c-48e7-bbf2-6aa10868351d
title: D3DXMatrixShadow, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixShadow
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a2edaee98f5a56cf5dffec262ecc3d546f0116f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323242"
---
# <a name="d3dxmatrixshadow-function-d3dx10mathh"></a>D3DXMatrixShadow, fonction (D3DX10Math. h)

Crée une matrice qui aplatit la géométrie dans un plan.

## <a name="syntax"></a>Syntaxe


```C++
D3DXMATRIX* D3DXMatrixShadow(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR4 *pLight,
  _In_    const D3DXPLANE   *pPlane
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.

</dd> <dt>

*pLight* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Pointeur vers un [**D3DXVECTOR4**](d3d10-d3dxvector4.md) décrivant la position de la lumière.

</dd> <dt>

*pPlane* \[ dans\]
</dt> <dd>

Type : **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Pointeur vers le [**D3DXPLANE**](d3d10-d3dxplane.md)source.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Pointeur vers une structure D3DXMATRIX qui aplatit la géométrie dans un plan.

## <a name="remarks"></a>Notes

La fonction **D3DXMatrixShadow** aplatit la géométrie dans un plan, comme s’il s’agissait d’une ombre à partir d’une lumière.

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, la fonction **D3DXMatrixShadow** peut être utilisée comme paramètre pour une autre fonction.

Cette fonction utilise la formule suivante pour calculer la matrice retournée.


```
P = normalize(Plane);
L = Light;
d = dot(P, L)
    
P.a * L.x + d  P.a * L.y      P.a * L.z      P.a * L.w  
P.b * L.x      P.b * L.y + d  P.b * L.z      P.b * L.w  
P.c * L.x      P.c * L.y      P.c * L.z + d  P.c * L.w  
P.d * L.x      P.d * L.y      P.d * L.z      P.d * L.w + d
```



Si le composant w de la lumière est égal à 0, le rayon de l’origine à la lumière représente une lumière directionnelle. S’il s’agit de 1, la lumière est une lumière de point.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
