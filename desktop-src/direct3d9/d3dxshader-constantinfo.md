---
description: D3DXSHADER \_ CONSTANTINFO, structure
ms.assetid: 0c42cea7-559e-4475-b66a-e932a9cb42de
title: Structure D3DXSHADER_CONSTANTINFO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: e90c0085035e78b9bc3ce1c48642157d8badc924
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211744"
---
# <a name="d3dxshader_constantinfo-structure"></a>D3DXSHADER \_ CONSTANTINFO, structure

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXSHADER_CONSTANTINFO {
  DWORD Name;
  WORD  RegisterSet;
  WORD  RegisterIndex;
  WORD  RegisterCount;
  WORD  Reserved;
  DWORD TypeInfo;
  DWORD DefaultValue;
} D3DXSHADER_CONSTANTINFO, *LPD3DXSHADER_CONSTANTINFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**Nom**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset à partir du début de cette structure, en octets, à la chaîne qui contient les informations de constante.

</dd> <dt>

**RegisterSet**
</dt> <dd>

Type : **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Ensemble de registres. Consultez [**D3DXREGISTER \_ Set**](./d3dxregister-set.md).

</dd> <dt>

**RegisterIndex**
</dt> <dd>

Type : **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Index du Registre.

</dd> <dt>

**RegisterCount**
</dt> <dd>

Type : **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de registres.

</dd> <dt>

**Reserved**
</dt> <dd>

Type : **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Réservé.

</dd> <dt>

**TypeInfo**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset à partir du début de cette structure, en octets, à la chaîne qui contient les informations [**\_ TypeInfo D3DXSHADER**](d3dxshader-typeinfo.md) .

</dd> <dt>

**DefaultValue**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset à partir du début de cette structure, en octets, à la chaîne qui contient la valeur par défaut.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
