---
description: 'D3DXMatrixOrthoOffCenterLH, fonction (D3DX10Math. h) : génère une matrice de projection orthographique personnalisée de gauche.'
ms.assetid: 84175c08-5a0b-4183-afe2-8aecafd73897
title: D3DXMatrixOrthoOffCenterLH, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2eb10963372519827eb544371ebb0df04df2e178
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109137"
---
# <a name="d3dxmatrixorthooffcenterlh-function-d3dx10mathh"></a>D3DXMatrixOrthoOffCenterLH, fonction (D3DX10Math. h)

Crée une matrice de projection orthographique personnalisée de gauche.

## <a name="syntax"></a>Syntaxe


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Pointeur vers le [**D3DXMATRIX**](d3d10-d3dxmatrix.md)résultant.

</dd> <dt>

*l* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Valeur x minimale du volume de la vue.

</dd> <dt>

*r* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Valeur x maximale du volume de la vue.

</dd> <dt>

*b* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Valeur y minimale du volume de la vue.

</dd> <dt>

*t* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Valeur y maximale du volume de la vue.

</dd> <dt>

*Zn* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Valeur z minimale du volume de la vue.

</dd> <dt>

*ZF* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Valeur z maximale du volume de la vue.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Pointeur vers le [**D3DXMATRIX**](d3d10-d3dxmatrix.md)résultant.

## <a name="remarks"></a>Notes 

Le [**D3DXMatrixOrthoLH**](d3d10-d3dxmatrixortholh.md) est un cas spécial de la fonction D3DXMatrixOrthoOffCenterLH. Pour créer la même projection à l’aide de D3DXMatrixOrthoOffCenterLH, utilisez les valeurs suivantes :

l =-w/2,

r = w/2,

b =-h/2 et

t = h/2.

Tous les paramètres de la fonction D3DXMatrixOrthoOffCenterLH sont des distances dans l’espace de l’appareil photo. Les paramètres décrivent les dimensions du volume de la vue.

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, la fonction D3DXMatrixOrthoOffCenterLH peut être utilisée comme paramètre pour une autre fonction.

Cette fonction utilise la formule suivante pour calculer la matrice retournée.


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zf-zn)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
