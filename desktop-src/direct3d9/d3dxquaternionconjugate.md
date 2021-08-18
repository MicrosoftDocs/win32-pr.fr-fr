---
description: Retourne le conjugué d’un Quaternion.
ms.assetid: f690fdd8-7805-4fc1-9064-4f249d5f7c4f
title: D3DXQuaternionConjugate, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionConjugate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cb4828d6e6dec80e8721b4e5bddd4728da7a72dc0c6ea9a9c315800e0b17fa00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988459"
---
# <a name="d3dxquaternionconjugate-function"></a>D3DXQuaternionConjugate fonction)

Retourne le conjugué d’un Quaternion.

## <a name="syntax"></a>Syntaxe


```C++
D3DXQUATERNION* D3DXQuaternionConjugate(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le résultat de l’opération.

</dd> <dt>

*PQ* \[ dans\]
</dt> <dd>

Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) source.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le conjugué du Quaternion.

## <a name="remarks"></a>Remarques

À partir d’un Quaternion (x, y, z, w), la fonction **D3DXQuaternionConjugate** retourne le Quaternion (-x,-y,-z, w).

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* . De cette façon, la fonction **D3DXQuaternionConjugate** peut être utilisée comme paramètre pour une autre fonction.

Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionInverse**](d3dxquaternioninverse.md)
</dt> </dl>

 

 




