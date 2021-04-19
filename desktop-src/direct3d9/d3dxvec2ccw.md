---
description: Retourne le composant z en utilisant le produit croisé de deux vecteurs 2D.
ms.assetid: daec19f2-cd0f-4a68-affc-9a42bda8912c
title: D3DXVec2CCW, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2CCW
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71c6e14171a9e7d12d86c30f05885cecf50ce973
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538971"
---
# <a name="d3dxvec2ccw-function"></a>D3DXVec2CCW fonction)

Retourne le composant z en utilisant le produit croisé de deux vecteurs 2D.

## <a name="syntax"></a>Syntaxe


```C++
FLOAT D3DXVec2CCW(
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pV1* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) source.

</dd> <dt>

*pV2* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) source.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **float**](../winprog/windows-data-types.md)**

Composant z.

## <a name="remarks"></a>Notes

Cette fonction détermine le composant z en déterminant le produit croisé en fonction de la formule suivante : ((x1, y1, 0) Croix (x2, Y2, 0)). Ou comme indiqué dans l’exemple suivant.


```
pV1->x * pV2->y - pV1->y * pV2->x
```



Si la valeur du composant z est positive, le vecteur v2 est dans le sens inverse des aiguilles d’une position dans le vecteur v1. Ces informations sont utiles pour l’élimination des faces arrière.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2Dot**](d3dxvec2dot.md)
</dt> </dl>

 

 
