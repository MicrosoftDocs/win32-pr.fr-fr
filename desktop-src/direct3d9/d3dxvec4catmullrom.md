---
description: D3DXVec4CatmullRom, fonction (D3dx9math. h)-effectue une interpolation Catmull-Rom à l’aide des vecteurs 4D spécifiés.
ms.assetid: 24c26e70-b02c-4621-8b7e-db16f99dddb5
title: D3DXVec4CatmullRom, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4CatmullRom
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7f55eb0434b36daca81e8e3e93b335c2d58124a53d31d59d20ddaa525a6b1c04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118803767"
---
# <a name="d3dxvec4catmullrom-function-d3dx9mathh"></a>D3DXVec4CatmullRom, fonction (D3dx9math. h)

Effectue une interpolation Catmull-Rom à l’aide des vecteurs 4D spécifiés.

## <a name="syntax"></a>Syntaxe


```C++
D3DXVECTOR4* D3DXVec4CatmullRom(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV0,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Pointeur vers la structure [**D3DXVECTOR4**](d3dxvector4.md) qui est le résultat de l’opération.

</dd> <dt>

*pV0* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Pointeur vers une structure source [**D3DXVECTOR4**](d3dxvector4.md) , un vecteur de position.

</dd> <dt>

*pV1* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Pointeur vers une structure source [**D3DXVECTOR4**](d3dxvector4.md) , un vecteur de position.

</dd> <dt>

*pV2* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Pointeur vers une structure source [**D3DXVECTOR4**](d3dxvector4.md) , un vecteur de position.

</dd> <dt>

*pV3* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Pointeur vers une structure source [**D3DXVECTOR4**](d3dxvector4.md) , un vecteur de position.

</dd> <dt>

 \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Facteur de pondération. Consultez la section Notes.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) qui est le résultat de l’interpolation Catmull-Rom.

## <a name="remarks"></a>Remarques

À partir de quatre points (P1, P2, P3, P4), recherchez une fonction Q (s) de ce type :


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



Le Catmull-Rom spline peut être dérivé de la spline Hermite en définissant :


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



où :

v1 est le contenu de pV0.

v2 dans le contenu de pV1.

P3 est le contenu de pV2.

P4 est le contenu de pV3.

À l’aide de l’équation spline Hermite :


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



et le remplacement de v1, v2, T1, T2 donne :


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2) / 2
```



Cette réorganisation peut être réorganisée comme suit :


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
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

[**D3DXVec2CatmullRom**](d3dxvec2catmullrom.md)
</dt> <dt>

[**D3DXVec3CatmullRom**](d3dxvec3catmullrom.md)
</dt> </dl>

 

 
