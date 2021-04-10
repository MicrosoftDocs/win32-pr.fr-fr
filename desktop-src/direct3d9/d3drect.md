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
ms.openlocfilehash: 9a22b74869afa16ca0c55ac50975eb36ba590c7a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762098"
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

[**Effacé**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear)
</dt> </dl>

 

 
