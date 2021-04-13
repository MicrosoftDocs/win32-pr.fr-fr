---
description: Retourne la version normalisée d’un vecteur 4D.
ms.assetid: ed3c48cf-4985-4ef3-b733-f8532e3ff6b5
title: D3DXVec4Normalize, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Normalize
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: ebedbdddbe558bfad71520b64aa0cf2ff4c2f451
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323094"
---
# <a name="d3dxvec4normalize-function-d3dx10mathh"></a>D3DXVec4Normalize, fonction (D3DX10Math. h)

Retourne la version normalisée d’un vecteur 4D.

## <a name="syntax"></a>Syntaxe


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Pointeur vers le [**D3DXVECTOR4**](d3d10-d3dxvector4.md) qui est le résultat de l’opération.

</dd> <dt>

*PV* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Pointeur vers la structure D3DXVECTOR4 source.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Pointeur vers une structure D3DXVECTOR4 qui est la version normalisée du vecteur.

## <a name="remarks"></a>Notes

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, la fonction D3DXVec4Normalize peut être utilisée comme paramètre pour une autre fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
