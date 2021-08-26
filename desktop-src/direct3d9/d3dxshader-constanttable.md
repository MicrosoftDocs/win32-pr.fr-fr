---
description: Structure d’assistance pour la gestion d’une table de constantes de nuanceur. Cela peut également être fait à l’aide de ID3DXConstantTable.
ms.assetid: cc6d66e4-c600-420b-b7b5-1bd10ecb22f9
title: Structure D3DXSHADER_CONSTANTTABLE (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTTABLE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: f423eba3187c6bbc5c17d4ba9284e4e1b2048a016b8a11744b83b46e4d8522af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027289"
---
# <a name="d3dxshader_constanttable-structure"></a>D3DXSHADER \_ CONSTANTTABLE, structure

Structure d’assistance pour la gestion d’une table de constantes de nuanceur. Cela peut également être fait à l’aide de [**ID3DXConstantTable**](id3dxconstanttable.md).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXSHADER_CONSTANTTABLE {
  DWORD Size;
  DWORD Creator;
  DWORD Version;
  DWORD Constants;
  DWORD ConstantInfo;
  DWORD Flags;
  DWORD Target;
} D3DXSHADER_CONSTANTTABLE, *LPD3DXSHADER_CONSTANTTABLE;
```



## <a name="members"></a>Membres

<dl> <dt>

**Taille**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Taille de la structure. Consultez la section Notes.

</dd> <dt>

**Creator**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset à partir du début de cette structure, en octets, à la chaîne qui contient le nom du créateur.

</dd> <dt>

**Version**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Version du nuanceur.

</dd> <dt>

**Constantes**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de constantes.

</dd> <dt>

**ConstantInfo**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Tableau d’informations constantes, \_ \[ *constantes* CONSTANTINFO D3DXSHADER \] . Consultez [**D3DXSHADER \_ CONSTANTINFO**](d3dxshader-constantinfo.md).

</dd> <dt>

**Indicateurs**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Indicateurs [D3DXSHADER Flags](d3dxshader-flags.md) utilisés pour compiler le nuanceur.

</dd> <dt>

**Cible**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset dans la chaîne qui contient la cible.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les informations de constante de nuanceur sont incluses dans une table de commentaires délimitée par des tabulations. Tous les décalages sont mesurés en octets à partir du début de la structure. Les entrées de la table constante sont triées par créateur dans l’ordre croissant.

Une table de constantes de nuanceur peut être gérée avec les interfaces [**ID3DXConstantTable**](id3dxconstanttable.md) . Vous pouvez également gérer la table constante avec **D3DXSHADER \_ CONSTANTTABLE**.

Ce membre de taille est souvent initialisé à l’aide des éléments suivants :


```
D3DXSHADER_CONSTANTTABLE constantTable;
constantTable.Size = sizeof(D3DXSHADER_CONSTANTTABLE)
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
