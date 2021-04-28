---
description: D3DXPLANE structure (D3DX10Math. h)-décrit un plan.
ms.assetid: c6da7343-a4f3-4cac-855b-14bd70c0d3c2
title: D3DXPLANE, structure (D3DX10Math. h)
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
- D3DX10Math.h
ms.openlocfilehash: 440246fb47a851f9f5339c72a484a2cb59e8f662
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103327"
---
# <a name="d3dxplane-structure-d3dx10mathh"></a>D3DXPLANE, structure (D3DX10Math. h)

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

Les membres de la structure **D3DXPLANE** prennent la forme de l’équation plan générale. Elles s’inscrivent dans l’équation plan générale, de sorte que ax + by + CZ + DW = 0.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
