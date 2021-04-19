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
ms.openlocfilehash: 12f1604cf954bcdd6a2a898fec5410804112e498
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542155"
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

## <a name="remarks"></a>Notes

Les pistes avec la même priorité sont fusionnées ensemble, et les deux valeurs résultantes sont ensuite fusionnées à l’aide du facteur de fusion de priorité. Une piste doit avoir un ensemble d’animations (stocké séparément) qui lui est associé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
