---
description: Décrit les valeurs de couleur.
ms.assetid: 53d3176a-f727-498e-8bea-0e30e0a1c66e
title: D3DXCOLOR, structure (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOLOR
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: c7e5c1ac12341ccf6272714511959ee9a131ba4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106524865"
---
# <a name="d3dxcolor-structure-d3dx9mathh"></a>D3DXCOLOR, structure (D3dx9math. h)

Décrit les valeurs de couleur.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXCOLOR {
  FLOAT r;
  FLOAT g;
  FLOAT b;
  FLOAT a;
} D3DXCOLOR, *LPD3DXCOLOR;
```



## <a name="members"></a>Membres

<dl> <dt>

**r**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Composant rouge de la couleur.

</dd> <dt>

**activée**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Composant vert de la couleur.

</dd> <dt>

**b**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Composant bleu de la couleur.

</dd> <dt>

**un**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Composant alpha de la couleur.

</dd> </dl>

## <a name="remarks"></a>Notes

Les programmeurs C++ peuvent tirer parti de la surcharge d’opérateur et de la conversion de type avec les [**Extensions D3DXCOLOR**](d3dxcolor-extensions.md), qui implémentent des constructeurs surchargés, ainsi que des opérateurs d’assignation, unaires et binaires (y compris l’égalité).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
