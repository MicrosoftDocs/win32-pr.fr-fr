---
description: Fonction D3DXVec3Hermite (D3dx9math. h)-effectue une interpolation spline Hermite à l’aide des vecteurs 3D spécifiés.
ms.assetid: d45b1179-0e11-4f58-8d50-432236cb88ca
title: D3DXVec3Hermite, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Hermite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fd45851108d3700446a2b7f27aa00a4cc61ca39b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097867"
---
# <a name="d3dxvec3hermite-function-d3dx9mathh"></a>D3DXVec3Hermite, fonction (D3dx9math. h)

Effectue une interpolation spline Hermite à l’aide des vecteurs 3D spécifiés.

## <a name="syntax"></a>Syntaxe


```C++
D3DXVECTOR3* D3DXVec3Hermite(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pT1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Pointeur vers la structure [**D3DXVECTOR3**](d3dxvector3.md) qui est le résultat de l’opération.

</dd> <dt>

*pV1* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers une structure source [**D3DXVECTOR3**](d3dxvector3.md) , un vecteur de position.

</dd> <dt>

*pt1* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers une structure source [**D3DXVECTOR3**](d3dxvector3.md) , un vecteur tangent.

</dd> <dt>

*pV2* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers une structure source [**D3DXVECTOR3**](d3dxvector3.md) , un vecteur de position.

</dd> <dt>

*Pt2* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers une structure source [**D3DXVECTOR3**](d3dxvector3.md) , un vecteur tangent.

</dd> <dt>

 \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Facteur de pondération. Consultez la section Notes.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) qui est le résultat de l’interpolation spline Hermite.

## <a name="remarks"></a>Notes 

La fonction **D3DXVec3Hermite** interpole de (positiona, tangenta) à (PositionB, tangentB) à l’aide de l’interpolation spline Hermite.

L’interpolation spline est une généralisation de l’accélération et de la simplicité de la spline. La rampe est une fonction de Q (s) avec les propriétés suivantes.

Q (s) = As ³ + BS ² + CS + D (et par conséquent, Q' (s) = 3As ² + 2Bs + C)

a) Q (0) = v1, Q' (0) = T1

b) Q (1) = v2, Q' (1) = T2

v1 est le contenu de pV1, v2 dans le contenu de pV2, T1 est le contenu de pT1, et T2 est le contenu de pT2.

Ces propriétés sont utilisées pour résoudre A, B, C, D.

``` syntax
D = v1  (from a)
C = t1  (from a)
3A + 2B = t2 - t1 (substituting for C)
A + B = v2 - v1 - t1 (substituting for C and D)
```

Branchez les solutions pour A, B, C et D pour générer Q (s).

``` syntax
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```

Cela donne :

Q (s) = (2V1-2V2 + T2 + T1) s ³ + (3V2-3V1-2t1-T2) s ² + T1S + v1

Qui peuvent être réorganisés comme suit :

Q (s) = (2S ³-3S ² + 1) v1 + (-2S ³ + 3S ²) v2 + (s ³-2S ² + s) T1 + (s ³-s ²) T2

Les splines Hermite sont utiles pour le contrôle de l’animation, car la courbe s’exécute à travers tous les points de contrôle. En outre, étant donné que la position et la tangente sont explicitement spécifiées aux extrémités de chaque segment, il est facile de créer une courbe continue C2 tant que vous vous assurez que votre position de départ et la tangente correspondent aux valeurs de fin du dernier segment.

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, la fonction **D3DXVec3Hermite** peut être utilisée comme paramètre pour une autre fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
