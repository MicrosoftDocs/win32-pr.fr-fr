---
description: Décrit un plan.
ms.assetid: ffca4650-9788-4559-8f6b-a4e5db29ce55
title: D3DXPLANE, structure (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLANE
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 260f9555313aea3443f0728f2b50189228429803
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525852"
---
# <a name="d3dxplane-structure-d3dx9mathh"></a>D3DXPLANE, structure (D3dx9math. h)

Décrit un plan.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a>Membres

<dl> <dt>

**un**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Coefficient du plan de découpage dans l’équation du plan général. Consultez la section Notes.

</dd> <dt>

**b**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Coefficient b du plan de découpage dans l’équation du plan général. Consultez la section Notes.

</dd> <dt>

**c**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Coefficient c du plan de découpage dans l’équation du plan général. Consultez la section Notes.

</dd> <dt>

**d**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Coefficient d du plan de découpage dans l’équation du plan général. Consultez la section Notes.

</dd> </dl>

## <a name="remarks"></a>Notes

Les membres de la structure **D3DXPLANE** prennent la forme de l’équation plan générale. Elles s’intègrent à l’équation plan générale, **de** sorte que x + **b** y + **c** z + **d** w = 0.

Les programmeurs C++ peuvent tirer parti de la surcharge d’opérateur et de la conversion de type avec les [**Extensions D3DXPLANE**](d3dxplane-extensions.md) qui implémentent des constructeurs surchargés et des opérateurs d’assignation, unaires et binaires (y compris l’égalité).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
