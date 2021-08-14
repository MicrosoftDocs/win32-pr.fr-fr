---
description: Structure d’assistance qui contient les informations de structure de membre.
ms.assetid: 2fbe5e97-047e-48bf-9413-dd297632288a
title: Structure D3DXSHADER_STRUCTMEMBERINFO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_STRUCTMEMBERINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 6f41c3d1911a046165d929bee50ef4e0b5691cebee9d90007bc367636e343731
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524212"
---
# <a name="d3dxshader_structmemberinfo-structure"></a>D3DXSHADER \_ STRUCTMEMBERINFO, structure

Structure d’assistance qui contient les informations de structure de membre.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXSHADER_STRUCTMEMBERINFO {
  DWORD Name;
  DWORD TypeInfo;
} D3DXSHADER_STRUCTMEMBERINFO, *LPD3DXSHADER_STRUCTMEMBERINFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**Nom**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset à partir du début de cette structure, en octets, à la chaîne qui contient le nom du membre de structure.

</dd> <dt>

**TypeInfo**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset à partir du début de cette structure, en octets, à la chaîne qui contient les informations de type. Consultez [**D3DXSHADER \_ TypeInfo**](d3dxshader-typeinfo.md).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSHADER \_ TypeInfo**](d3dxshader-typeinfo.md)
</dt> </dl>

 

 
