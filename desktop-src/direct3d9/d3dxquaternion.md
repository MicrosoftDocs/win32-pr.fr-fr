---
description: Décrit un Quaternion.
ms.assetid: 3d88ed17-5b0a-46d5-8fe6-d66e1fa26c13
title: D3DXQUATERNION, structure (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQUATERNION
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 59d3f147e8eb233b9197394bad738d19d9ceba5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106543561"
---
# <a name="d3dxquaternion-structure-d3dx9mathh"></a>D3DXQUATERNION, structure (D3dx9math. h)

Décrit un Quaternion.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a>Membres

<dl> <dt>

**x**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Composant x.

</dd> <dt>

**y**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Composant y.

</dd> <dt>

**z**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Composant z.

</dd> <dt>

**w**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Composant w.

</dd> </dl>

## <a name="remarks"></a>Notes

Les quaternions ajoutent un quatrième élément aux \[ valeurs x, y, z \] qui définissent un vecteur, entraînant des vecteurs 4D arbitraires. Toutefois, l’exemple suivant illustre la façon dont chaque élément d’un Quaternion d’unité se réfère à une rotation de l’axe d’un axe (où q représente un Quaternion d’unité (x, y, z, w), l’axe est normalisé et Theta la rotation CCW souhaitée sur l’axe) :


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



Les programmeurs C++ peuvent tirer parti de la surcharge d’opérateur et de la conversion de type avec les [**Extensions D3DXQUATERNION**](d3dxquaternion-extensions.md), qui implémentent des constructeurs surchargés et des opérateurs d’assignation, unaires et binaires (y compris l’égalité).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[Vecteurs, vertex et quaternions (Direct3D 9)](vectors--vertices--and-quaternions.md)
</dt> </dl>

 

 
