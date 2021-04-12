---
description: Structure d’assistance qui contient les informations de type de membre.
ms.assetid: 5580122d-c700-4632-8fcf-903519f2429e
title: Structure D3DXSHADER_TYPEINFO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_TYPEINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 71b9cc893cdcfdc9802aca173627cd9da4f9ca4b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322862"
---
# <a name="d3dxshader_typeinfo-structure"></a>D3DXSHADER \_ TypeInfo, structure

Structure d’assistance qui contient les informations de type de membre.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXSHADER_TYPEINFO {
  WORD  Class;
  WORD  Type;
  WORD  Rows;
  WORD  Columns;
  WORD  Elements;
  WORD  StructMembers;
  DWORD StructMemberInfo;
} D3DXSHADER_TYPEINFO, *LPD3DXSHADER_TYPEINFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**Classe**
</dt> <dd>

Type : **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Type d’objet Shader. Consultez [**la \_ classe D3DXPARAMETER**](./d3dxparameter-class.md).

</dd> <dt>

**Type**
</dt> <dd>

Type : **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Type de données. Consultez [**\_ type D3DXPARAMETER**](./d3dxparameter-type.md).

</dd> <dt>

**Lignes**
</dt> <dd>

Type : **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de lignes de matrice (matrices).

</dd> <dt>

**Colonnes**
</dt> <dd>

Type : **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de colonnes (vecteurs et matrices).

</dd> <dt>

**Éléments**
</dt> <dd>

Type : **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimension du tableau.

</dd> <dt>

**StructMembers**
</dt> <dd>

Type : **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de membres de structure.

</dd> <dt>

**StructMemberInfo**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Tableau d’informations sur les membres de la structure, D3DXSHADER \_ STRUCTMEMBERINFO \[ *StructMembers* \] . Consultez [**D3DXSHADER \_ STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).

</dd> </dl>

## <a name="remarks"></a>Notes

Les informations de type font partie de [**D3DXSHADER \_ STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSHADER \_ CONSTANTINFO**](d3dxshader-constantinfo.md)
</dt> </dl>

 

 
