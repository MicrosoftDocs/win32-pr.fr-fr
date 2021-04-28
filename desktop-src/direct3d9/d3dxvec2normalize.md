---
description: 'D3DXVec2Normalize, fonction (D3dx9math. h) : retourne la version normalisée d’un vecteur 2D.'
ms.assetid: 2796a5d1-cb1c-4093-87f2-a2ad43279d91
title: D3DXVec2Normalize, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3322981be5c266bee20a61e85302cb22538a7b0d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097967"
---
# <a name="d3dxvec2normalize-function-d3dx9mathh"></a>D3DXVec2Normalize, fonction (D3dx9math. h)

Retourne la version normalisée d’un vecteur 2D.

## <a name="syntax"></a>Syntaxe


```C++
D3DXVECTOR2* D3DXVec2Normalize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Pointeur vers la structure [**D3DXVECTOR2**](d3dxvector2.md) qui est le résultat de l’opération.

</dd> <dt>

*PV* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Pointeur vers la structure [**D3DXVECTOR2**](d3dxvector2.md) source.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) qui est la version normalisée du vecteur.

## <a name="remarks"></a>Notes 

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* . De cette façon, la fonction **D3DXVec2Normalize** peut être utilisée comme paramètre pour une autre fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




