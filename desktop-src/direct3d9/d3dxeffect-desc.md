---
description: Décrit un objet Effect.
ms.assetid: 161d3e7a-213a-4a83-a1b5-837b0aab96bf
title: Structure D3DXEFFECT_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: c8e7a3a2adf19514e2e4d1c6f61dbea888ce033d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012823"
---
# <a name="d3dxeffect_desc-structure"></a>D3DXEFFECT \_ desc, structure

Décrit un objet Effect.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXEFFECT_DESC {
  LPCSTR Creator;
  UINT   Parameters;
  UINT   Techniques;
  UINT   Functions;
} D3DXEFFECT_DESC, *LPD3DXEFFECT_DESC;
```



## <a name="members"></a>Membres

<dl> <dt>

**Creator**
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Chaîne qui contient le nom du créateur de l’effet.

</dd> <dt>

**Paramètres**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de paramètres utilisés pour l’effet.

</dd> <dt>

**Technologie**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de techniques pouvant rendre l’effet.

</dd> <dt>

**Fonctions**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de fonctions qui peuvent rendre l’effet.

</dd> </dl>

## <a name="remarks"></a>Notes

Un objet Effect peut contenir plusieurs techniques et paramètres de rendu pour le même effet.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’effet](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
