---
description: 'D3DXPlaneFromPoints, fonction (D3DX10Math. h) : construit un plan à partir de trois points.'
ms.assetid: 0e77af1b-cedf-482c-8398-10becb398a2c
title: D3DXPlaneFromPoints, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPoints
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 07275d7a67527959396ba82f7e0fb8cbbc39b27d7e3adeca70df2e174fe09258
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895379"
---
# <a name="d3dxplanefrompoints-function-d3dx10mathh"></a>D3DXPlaneFromPoints, fonction (D3DX10Math. h)

Construit un plan à partir de trois points.

## <a name="syntax"></a>Syntaxe


```C++
D3DXPLANE* D3DXPlaneFromPoints(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Pointeur vers le [**D3DXPLANE**](d3d10-d3dxplane.md) qui est le résultat de l’opération.

</dd> <dt>

*pV1* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Pointeur vers un [**D3DXVECTOR3**](d3d10-d3dxvector3.md), définissant l’un des points utilisés pour construire le plan.

</dd> <dt>

*pV2* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Pointeur vers une structure D3DXVECTOR3, définissant l’un des points utilisés pour construire le plan.

</dd> <dt>

*pV3* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Pointeur vers une structure D3DXVECTOR3, définissant l’un des points utilisés pour construire le plan.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Pointeur vers la structure D3DXPLANE construite à partir des points donnés.

## <a name="remarks"></a>Remarques

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue. De cette façon, la fonction D3DXPlaneFromPoints peut être utilisée comme paramètre pour une autre fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
