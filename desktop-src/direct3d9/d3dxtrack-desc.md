---
description: Décrit une piste d’animation et spécifie le poids de fusion, la vitesse et la position de la piste à un moment donné.
ms.assetid: f1469b6f-861f-4b7d-a187-933092a5d257
title: Structure D3DXTRACK_DESC (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRACK_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: cddabb3ea79951e35831c2cdc32e11baeb5c7c1c4ce174fd29d9382edb391953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731116"
---
# <a name="d3dxtrack_desc-structure"></a>D3DXTRACK \_ desc, structure

Décrit une piste d’animation et spécifie le poids de fusion, la vitesse et la position de la piste à un moment donné.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXTRACK_DESC {
  D3DXPRIORITY_TYPE Priority;
  FLOAT             Weight;
  FLOAT             Speed;
  DOUBLE            Position;
  BOOL              Enable;
} D3DXTRACK_DESC, *LPD3DXTRACK_DESC;
```



## <a name="members"></a>Membres

<dl> <dt>

**Priorité**
</dt> <dd>

Type : **[ **D3DXPRIORITY \_**](./d3dxpriority-type.md)**

</dd> <dd>

Type de priorité, tel que défini dans [**D3DXPRIORITY \_ type**](./d3dxpriority-type.md).

</dd> <dt>

**Poids**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valeur de poids. Le poids détermine la proportion de cette piste à mélanger avec d’autres pistes.

</dd> <dt>

**Vitesse**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valeur de vitesse. Cela est utilisé de la même façon qu’un multiplicateur pour mettre à l’échelle la période de la piste.

</dd> <dt>

**Position**
</dt> <dd>

Type : **[ **double**](../winprog/windows-data-types.md)**

</dd> <dd>

Position horaire de la piste, dans la plage locale de son ensemble d’animations actuel.

</dd> <dt>

**Activer**
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Suivi d’activation/désactivation. Pour activer, affectez à la valeur **true**. Pour désactiver, affectez la valeur **false**.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les pistes avec la même priorité sont fusionnées ensemble, et les deux valeurs résultantes sont ensuite fusionnées à l’aide du facteur de fusion de priorité. Une piste doit avoir un ensemble d’animations (stocké séparément) qui lui est associé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
