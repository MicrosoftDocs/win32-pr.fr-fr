---
description: D3DXCOLOR structure (D3dx9math. h)-décrit les valeurs de couleur.
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
ms.openlocfilehash: 28f170814988317cd1cdf3300e4cbb3c2a97fa0fac7a43b2231767914a9b103a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988719"
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

## <a name="remarks"></a>Remarques

Les programmeurs C++ peuvent tirer parti de la surcharge d’opérateur et de la conversion de type avec les [**Extensions D3DXCOLOR**](d3dxcolor-extensions.md), qui implémentent des constructeurs surchargés, ainsi que des opérateurs d’assignation, unaires et binaires (y compris l’égalité).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
