---
description: Retourne le carré de la longueur d’un vecteur 4D.
ms.assetid: 73091179-4acb-408b-8c91-766052999f26
title: D3DXVec4LengthSq, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4LengthSq
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c2ac165c27ad0e29579cbde165c48adb98853b16b17ebc3b022c3ba5711e52b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118095205"
---
# <a name="d3dxvec4lengthsq-function"></a>D3DXVec4LengthSq fonction)

Retourne le carré de la longueur d’un vecteur 4D.

## <a name="syntax"></a>Syntaxe


```C++
FLOAT D3DXVec4LengthSq(
  _In_ const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PV* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Pointeur vers la structure [**D3DXVECTOR4**](d3dxvector4.md) source.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **float**](../winprog/windows-data-types.md)**

Longueur au carré du vecteur.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec4Length**](d3dxvec4length.md)
</dt> </dl>

 

 
