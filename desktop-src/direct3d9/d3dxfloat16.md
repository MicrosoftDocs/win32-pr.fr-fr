---
description: Décrit un vecteur à virgule flottante 16 bits.
ms.assetid: f823a327-f07a-44e9-b58a-7865e11e80eb
title: D3DXFLOAT16, structure (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFLOAT16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 4b469c770b811ed11ec21b21d2b449df1fd75b1c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520323"
---
# <a name="d3dxfloat16-structure-d3dx9mathh"></a>D3DXFLOAT16, structure (D3dx9math. h)

Décrit un vecteur à virgule flottante 16 bits.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXFLOAT16 {
  WORD Value;
} D3DXFLOAT16, *LPD3DXFLOAT16;
```



## <a name="members"></a>Membres

<dl> <dt>

**Valeur**
</dt> <dd>

Type : **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Données 16 bits.

</dd> </dl>

## <a name="remarks"></a>Notes

Les programmeurs C++ peuvent tirer parti de la surcharge d’opérateur et de la conversion de type avec les [**Extensions D3DXFLOAT16**](d3dxfloat16-extensions.md), qui implémentent des constructeurs surchargés et des opérateurs d’assignation, unaires et binaires (y compris l’égalité).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
