---
description: 'Fonction D3DXQuaternionExp (D3dx9math. h) : calcule la valeur exponentielle.'
ms.assetid: 648aeaf1-ead3-4b21-819f-cd2a70881a13
title: D3DXQuaternionExp, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionExp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2a69364e3cb294f088023d7e67973fb55f6e3396987ee9b63e9f9383dcf81917
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044740"
---
# <a name="d3dxquaternionexp-function-d3dx9mathh"></a>D3DXQuaternionExp, fonction (D3dx9math. h)

Calcule la valeur exponentielle.

## <a name="syntax"></a>Syntaxe


```C++
D3DXQUATERNION* D3DXQuaternionExp(
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

Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est l’exponentiel.

## <a name="remarks"></a>Remarques

Cette méthode convertit un Quaternion pur en un Quaternion d’unité. **D3DXQuaternionExp** attend un Quaternion pur, où w est ignoré dans le calcul (w = = 0).


```
Given a pure quaternion defined by:
q = (0, theta * v); 
    
This method calculates the exponential result.
exp(Q) = (cos(theta), sin(theta) * v)
```



où v est la partie vectorielle d’un Quaternion.

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* . De cette façon, la fonction **D3DXQuaternionExp** peut être utilisée comme paramètre pour une autre fonction.

La méthode [**D3DXQuaternionSquadSetup**](d3dxquaternionsquadsetup.md) peut également être utilisée pour configurer les points de contrôle d’un Quaternion.

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

[**D3DXQuaternionLn**](d3dxquaternionln.md)
</dt> <dt>

[**D3DXQuaternionSquad**](d3dxquaternionsquad.md)
</dt> </dl>

 

 




