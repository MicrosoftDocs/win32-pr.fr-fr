---
description: Description d’une constante dans une table constante.
ms.assetid: d1970536-7195-4270-a1b9-b082ebe4f17f
title: Structure D3DXCONSTANT_DESC (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCONSTANT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: d737fa1d95a119668602aeb056e15bc4248200aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531361"
---
# <a name="d3dxconstant_desc-structure"></a>D3DXCONSTANT \_ desc, structure

Description d’une constante dans une table constante.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXCONSTANT_DESC {
  LPCSTR              Name;
  D3DXREGISTER_SET    RegisterSet;
  UINT                RegisterIndex;
  UINT                RegisterCount;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                StructMembers;
  UINT                Bytes;
  LPCVOID             DefaultValue;
} D3DXCONSTANT_DESC, *LPD3DXCONSTANT_DESC;
```



## <a name="members"></a>Membres

<dl> <dt>

**Nom**
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Nom de la constante.

</dd> <dt>

**RegisterSet**
</dt> <dd>

Type : **[ **D3DXREGISTER \_ Set**](./d3dxregister-set.md)**

</dd> <dd>

Type de données constant. Consultez [**D3DXREGISTER \_ Set**](./d3dxregister-set.md).

</dd> <dt>

**RegisterIndex**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Index de base zéro de la constante dans la table.

</dd> <dt>

**RegisterCount**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de registres qui contiennent des données.

</dd> <dt>

**Classe**
</dt> <dd>

Type : **[ **D3DXPARAMETER, \_ classe**](./d3dxparameter-class.md)**

</dd> <dd>

Classe de paramètre. Consultez [**la \_ classe D3DXPARAMETER**](./d3dxparameter-class.md).

</dd> <dt>

**Type**
</dt> <dd>

Type : **[ **D3DXPARAMETER \_**](./d3dxparameter-type.md)**

</dd> <dd>

Type de paramètre. Consultez [**\_ type D3DXPARAMETER**](./d3dxparameter-type.md).

</dd> <dt>

**Lignes**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de lignes.

</dd> <dt>

**Colonnes**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de colonnes.

</dd> <dt>

**Éléments**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre d’éléments dans le tableau.

</dd> <dt>

**StructMembers**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de sous-paramètres de membre de structure.

</dd> <dt>

**Octets**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Taille des données en nombre d’octets.

</dd> <dt>

**DefaultValue**
</dt> <dd>

Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Pointeur vers la valeur par défaut.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXCONSTANTTABLE \_ desc**](d3dxconstanttable-desc.md)
</dt> </dl>

 

 
