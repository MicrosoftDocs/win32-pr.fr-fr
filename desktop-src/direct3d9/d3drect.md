---
description: Définit un rectangle.
ms.assetid: a8590411-fd34-4048-a41f-b4155d955573
title: D3DRECT, structure (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 5e202ae058cdc30b79e2cc579a064b597d0013f7447e70f0fd6d996d9740a830
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732283"
---
# <a name="d3drect-structure"></a>D3DRECT, structure

Définit un rectangle.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DRECT {
  LONG x1;
  LONG y1;
  LONG x2;
  LONG y2;
} D3DRECT;
```



## <a name="members"></a>Membres

<dl> <dt>

**x1**
</dt> <dd>

Type : **[ **long**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordonnée x du coin supérieur gauche du rectangle.

</dd> <dt>

**y1**
</dt> <dd>

Type : **[ **long**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordonnée y du coin supérieur gauche du rectangle.

</dd> <dt>

**x2**
</dt> <dd>

Type : **[ **long**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordonnée x du coin inférieur droit du rectangle.

</dd> <dt>

**Y2**
</dt> <dd>

Type : **[ **long**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordonnée y du coin inférieur droit du rectangle.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**Effacer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear)
</dt> </dl>

 

 
