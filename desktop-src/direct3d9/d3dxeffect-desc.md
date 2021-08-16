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
ms.openlocfilehash: 0b30ad0348a5c799690d668e036724d30808c2998eee9d762fa2ad3fc8106c91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298592"
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’effet](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
