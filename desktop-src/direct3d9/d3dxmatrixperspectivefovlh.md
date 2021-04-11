---
description: Crée une matrice de projection de perspective pour un système gaucher en fonction d’un champ de vue.
ms.assetid: 90328798-f124-4b61-90a9-971946066b02
title: D3DXMatrixPerspectiveFovLH, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveFovLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 91b25a2e319236485c2c290b55acb94954a4791d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211883"
---
# <a name="d3dxmatrixperspectivefovlh-function-d3dx9mathh"></a>D3DXMatrixPerspectiveFovLH, fonction (D3dx9math. h)

Crée une matrice de projection de perspective pour un système gaucher en fonction d’un champ de vue.

## <a name="syntax"></a>Syntaxe


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.

</dd> <dt>

*fovY* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Champ de vue sur l’axe y, en radians.

</dd> <dt>

*Aspect* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Proportions, défini en tant que largeur d’espace de vue divisée par la hauteur.

</dd> <dt>

*Zn* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Valeur Z du plan de vue proche.

</dd> <dt>

*ZF* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Valeur Z du plan d’affichage Far.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui est une matrice de projection de perspective de gauche.

## <a name="remarks"></a>Notes

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* . De cette façon, la fonction **D3DXMatrixPerspectiveFovLH** peut être utilisée comme paramètre pour une autre fonction.

Pour modifier l’axe des proportions, utilisez la formule de calcul : fovY = 2 * Math. ATAN (Math. Tan (fovY * 0,5)/aspect). Vous pouvez également ajouter des variables de proportions X et Y dans la structure pour mettre à l’échelle l’espace d’affichage vertical : fovY = 2 * Math. ATAN (Math. Tan (fovY * 0,5)/aspecty), aspect = aspectX * aspect Y.

Cette fonction calcule la matrice retournée comme indiqué ci-dessous :


```
xScale     0          0               0
0        yScale       0               0
0          0       zf/(zf-zn)         1
0          0       -zn*zf/(zf-zn)     0
where:
yScale = cot(fovY/2)

xScale = yScale / aspect ratio
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveLH**](d3dxmatrixperspectivelh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveFovRH**](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveOffCenterRH**](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveOffCenterLH**](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
