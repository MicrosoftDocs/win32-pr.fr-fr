---
description: Définit une plage.
ms.assetid: 28e8c478-f6ce-4f75-95c6-ea2d08424238
title: D3DRANGE, structure (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRANGE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 15ff267528ddfd12f8da77921e2edc2d836e1a39
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855190"
---
# <a name="d3drange-structure"></a>D3DRANGE, structure

Définit une plage.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DRANGE {
  UINT Offset;
  UINT Size;
} D3DRANGE, *LPD3DRANGE;
```



## <a name="members"></a>Membres

<dl> <dt>

**Offset**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Décalage, en octets.

</dd> <dt>

**Taille**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Taille, en octets.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
