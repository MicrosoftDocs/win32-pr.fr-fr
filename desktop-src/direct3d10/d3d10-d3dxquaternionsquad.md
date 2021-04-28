---
description: 'Fonction D3DXQuaternionSquad (D3DX10Math. h) : interpole entre les quaternions, à l’aide de l’interpolation Quadrangle sphérique.'
ms.assetid: ba953731-4372-4b32-942b-23abfe479704
title: D3DXQuaternionSquad, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquad
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9671b2a161124228c264da7eac0a2aa3a915ff95
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108757"
---
# <a name="d3dxquaternionsquad-function-d3dx10mathh"></a>D3DXQuaternionSquad, fonction (D3DX10Math. h)

Interpole entre les quaternions, à l’aide de l’interpolation sphérique Quadrangle.

## <a name="syntax"></a>Syntaxe


```C++
D3DXQUATERNION* D3DXQuaternionSquad(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pA,
  _In_    const D3DXQUATERNION *pB,
  _In_    const D3DXQUATERNION *pC,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Pointeur vers le [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) qui est le résultat de l’opération.

</dd> <dt>

*pQ1* \[ dans\]
</dt> <dd>

Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Pointeur vers une structure D3DXQUATERNION source.

</dd> <dt>

*PA* \[ dans\]
</dt> <dd>

Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Pointeur vers une structure D3DXQUATERNION source.

</dd> <dt>

*PB* \[ dans\]
</dt> <dd>

Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Pointeur vers une structure D3DXQUATERNION source.

</dd> <dt>

*ordinateur* \[ dans\]
</dt> <dd>

Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Pointeur vers une structure D3DXQUATERNION source.

</dd> <dt>

*t* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Paramètre qui indique la distance à interpoler entre les quaternions.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Pointeur vers une structure D3DXQUATERNION qui est le résultat de l’interpolation sphérique Quadrangle.

## <a name="remarks"></a>Notes 

Cette fonction utilise la séquence suivante d’opérations d’interpolation linéaire sphérique :


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, la fonction D3DXQuaternionSquad peut être utilisée comme paramètre pour une autre fonction.

Utilisez [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
