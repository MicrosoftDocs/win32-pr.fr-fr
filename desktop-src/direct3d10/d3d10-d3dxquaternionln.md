---
description: 'Fonction D3DXQuaternionLn (D3DX10Math. h) : calcule le logarithme népérien.'
ms.assetid: 576cf676-bb42-45ec-8e45-4612a7cdb167
title: D3DXQuaternionLn, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLn
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9abaaa231e424e55e496b7901882e9da17c59786
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103207"
---
# <a name="d3dxquaternionln-function-d3dx10mathh"></a>D3DXQuaternionLn, fonction (D3DX10Math. h)

Calcule le logarithme népérien.

## <a name="syntax"></a>Syntaxe


```C++
D3DXQUATERNION* D3DXQuaternionLn(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Pointeur vers le [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) qui est le résultat de l’opération.

</dd> <dt>

*PQ* \[ dans\]
</dt> <dd>

Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Pointeur vers la structure D3DXQUATERNION source.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Pointeur vers une structure D3DXQUATERNION qui est le logarithme népérien.

## <a name="remarks"></a>Notes 

La fonction D3DXQuaternionLn fonctionne uniquement pour les quaternions d’unité.


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, la fonction D3DXQuaternionLn peut être utilisée comme paramètre pour une autre fonction.

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

 

 
