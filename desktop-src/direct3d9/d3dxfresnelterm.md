---
description: 'Fonction D3DXFresnelTerm (D3dx9math. h) : calcule le terme de la Fresnel.'
ms.assetid: d3d281db-91a1-4100-8a82-028554b5a91d
title: D3DXFresnelTerm, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFresnelTerm
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5472f9839928fd3b4c1830bc309c7f610d487864
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012783"
---
# <a name="d3dxfresnelterm-function-d3dx9mathh"></a>D3DXFresnelTerm, fonction (D3dx9math. h)

Calculez le terme de la Fresnel.

## <a name="syntax"></a>Syntaxe


```C++
FLOAT D3DXFresnelTerm(
  _In_ FLOAT CosTheta,
  _In_ FLOAT RefractionIndex
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CosTheta* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Elle doit être comprise entre 0 et 1.

</dd> <dt>

*RefractionIndex* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Index de réfraction d’un matériau. La valeur doit être supérieure à 1.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **float**](../winprog/windows-data-types.md)**

Cette fonction retourne le terme de Fresnel pour la lumière dépolarisée. CosTheta est le cosinus de l’angle d’incident.

## <a name="remarks"></a>Notes

Pour rechercher le terme de la Fresnel (F) :

Si un est un angle d’incidence et que B est l’angle de réfraction, alors


```
F = 0.5 * [tan2(A - B) / tan2(A + B) + sin2(A - B) / sin2(A + B)]
  = 0.5 * sin2(A - B) / sin2(A + B) * [cos2(A + B) / cos2(A - B) + 1]
    
Let r   = sina(A) / sin(B)      (the relative refractive index)
Let c   = cos(A)
Let g   = (r2 + c2 - 1)1/2
```



Ensuite, en développant à l’aide des identités trig et en simplifiant, vous bénéficiez des éléments suivants :


```
F = 0.5 * (g + c)2 / (g - c)2 * ([c(g + c) - 1]2 / [c(g - c) + 1]2 + 1)
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
