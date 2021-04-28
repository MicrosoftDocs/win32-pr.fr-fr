---
description: D3DXQUATERNION, structure (D3DX10Math. h)-décrit un Quaternion.
ms.assetid: e6cb45b2-3132-4315-b02d-a3dfc444f8cc
title: D3DXQUATERNION, structure (D3DX10Math. h)
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
- D3DX10Math.h
ms.openlocfilehash: dac880607cf482b409c407b43992747af4aa39a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103247"
---
# <a name="d3dxquaternion-structure-d3dx10mathh"></a>D3DXQUATERNION, structure (D3DX10Math. h)

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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
