---
description: Retourne un vecteur 2D composé des composants les plus petits de deux vecteurs 2D.
ms.assetid: 6944523e-33dd-456e-9cc2-17760d76c548
title: D3DXVec2Minimize, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Minimize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da16c90ee5757ec72ee98932164a7281194553e63b4921ca42c666f660f7f904
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044627"
---
# <a name="d3dxvec2minimize-function"></a>D3DXVec2Minimize fonction)

Retourne un vecteur 2D composé des composants les plus petits de deux vecteurs 2D.

## <a name="syntax"></a>Syntaxe


```C++
D3DXVECTOR2* D3DXVec2Minimize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*moue* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Pointeur vers la structure [**D3DXVECTOR2**](d3dxvector2.md) qui est le résultat de l’opération.

</dd> <dt>

*pV1* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) source.

</dd> <dt>

*pV2* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) source.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) composée des plus petits composants des deux vecteurs.

## <a name="remarks"></a>Remarques

La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* . De cette façon, la fonction **D3DXVec2Minimize** peut être utilisée comme paramètre pour une autre fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2Maximize**](d3dxvec2maximize.md)
</dt> </dl>

 

 




