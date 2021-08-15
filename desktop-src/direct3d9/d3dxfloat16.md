---
description: D3DXFLOAT16 structure (D3dx9math. h)-décrit un vecteur à virgule flottante 16 bits.
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
ms.openlocfilehash: c6f1c204dfe674a2c2db995e158891ea03ca571b00c0fc4f49f4e52884042c34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526063"
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

## <a name="remarks"></a>Remarques

Les programmeurs C++ peuvent tirer parti de la surcharge d’opérateur et de la conversion de type avec les [**Extensions D3DXFLOAT16**](d3dxfloat16-extensions.md), qui implémentent des constructeurs surchargés et des opérateurs d’assignation, unaires et binaires (y compris l’égalité).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
