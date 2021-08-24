---
description: Décrit un paramètre utilisé pour un objet Effect.
ms.assetid: 60d19b52-67ef-4903-bbde-922a8fac1ad8
title: Structure D3DXPARAMETER_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: a12541e9bfb33979b11f8198e218a3eb474f948aeb8c74982a5369eed782eaa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631149"
---
# <a name="d3dxparameter_desc-structure"></a>D3DXPARAMETER \_ desc, structure

Décrit un paramètre utilisé pour un objet Effect.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXPARAMETER_DESC {
  LPCSTR              Name;
  LPCSTR              Semantic;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                Annotations;
  UINT                StructMembers;
  DWORD               Flags;
  UINT                Bytes;
} D3DXPARAMETER_DESC, *LPD3DXPARAMETER_DESC;
```



## <a name="members"></a>Membres

<dl> <dt>

**Nom**
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Nom du paramètre.

</dd> <dt>

**Équivalent**
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

La signification sémantique, également appelée utilisation.

</dd> <dt>

**Classe**
</dt> <dd>

Type : **[ **D3DXPARAMETER, \_ classe**](./d3dxparameter-class.md)**

</dd> <dd>

Classe de paramètre. Définissez cette valeur sur l’une des valeurs de la [**\_ classe D3DXPARAMETER**](./d3dxparameter-class.md).

</dd> <dt>

**Type**
</dt> <dd>

Type : **[ **D3DXPARAMETER \_**](./d3dxparameter-type.md)**

</dd> <dd>

Type de paramètre. Définissez cette valeur sur l’une des valeurs [**de \_ type D3DXPARAMETER**](./d3dxparameter-type.md).

</dd> <dt>

**Lignes**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de lignes dans le tableau.

</dd> <dt>

**Colonnes**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de colonnes dans le tableau.

</dd> <dt>

**Éléments**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre d’éléments dans le tableau.

</dd> <dt>

**Annotations**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre d’annotations.

</dd> <dt>

**StructMembers**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de membres de structure.

</dd> <dt>

**Indicateurs**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Attributs du paramètre. Consultez [effets, constantes](dx9-graphics-reference-effects-constants.md).

</dd> <dt>

**Octets**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Taille du paramètre, en octets.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’effet](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
